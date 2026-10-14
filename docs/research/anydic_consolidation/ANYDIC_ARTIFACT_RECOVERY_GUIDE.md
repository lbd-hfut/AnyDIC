# 科研资产恢复指南

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

主仓库：`${ANYDIC_REPOSITORY}`。资产根目录：`${ANYDIC_RESEARCH_ARCHIVE}`。每个 worktree 完整文件清单位于 `manifests/<原worktree名>.json`，包括相对路径、大小、SHA256、Git类别、原分支/HEAD、归档路径和校验状态。汇总入口为 [ARCHIVE_MANIFEST](ARCHIVE_MANIFEST.json)。原始绝对路径是来源，不是当前运行默认。

只读读取原 Decision 无需额外 checkout：

```bash
cd "${ANYDIC_REPOSITORY}"
git show caba509f21de6f698c01e8ef685851c0b2dca887:docs/results/anydic_c16/C16_A_RESULTS_SUMMARY.json
```

后续需要重开时，先检查分支是否仍被保护 worktree 占用；仅在该分支未 checkout 时运行：

```bash
cd "${ANYDIC_REPOSITORY}"
git worktree add \
  ${ANYDIC_WORKTREES}/anydic-c16-reopened \
  experiment/anydic-c16-native-update-stability
```

本次仅记录示例，未在清理后重新创建 checkout。当前受保护 C16 若仍存在，应先使用它或为指定 SHA 创建 detached 临时 checkout，不能强抢分支。

Git 恢复 tracked 代码、图表和报告。ignored/untracked 的 runs、checkpoint、原始GT、预测、日志、外部源码/内部.git、完整隔离环境来自 `worktree_assets/<原worktree名>/<relative_path>`。先通过 manifest 检查来源身份和完整 SHA256，再向空目的路径复制，禁止覆盖不同内容或往旧科研输出重跑。恢复文件以8MiB分块 `hashlib.sha256` 计算；symlink 的 manifest hash 对应链接目标文本，另检查外部目标存在。

符号链接恢复另见外部 `verification/SYMLINK_RECOVERY_MAP.json`：12个环境链接目标仍存在；6个MEDIUM M1 pytest `current`绝对路径别名的目标目录已随完整runs归档，按该映射直接访问新目标即可。原链接文本和SHA256未修改，不要以旧绝对链接无法直接跟随推断目标数据丢失。另有3个浏览器profile `lock`链接的目标文本为`LOOPBACK:+PID`，初始完整清单中就无对应目标文件；锁标记原样保留，不是需恢复的科研文件。需要重建别名时在新的恢复工作区操作，不覆盖本归档的原始链接证据。

原实验代码/配置经常硬编码历史绝对路径。保留原相对结构，在新分支以显式 artifact root/config 或经过审计的路径适配修复引用，避免修改生产 LOW 或覆盖原始 evidence。C13/C14/C15/C16 依赖冻结 C11 与 C15 原始 checkpoint/源码，其全映射见模型索引；移动路径本身不提供数值等价证明。

环境：原环境记录由 [RESEARCH_SOURCE_INDEX](RESEARCH_SOURCE_INDEX.json) 的 environment_manifests 定位；额外环境/外部Git版本收据见外部 `verification/ENVIRONMENT_RECOVERY.json`。C11 成功计算使用 Python3.13.12/PyTorch2.13.0+cu130/CUDA13.0，env-official 使用原 base system-site-packages；env-sea3.9/env-flow3.10 是失败尝试。C16 重建是同版本 CPU（4 threads），不能声称 GPU 数值等价。全部原 venv 数据保留，移动后 activate/shebang 绝对前缀可能失效，应按原清单在新路径重建而非自动删环境；外部 conda/base 环境不在本次移动范围。

生产 V2 权重仍位于 `${LOCAL_HOME}/releases/AnyDIC/anydic-v2.0-final/`，GMFlow 权重/源码仍位于 `${LOCAL_HOME}/externals/phase4q/`；早先 runtime 归档仍位于 `${LOCAL_HOME}/releases/AnyDIC/historical-runtime-archive/`。本轮不搬动这些外部既有权威。主项目 `case/dic_challenge/`、TIFF、原始压缩包和 `.git` 均原位保留。

禁止把恢复 checkout 等同于大型模型/GT已经恢复。至少核验 checkpoint 和一个真实结果文件的 SHA256/只读结构；GPU数值复现须另行按原精度/TF32/metadata协议运行，不能用本轮文件完整性审计替代科研再现。
