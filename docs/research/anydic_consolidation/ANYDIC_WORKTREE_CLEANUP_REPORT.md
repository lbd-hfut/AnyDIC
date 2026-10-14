# 已验证归档与清理收据

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

任务 ANYDIC_RESEARCH_CONSOLIDATION_AND_WORKTREE_CLEANUP；2026-10-14。安全完成：初始39个注册worktree，普通git worktree remove移除37个，保留主项目及1个受保护旧worktree。没有force、rm、reset、clean、分支删除、GC、push/merge/release或生产代码变更。

## 归档结果

资产位置：`${ANYDIC_RESEARCH_ARCHIVE}`。38个额外worktree全部完成非Git资产保留；共155,601个文件/链接、199,624,108,428 bytes（199.624 GB / 185.914 GiB，logical size，包括链接文本，不去重）。同文件系统rename保留inode；活跃C16只复制。数GB完整隔离环境、所有缓存/未知资产、原始GT/图像、checkpoint、预测数组、日志、world生成记录、GPU/CPU收据及外部源码内部.git全部保存。完整tracked报告/科学源码由保留Git分支恢复，common Git目录原位保护；本轮无Git LFS依赖。

非Git数据在移动/复制前后完整读取SHA256、核对size；rename资产另核对inode。38份完整源清单包含branch/HEAD及逐文件分类，目标路径和verified字段；[manifest](ARCHIVE_MANIFEST.json)绑定清单SHA256。重复tracked内容按已实测相同Git blob复用SHA256并检查工作树无tracked变化，不把Git clean当ignored资产资格。

## 核心模型

D4 A4R_step3000、C11 step12000、C13 main_step12000、C15 Crop600/Full600皆通过归档校验。C11 `329e670f2064ccccb5ae6faa4d7b1ce853c3c153b06dfd1b7f11bff535bb7727`，C13 `152ee60356f4503143818597eb6e30d32236bf8bad47f6041435b42588a247fb`，Crop600 `58033c00c663e91c1c1dcb7e7ad9e8ba32981b59dc5f07c80b93976c3b5b6f8d`，Full600 `bfdbba89ca66870f3bdd1a6d56c10b266df28be6e29da22aaa9b6b53b855f780`。全部114模型文件及4个既有外部权威见[checkpoint索引](ANYDIC_CHECKPOINT_INDEX.md)。C16无新训练模型，其原源码/288条轨迹及C15依赖均可定位。

## 已移除worktree

