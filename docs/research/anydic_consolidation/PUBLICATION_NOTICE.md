# 公开发布范围、修改说明与许可证

本快照来自 ANYDIC 科研汇总分支 `research/anydic-roadmap-consolidation` 的冻结提交 `126cab8a2e3c66fc4d6776981b248eb2a519ba21`。它以独立根提交发布文档，不继承原 main、科研分支或任何模型/实验二进制历史。本目录包含原 18 个 Markdown/JSON 的公开副本及本说明、许可证副本；没有原科研资产、第三方源码、模型权重、GT、图像、预测数组或实验环境。

## 修改及隐私范围

本机用户名、绝对目录与本地进程/浏览器锁身份不公开。路径符号仅表达保管角色，不能按字面直接执行：

| 符号 | 含义 |
| --- | --- |
| `${ANYDIC_REPOSITORY}` | 自行持有完整科研 Git 历史的本地仓库 |
| `${ANYDIC_RESEARCH_ARCHIVE}` | 自行持有的本地科研归档根目录 |
| `${ANYDIC_WORKTREES}` | 本地历史科研 checkout 的父目录 |
| `${LOCAL_HOME}` | 本地使用者自行设置的用户主目录 |
| `${LOCAL_BROWSER_LOCK}` / `LOOPBACK:+PID` | 原本机浏览器进程锁标记，已泛化 |

工作树 JSON 移除了进程可执行文件、cwd、PID、打开路径，以及逐项删除操作的命令输出/时间收据；保留原分支、提交、最终状态、规模与归档来源哈希。原本机 `.git/info/exclude` 内容没有重发。模型权威文档的两处完整仓库链接改为原文件位置说明，避免独立快照中的失效链接。Markdown 带显著修改说明，字典型 JSON 增加 `_publication` 元数据；数组型 JSON 的修改范围由本说明记录。

科研结果仅以原作者汇总文字、资格状态、统计指标和工件元数据/哈希表示；本发布不包含逐点实验数据或第三方模型内容。C13/C14/C15 不具所述资格，C16-A 需要进一步诊断，C16-B 未启动；C11 仅有界合成资格，GMFlow+RAFT 仍是未来方案。

## 历史证据与恢复边界

原文中 PASS、verified、SHA256、清理数量与环境描述均是冻结源材料的历史声明。经脱敏后的 `target` 和路径文本不同于原始材料；保留的 `link_text_sha256`、manifest SHA256、source-file SHA256 绑定原始材料，不能用于直接哈希脱敏字符串。JSON 不作为本次 199.624 GB 文件内容重新核验的收据。本次没有科研训练或数值复现。

历史 Git SHA、blob ID 和 SHA256 在本快照里只是普通文本；Git 可达性由本根提交的 tree 决定。原代码、Decision、环境、manifest、checkpoint、GT 与 runs 的恢复依赖本地保留的完整历史及私有资产，公开分支不提供这些对象，也没有替它们承诺下载链接。恢复示例只能在该完整本地仓库执行，不能在本独立快照直接恢复历史。

## 许可证与第三方边界

沿用原项目随源提交提供的 Apache-2.0 许可证；完整文本见 [LICENSE](LICENSE.md)，其内容与原提交的根 LICENSE 完全相同。原声明与署名保留，以上公开副本的修改范围已标明。源提交没有根 NOTICE 文件。

SEA-RAFT、GMFlow、WAFT、Depth Anything 等仅作为科研对象名称、版本、参数规模、文件名及哈希引用；本快照没有复制其源码、权重、样本或许可证文件，不声称替第三方资产授予再分发权。后续单独发布这些资产需单独核验其许可和数据授权。此前用户已授权对这组科研汇总 Markdown/JSON 准备公开副本；本次没有执行 push。

## 源文件与公开副本指纹

以下源指纹绑定冻结本地源文件，公开指纹绑定本次脱敏文件；原文件没有被修改。

