# ANYDIC 科研收敛入口

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

本目录用于新的 Codex 会话从主项目继续研究，任务 ANYDIC_RESEARCH_CONSOLIDATION_AND_WORKTREE_CLEANUP，2026-10-14。

目标是任意不规则有效 Query 的真实 DIC 对应恢复，同时保护原正确点、复杂非均匀场与跨尺度物理位移/梯度。正式生产模型仍是 **AnyDIC V2.0 Final / LOW**，没有合并旧实验代码。

冻结研究基线 **LOW_V3_D4_DIRECT** 保留 **LOW_V3_C2_BOUNDED_SYNTHETIC_QUALIFIED**。**C11 SEA-RAFT M step12000** 是独立192×256连续合成GT确认匹配恢复的主要新候选；并无全面跨尺度、真实实验或下一代默认资格。C13/C14/C15资格失败；C16-A需要进一步诊断，C16-B未正式启动。GMFlow+SEA-RAFT是未来方案，尚未完成联合求解器。

已经解决的是有界独立合成对应恢复及若干局部信息/更新机制归因；尚未解决的是R3稳定性、周期场、原正确点保护、完整物理尺度一致性与广泛成像/真实计量泛化。C3A/C5早期工程不确定、C5R/C7微型负结果、C8 runtime停止与真实图像描述性分析不能混成普遍失败。停止实验的原结论永久保留。

优先读取：

- [历史 C0–C16](ANYDIC_RESEARCH_HISTORY_C0_C16.md)、[科学状态矩阵](ANYDIC_SCIENTIFIC_STATUS_MATRIX.md)、[模型权威](ANYDIC_MODEL_AUTHORITY.md)。
- [总路线](ANYDIC_RESEARCH_ROADMAP.md)、[失效教训](ANYDIC_MATCHING_FAILURE_LESSONS.md)、[GMFlow+RAFT未来方案](ANYDIC_GMFLOW_RAFT_ROADMAP.md)。
- [checkpoint索引](ANYDIC_CHECKPOINT_INDEX.md)、[原分支/commit索引](ANYDIC_BRANCH_AND_COMMIT_INDEX.md)、[恢复指南](ANYDIC_ARTIFACT_RECOVERY_GUIDE.md)。
- [worktree台账](ANYDIC_WORKTREE_INVENTORY.md)、[清理收据](ANYDIC_WORKTREE_CLEANUP_REPORT.md)、[资产manifest](ARCHIVE_MANIFEST.json)。

下一步先核查原GPU轨迹与Decoder-only/Joint-state机制，基于冻结证据注册新的独立协议。不要重新把旧暴露集当新资格集，也不要把C11/C16描述成已实现GMFlow+RAFT。

外部研究资产归档在 `${ANYDIC_RESEARCH_ARCHIVE}/`。Git分支恢复tracked源码/报告，checkpoint、GT和runs必须按manifest从归档恢复。受保护worktree以最终清理报告为准；不能仅因Git clean删除ignored数据。

本分支是无父提交的独立文档快照，不提供原科研源码、模型、GT、runs 或完整归档。索引中的 Git SHA 与 SHA256 是文本出处标识，不表示历史对象随本快照分发。原科研结论和归档验证是 2026-10-14 冻结源记录，本次发布准备没有重跑实验或重新授予资格。

路径符号、精简范围与许可证见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md) 和 [LICENSE](LICENSE.md)。恢复指南中的命令只能在拥有原完整历史和资产的独立本地科研仓库中使用。