| 路径 | 原分支 | 原HEAD |
| --- | --- | --- |
| ${ANYDIC_WORKTREES}/anydic-c11-matching-repair | experiment/anydic-c11-matching-repair | 0ac7d6659b84e2ef39072e45e88f06e3a38fce51 |
| ${ANYDIC_WORKTREES}/anydic-c12-cross-resolution | experiment/anydic-c12-cross-resolution | 97cecd6fd3ad7b424502cfdbc0cdc09ccdee4176 |
| ${ANYDIC_WORKTREES}/anydic-c13-scale-aware | experiment/anydic-c13-scale-aware | c9270878b1d4e463d5823da1c92c859fef7ad3e1 |
| ${ANYDIC_WORKTREES}/anydic-c14-nonrotation | experiment/anydic-c14-nonrotation-cross-scale | f2dbcfe8120b04ffcc30a32eba2675c865df715d |
| ${ANYDIC_WORKTREES}/anydic-c15-full-frame | experiment/anydic-c15-full-frame-training | c960a39379ea10d5f65825a89f4bc29e69832746 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c0 | experiment/anydic-low-v3-c0-generalization | 335284bf24a1ec252901ed6b1d662543cf05acc5 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c1 | experiment/anydic-low-v3-c1-convergence | d760af109a22010b758b91c7336d939cfe6cdad3 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c10 | experiment/anydic-low-v3-c10-support-aware | 40ab87ed1ae3478cc32d5121b84824c014616689 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c1g | experiment/anydic-low-v3-c1g-affine | 837a2cafa000f9953172693770a1ac9a2b1ab605 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c2 | experiment/anydic-low-v3-c2-final | bf6e0d29cdd870c47d65bf81696beddf0c31edcd |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c3a | experiment/anydic-low-v3-c3a-equivariant | bd8f347d7b7097fdc65697b4226b921030f0cf60 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c3d | experiment/anydic-low-v3-c3d-candidate-fate | 735acc53a962922d9ba357eb05a067b8b68819c3 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c3e | experiment/anydic-low-v3-c3e-f4-multihypothesis | 6f23a9424d3d1c7f662c1d9d5e80a86c20361225 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c4 | experiment/anydic-low-v3-c4-identifiability | c033fc1ea98e8f56c8bbec3e090e118c6bd66ffb |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c4b | experiment/anydic-low-v3-c4b-bidirectional | dad1a0616efa4d375caa030297bb3142842cbc7a |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c5 | experiment/anydic-low-v3-c5-local-refinement | 56303e977cef3e4d8b2de96d51ebdbce92ba8649 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c5r | experiment/anydic-low-v3-c5r-recheck | 5df6219f0c732cec1fab8f1279661b9fa732a242 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c6 | experiment/anydic-low-v3-c6-information-audit | 7af849d8f4e1073a82c29604d4b0010cf236ff0d |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c7 | experiment/anydic-low-v3-c7-local-feature | 08747426ee2fcfe89a16864312606e0321338f85 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c8 | experiment/anydic-low-v3-c8-pair-conditioned | d6506f3b24d86154bde45205cc8bb84de1b0b434 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c9 | experiment/anydic-low-v3-c9-real-validation | 0d802df1bdd5c3456072d43e076efa3300ac8e46 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c9b | experiment/anydic-low-v3-c9b-dic-challenge | 859d53e1b7e769f15e4ac91d397de56c4804f5ba |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c9c | experiment/anydic-low-v3-c9c-observability | 594678f2315b1b2a2a948ef624d27145c1690648 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d2 | diagnostic/low-v3-r1-failure-mechanism | 52c7981f4b754fcfd2b97a8b8cbeaaadb5200d0f |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d3 | experiment/anydic-low-v3-d3-dual-phase | ae59a4b74bb975be5d7da68c26ae24d2a6b961d3 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d4-f8net | experiment/anydic-low-v3-d4-f8net | 1b8d72fe82150b8ca1c171799ce0664e0930dcfa |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d5 | diagnostic/anydic-low-v3-d5 | f2a20057e93595e7a98243812cc817d64443cf15 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d6a-f4net | experiment/anydic-low-v3-d6a-f4net | 02ca1ab8e16d9bf432063816e2011840293d51ed |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d6b-joint | experiment/anydic-low-v3-d6b-joint | 7bef21a6b119c051f0805031dc18a3229d212497 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-f8 | experiment/anydic-low-v3-f8 | 2dee12c21d8cfcf2cde4088daeb2d613b0c8eeef |
| ${ANYDIC_WORKTREES}/anydic-low-v3-f8-r1 | experiment/anydic-low-v3-f8-r1 | e79619081a737b5d39d1dcac65c81e440b5b3ab0 |
| ${ANYDIC_WORKTREES}/anydic-low-v3-prospective | experiment/anydic-low-v3-prospective | ef942815a618ef9d5920cf92576b630cf8698171 |
| ${ANYDIC_WORKTREES}/anydic-medium-gmflow-coarse | experiment/anydic-medium-gmflow-coarse | d74511567de499f53f8b3ce83534b137c2e22603 |
| ${ANYDIC_WORKTREES}/anydic-medium-m2-gmflow-lightweight | experiment/anydic-medium-m2-gmflow-lightweight | 2f0f2c4b49faa9ccd489cebbebd2b7b821782fd3 |
| ${ANYDIC_WORKTREES}/anydic-medium-m3-continuous-e8 | experiment/anydic-medium-m3-continuous-e8 | b45668d3fe41a941be0a189e6f4e2bbe26e824ac |
| ${ANYDIC_WORKTREES}/anydic-medium-m4-routing | experiment/anydic-medium-m4-routing | 1d53d4cbd37cb8fe3defd69e2e7fc1d27e3f23b5 |
| ${ANYDIC_WORKTREES}/anydic-medium-m5-prospective | experiment/anydic-medium-m5-prospective | d4c0c6c42cc90c1f05a52b3f0ed4561b3ed4c857 |