| 文件 | 原文件 SHA256 | 公开副本 SHA256 |
| --- | --- | --- |
| `ANYDIC_ARTIFACT_RECOVERY_GUIDE.md` | `1326d8c57369b4452924a8f3dc7fd53e3a935a5fd6656b88a6539a7f5085ad88` | `7472a18cbcf2b12084434f3ff51303b4103b80cdc445c3415c9e724f948b209e` |
| `ANYDIC_BRANCH_AND_COMMIT_INDEX.md` | `eb186d54c2f26872f69eaa6b753ce07582896acf6b17e8f9eac185cb8f086e65` | `6b37b63132b12d11903b8fa4c10461948527935ab153afacc5d5d2b2843601ce` |
| `ANYDIC_CHECKPOINT_INDEX.md` | `94e6901d212a9cb2253e5f17e0b868a17f5ecb4f9956a8f73c00e82f1c530e8d` | `c5e649c67b8fe51359d698976422bb865c5e45ef3151b153775a9a1e3be2eec1` |
| `ANYDIC_GMFLOW_RAFT_ROADMAP.md` | `6a33d8f0ffef8547e91c66493b1c5ce8d526bea62679e62f8cc217ba341eddd4` | `ab9e08bce1b984ee4c7de9da19cff45a600aa882ff419c75b4e09daecfc4c617` |
| `ANYDIC_MATCHING_FAILURE_LESSONS.md` | `17474f86efe02f2fa7a856e725d3976f8a94c4173b690e8fc10763284e61817a` | `ea3d252c4e389cfd060d14d96ccea3fe36a0b287be03905a4b6ca48fe9e54bf8` |
| `ANYDIC_MODEL_AUTHORITY.md` | `8c46a11e2424465af90b369c086e17c11c579af3a979e468f55bd49bffff925d` | `e8e095a88f95b73aa305921aa74b6bf608565bbc3cc0e04d9ce1fe830d6db670` |
| `ANYDIC_RESEARCH_HISTORY_C0_C16.md` | `c936a33604837189ed9add42ce13f50c7afa97947c3946073c67a2d60ec630d3` | `8a95239c180dde388d48502563141393fed59fd5a47089825549e0081571e0c7` |
| `ANYDIC_RESEARCH_ROADMAP.md` | `0d26ed9fd0b698dcdec9b3d4d8de7db7e340bc4447ccc97d765f2826769d0f88` | `f565bf9f8c8881ecdde56855fe07f5b72f61d3ff5f05b32ed02960f617b59438` |
| `ANYDIC_SCIENTIFIC_STATUS_MATRIX.md` | `dc2a1025ed9bb902e39ab2aed7d3969e8872141d6c131f05b36dc45b3feaf189` | `20a3b683487323357b9e511aa78ec5a1f8d94fd9dacc15a53c2d26d522ef9613` |
| `ANYDIC_WORKTREE_CLEANUP_REPORT.md` | `c28f7b2b38e61778fa9478d7528dc9b17f50968f77f53d25b994beea7d13e30c` | `210762f4f5e022658c0667b38eac01c924f381ab6cda4e7f2a37f7ba0e20183f` |
| `ANYDIC_WORKTREE_INVENTORY.md` | `14f5cf92613228df22a50718e279674c228dbe2aceda69a354ccc56bc035ad74` | `e724e7353017a4c7960ee4132bc862526ce6940d1c9932f9eeb9e6db86105367` |
| `ARCHIVE_MANIFEST.json` | `8c5020d000a5455c0c7d739931a7563dfafd99e492f85965bdd4c58e78038bd8` | `c6c1d5df89b667f65ccdb9b48687630926f5e8c7faeed7faa1fcb7b9a90b8bd4` |
| `BRANCH_RECOVERY_INDEX.json` | `1305981c0faa57f2c474dace18367fcfa3a81c70854f79f61636fa38f0ab8242` | `8ce8faa96c59c917d18e8bcbb9511f6df5906e82fcdc97bcd3e6d61a2a76e53f` |
| `CHECKPOINT_INVENTORY.json` | `c6a3ae1f042486cf9518b259f6f5312936faf0f0850dc6f9668dc3abc2595d61` | `2fbf2dd7d975f2f32a0870507c84d79f9736aed9ee472f97f956efe4870483ea` |
| `CONSOLIDATION_VALIDATION.json` | `6cce06c0a170e8bfc5def177853d8094ac208a437d6ffead8b6ba77aa5484d4e` | `92209a28c85c8d1e9937714ba0cec112cbdb5f5313d00d6726d63ee81f673805` |
| `README.md` | `ceb35197db2dc709baeb11577148d1e8bb256c158944673721491ba3f94d632e` | `73a13c7daa40127b2ad0585403f4a5109b9e43fa9d40cc488ab70ba20e51aa99` |
| `RESEARCH_SOURCE_INDEX.json` | `ae9821d087e694f67b2600d13548b1af973fa496d0461214ba71b57a4f70645c` | `ccdc726ed613919ddaa9bee26e10199eb50634508b43bc534e712915261afd41` |
| `WORKTREE_INVENTORY.json` | `30b52688ed43625cb517e3b36ff5c6d4f4d674cad0897237184dc1abfcbe30e5` | `641e51ca0b046c288d2179b91c16a4bf8af9625260e310230b1b38d1566b8d4c` |

许可证副本 SHA256：`c71d239df91726fc519c6eb72d318ec65820627232b2f796219e87dcf35d0ab4`。