## 保护性保留

| 目录 | 状态 | 原因/处理 |
| --- | --- | --- |
| ${ANYDIC_REPOSITORY} | MAIN_PROTECTED | 主项目、case、生产源码/权重、common .git保护 |
| ${ANYDIC_WORKTREES}/anydic-c16-native-update-stability | ACTIVE_PROTECTED | 活动shell/VS Code；只复制全部非Git资产，原目录/分支checkout保留 |

## 恢复核验

随机种子20261014从manifest定位并只读打开C11实际预测、C13原生R3预测、同root/分辨率的C15 Crop600和Full600配对结果、C16 Full600 R3迭代轨迹，共5个NPZ；SHA256、keys/数组shape与dtype核验通过。全部39个原分支完整SHA及24个最终Decision的Git原字节可恢复；10个原tag完整ref不变。主项目原有4460个文件/链接的inode/size/mtime保持，其中case文件102个；main指针仍为 `5c0ec91458ab6dbe5f485a78e453da5061099a62`。只做文件完整性与读取核验，没有重训或GPU数值复现。

环境/源码版本、venv结构/依赖/编译扩展列表见外部 `verification/ENVIRONMENT_RECOVERY.json`。外部conda/base环境保留，移动venv的shebang/activate绝对前缀可能需按清单重建；历史源码中的绝对runs依赖需显式路径适配。不得覆盖既有checkpoint或旧结果。

21个归档符号链接均保留原始文本及SHA256：12个环境目标仍存在；6个pytest绝对路径别名的原目标目录已完整归档，可由 `verification/SYMLINK_RECOVERY_MAP.json` 定位；3个浏览器锁标记在初始完整文件/目录清单中就没有对应目标文件，原样保留。没有为修复显示而覆盖原链接或修改科学数据。

## 本地提交与最终状态

科研提交：`18f618af2e74cbe2898e0008fb55f912119f287f`，message `docs(anydic): consolidate C0-C16 research and matching roadmap`。本收据与最终模型归档状态纳入第二个本地提交 `chore(anydic): record verified worktree archival and cleanup`；最终HEAD/clean收据保存于外部 `verification/FINAL_GIT_AUDIT.json`，避免文档自引用hash。只提交本目录文档及小型JSON，不提交大数据。

为了满足最终常规Git status clean，追加本机 `.git/info/exclude` 的 `/case/dic_challenge/`，没有修改tracked `.gitignore`，没有隐藏tracked修改或处理其他未提交工作。原规则和追加收据见外部 `verification/LOCAL_EXCLUDE_RECEIPT.json`；如希望重新看到原未追踪case，只删除这一条本机新增规则，数据始终原位存在。

## 后续人工动作

关闭/确认C16 shell与VS Code不再使用该目录后，可基于本manifest再次核查活动/HEAD/status和新增ignored资产，再执行普通移除；本轮不为数量目标强制处理。后续复现必须重新绑定归档路径与原环境，文件完整性并非训练/推理数值等价或新科学资格。两个外部第三方模型参数量仅安全state规模，其他112个checkpoint参数量已有原始记录。科研仍需GPU轨迹/Decoder-only/Joint-state诊断及新独立协议。
