# ANYDIC C0–C16 科研历史

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

原始分支 HEAD、最终 Decision 和机器 manifest 为权威。此次仅整理证据，未执行训练或新科学评价。旧报告中路径是来源路径，恢复以本目录 manifest 为准。

台账没有发现独立 C3B/C3C 本地分支。C3A 的 C3B 状态为 NO-GO，未进入完整场资格阶段；不能根据阶段编号补造不存在的已执行实验。C5R 的 resume Decision 是该分支最终状态，早期工程不确定 Decision 仍保留在原始分支中。

## D4 的位置

GMFlow K6 粗尺度 → F8 Top4 → F4 9×9 hard winner → F1 33×33、0.25px refinement → Final Selector。D4_DIRECT 使用 A4R_step3000；其 C2 有界资格与 D4 分支的 F8Net 开发负结果是不同结论，不得混同。生产 LOW 仍是 V2.0 Final。

## C0

- 主要假设：D4 的合成泛化是否优于 V2/R1。
- 实际实现：冻结模型，连续物理 world 与 Query/原生及标准化尺度对照。
- 执行：120 合成 world 推理；0 训练。
- 最终状态：`LOW_V3_C0_GENERALIZATION_PARTIALLY_SUPPORTED`。
- 核心结果：部分维度支持；推荐 D4_DIRECT。
- 失败原因与证据限制：纹理 OOD、原生收敛和复杂场不全面支持；无真实资格。
- 实际贡献：建立独立 world、物理单位与 Query 一致性评价。
- 原分支：`experiment/anydic-low-v3-c0-generalization`；HEAD：`335284bf24a1ec252901ed6b1d662543cf05acc5`。
- 原始 Decision：`docs/results/low_v3_c0/C0_GENERALIZATION_FINAL_DECISION.json`，SHA256 `c5664d869ae42153f67754578ff4e70ecfa8b4bbccc8b45bebe6895bcf84562c`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c0/runs/low_v3_c0` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c0`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C1

- 主要假设：形变敏感特征适配能否恢复匹配。
- 实际实现：Route A 68,693 参数 adapter，B1/B2 对照。
- 执行：各 12,000 GPU 更新；选择 step9000。
- 最终状态：`LOW_V3_C1_DEVELOPMENT_NOT_SUPPORTED`。
- 核心结果：特征形变失配获支持，开发修复未获支持。
- 失败原因与证据限制：大位移、高梯度、标准化非回归、star-like Gate 失败。
- 实际贡献：区分特征机制与完整场资格，保留实际训练负结果。
- 原分支：`experiment/anydic-low-v3-c1-convergence`；HEAD：`d760af109a22010b758b91c7336d939cfe6cdad3`。
- 原始 Decision：`docs/results/low_v3_c1/C1_FINAL_DECISION.json`，SHA256 `7ec8c68eaebc15070960531ea53091d09c1f200c1f8b01992c082be420681213`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c1/runs/low_v3_c1` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c1`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C1G

- 主要假设：局部仿射补偿能否解除复杂变形失配。
- 实际实现：固定与 oracle 几何补偿上界。
- 执行：推理诊断；0 训练；B2/B3/B4 和 LOCKED 未运行。
- 最终状态：`C1G_AFFINE_COMPENSATION_UPPER_BOUND_INSUFFICIENT`。
- 核心结果：G1 恢复 0 复杂 root；O2 恢复 8。
- 失败原因与证据限制：即使有 GT 上界也不足；不能部署 oracle。
- 实际贡献：转向冻结 D4 的独立 C2 资格。
- 原分支：`experiment/anydic-low-v3-c1g-affine`；HEAD：`837a2cafa000f9953172693770a1ac9a2b1ab605`。
- 原始 Decision：`docs/results/low_v3_c1g/C1G_FINAL_DECISION.json`，SHA256 `609049dc196056af192b066966c54cf3a2c0e47607983968ef01349a8855c430`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c1g/runs/low_v3_c1g` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c1g`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C2

- 主要假设：未变 D4 是否取得有界合成资格。
- 实际实现：一次预测封存后 GT 解封，240 独立物理 world。
- 执行：执行推理和独立核验；0 训练。
- 最终状态：`LOW_V3_C2_BOUNDED_SYNTHETIC_QUALIFIED`。
- 核心结果：IID192 24 roots 中 21 通过；Query 支持通过；有界资格。
- 失败原因与证据限制：Wilson 下界约 68.996%，不能证明普遍成功率≥80%；跨原生尺度、复杂场、真实实验未全面资格。
- 实际贡献：冻结 LOW_V3_D4_DIRECT 与资格边界，不改生产。
- 原分支：`experiment/anydic-low-v3-c2-final`；HEAD：`bf6e0d29cdd870c47d65bf81696beddf0c31edcd`。
- 原始 Decision：`docs/results/low_v3_c2/C2_FINAL_DECISION.json`，SHA256 `35f14e5308c4e48dc9c4ca693786d6fd8244a67d2ff981c4a79c82e03d6bf9b0`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c2/runs/low_v3_c2` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c2`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C3A

- 主要假设：几何等变特征能否迁移到 DIC。
- 实际实现：受约束 E8 几何矩阵/0–1 阶仿射与 SIFT 对照。
- 执行：24 校准 roots，48 选择 roots；拟合和推理执行，未进入全场 B2/LOCKED。
- 最终状态：`C3A_ENGINEERING_INCONCLUSIVE`。
- 核心结果：rotation 子群候选召回改善；复杂 Top4 +0.821pp、Top1 −3.740pp。
- 失败原因与证据限制：整体判别失败，严格 Query bitwise 失败；5 纹理条件不构成 240 独立 roots。
- 实际贡献：相似度改善不能替代候选辨别和场级改善。
- 原分支：`experiment/anydic-low-v3-c3a-equivariant`；HEAD：`bd8f347d7b7097fdc65697b4226b921030f0cf60`。
- 原始 Decision：`docs/results/low_v3_c3a/C3A_DELIVERY_MANIFEST.json`，SHA256 `899e6ce98d6924daf7fc89a3c37e52f17ba90bc4c5fedd86c0462511759011bd`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c3a/runs/low_v3_c3a` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c3a`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C3D

- 主要假设：D4 候选在哪一级丢失。
- 实际实现：F8/F4/F1 候选命运追踪与受控 GT oracle。
- 执行：0 训练；实际阶段推理和 12-root 单独受控人口。
- 最终状态：`C3D_STAGE_FAILURE_MECHANISM_ATTRIBUTED`。
- 核心结果：主要 F4_SELECTION_LOSS，次要 F1_LOCALIZATION_LOSS。
- 失败原因与证据限制：暴露开发人口；bitwise 失败但容差/候选身份/selector 决策一致；oracle 仅上界。
- 实际贡献：提出形变鲁棒 F4 refinement 研究并量化支持丢失。
- 原分支：`experiment/anydic-low-v3-c3d-candidate-fate`；HEAD：`735acc53a962922d9ba357eb05a067b8b68819c3`。
- 原始 Decision：`docs/results/low_v3_c3d/C3D_FINAL_DECISION.json`，SHA256 `be649ce26d5d48eb7f048b58180a1f0b2f612b24ad66fc798bcbe1457b413dbf`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c3d/runs/low_v3_c3d` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c3d`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C3E

- 主要假设：保留多个 F4 假设是否修复完整场。
- 实际实现：冻结网络、额外 F4 假设、无 GT 输出决策。
- 执行：推理执行；0 训练；Gate2 停止，LOCKED 未运行。
- 最终状态：`LOW_V3_C3E_MULTI_HYPOTHESIS_NOT_SUPPORTED`。
- 核心结果：有限单点改善；场趋势和 coherent 可靠性不改善。
- 失败原因与证据限制：GT-free 部署规则不合格，仅暴露开发数据。
- 实际贡献：多候选覆盖收益需要合法可部署的判别器。
- 原分支：`experiment/anydic-low-v3-c3e-f4-multihypothesis`；HEAD：`6f23a9424d3d1c7f662c1d9d5e80a86c20361225`。
- 原始 Decision：`docs/results/low_v3_c3e/C3E_FINAL_DECISION.json`，SHA256 `1a3d1815f8ff402a62754e6f10f7a1b1608ae275c27b384b50b76fc6b541f9f8`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c3e/runs/low_v3_c3e` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c3e`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C4

- 主要假设：候选分数/光度/反向证据能否判别。
- 实际实现：完整反向匹配、锚点和候选证据审计。
- 执行：实际诊断推理；0 训练；新校准/新 LOCKED 未运行。
- 最终状态：`C4_FEATURE_IDENTIFIABLE_FIELD_UNPROVEN`。
- 核心结果：存在独立候选信息；固定规则只有有限单点/趋势改善。
- 失败原因与证据限制：成片错误未可靠减少；完整反向与锚点成本不满足部署。
- 实际贡献：将研究问题收敛到可复用的低成本双向证据。
- 原分支：`experiment/anydic-low-v3-c4-identifiability`；HEAD：`c033fc1ea98e8f56c8bbec3e090e118c6bd66ffb`。
- 原始 Decision：`docs/results/low_v3_c4/C4_FINAL_DECISION.json`，SHA256 `5da193c76d60a7e8ae0cc4753500fbd142878398ed58c1d7e19a976e34f65c7e`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c4/runs/low_v3_c4` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c4`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C4B

- 主要假设：低成本双向候选证据是否足够。
- 实际实现：图像级反向上下文复用、E8→E4 选择端点。
- 执行：推理执行；0 训练；Gate1 失败。
- 最终状态：`C4B_LOW_COST_BIDIRECTIONAL_EVIDENCE_INSUFFICIENT`。
- 核心结果：部分信息保留；趋势/coherent roots 无改善。
- 失败原因与证据限制：冻结信息充分性门槛未过；未启动独立新人口。
- 实际贡献：成本可行不代表证据充分，停止当前集成。
- 原分支：`experiment/anydic-low-v3-c4b-bidirectional`；HEAD：`dad1a0616efa4d375caa030297bb3142842cbc7a`。
- 原始 Decision：`docs/results/low_v3_c4b/C4B_FINAL_DECISION.json`，SHA256 `b0e9eb6ac597490f84f9ea6b8e1693de6506fe475ab62a730c973b5201af720a`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c4b/runs/low_v3_c4b` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c4b`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C5

- 主要假设：局部学习 Refiner 可否生成正确新位置。
- 实际实现：形变感知局部 learned refinement。
- 执行：100 GPU smoke 更新；正式训练 0；2000-step Gate 未运行。
- 最终状态：`LOW_V3_C5_ENGINEERING_INCONCLUSIVE`。
- 核心结果：梯度 smoke 通过，完整端点预算未通过。
- 失败原因与证据限制：共享硬件下工程不确定；5 roots/6400 Query smoke 不构成正式资格。
- 实际贡献：必须先验证完整端点与学习门槛。
- 原分支：`experiment/anydic-low-v3-c5-local-refinement`；HEAD：`56303e977cef3e4d8b2de96d51ebdbce92ba8649`。
- 原始 Decision：`docs/results/low_v3_c5/C5_FINAL_DECISION.json`，SHA256 `bb3158f0cf1fe5e82e6fbda20af15f3823781d5a1321735718ecae63b91f5285`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c5/runs/low_v3_c5` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c5`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C5R

- 主要假设：C5 资源及微型学习是否可复核。
- 实际实现：同一 Refiner 有界复核；保持早期与 resume 两份 Decision。
- 执行：早期 0 optimizer；resume A=600，B=0，正式=0。
- 最终状态：`C5R_MICRO_LEARNABILITY_NOT_SUPPORTED`。
- 核心结果：最终 C5R_MICRO_LEARNABILITY_NOT_SUPPORTED。
- 失败原因与证据限制：补充 backend parity 失败；不是所有 Refiner 不可能的证明；无独立人工审查。
- 实际贡献：停止此 Refiner 的正式训练投入。
- 原分支：`experiment/anydic-low-v3-c5r-recheck`；HEAD：`5df6219f0c732cec1fab8f1279661b9fa732a242`。
- 原始 Decision：`docs/results/low_v3_c5r/C5R_RESUME_FINAL_DECISION.json`，SHA256 `1c8f1966f0243aef307dd01785d85d64cb64673ffc0ccebfa6a41d537dfe6d0c`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c5r/runs/low_v3_c5r` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c5r`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C6

- 主要假设：局部失败是否来自支持/表示信息损失。
- 实际实现：E4 连续信息、合法 F4 中心、冻结 F1/原图对照。
- 执行：48 新独立 roots/96 条件机制推理；0 训练。
- 最终状态：`C6_LOCAL_INFORMATION_MECHANISM_CONFIRMED`。
- 核心结果：F4 离散支持丢失与 E1 辨别不足并存；大旋转有 F8 覆盖丢失。
- 失败原因与证据限制：不能宣称所有图像信息消失或未见生成器资格；判别解释为分析后规则。
- 实际贡献：形变感知 E1 描述子优先，保留 E4 连续证据。
- 原分支：`experiment/anydic-low-v3-c6-information-audit`；HEAD：`7af849d8f4e1073a82c29604d4b0010cf236ff0d`。
- 原始 Decision：`docs/results/low_v3_c6/C6_FINAL_DECISION.json`，SHA256 `6dbc1ced8323bc08b640dc3cbfb40a8f0c50548ba982eb9383e59570aa0040b0`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c6/runs/low_v3_c6` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c6`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C7

- 主要假设：小型局部特征可否学到所需辨别。
- 实际实现：5920 参数局部表示。
- 执行：800 micro 更新；8 TRAIN roots，同 root heldout Query；正式训练 0。
- 最终状态：`C7_LOCAL_FEATURE_LEARNABILITY_NOT_ESTABLISHED`。
- 核心结果：局部特征可学习性未建立。
- 失败原因与证据限制：单一结构/有限训练，不是理论不可能；SELECTION/LOCKED 未生成。
- 实际贡献：保留局部表示负结果，停止该架构续训。
- 原分支：`experiment/anydic-low-v3-c7-local-feature`；HEAD：`08747426ee2fcfe89a16864312606e0321338f85`。
- 原始 Decision：`docs/results/low_v3_c7/C7_FINAL_DECISION.json`，SHA256 `47621d3f45e45769052fc3aea3a1d0a7f2714241991d586ee182ee1774e38620`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c7/runs/low_v3_c7` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c7`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C8

- 主要假设：成对局部匹配能否兼顾证据与预算。
- 实际实现：1383 参数 pair-conditioned matcher。
- 执行：3 工程 smoke 更新后丢弃；micro/正式训练 0。
- 最终状态：`C8_RUNTIME_NOT_SUPPORTED`。
- 核心结果：Gate0 runtime 未支持。
- 失败原因与证据限制：单一工程图像对及 3 历史 GT-free replay；没有科学 learnability 否定。
- 实际贡献：匹配证据必须在完整端点预算内实现。
- 原分支：`experiment/anydic-low-v3-c8-pair-conditioned`；HEAD：`d6506f3b24d86154bde45205cc8bb84de1b0b434`。
- 原始 Decision：`docs/results/low_v3_c8/C8_FINAL_DECISION.json`，SHA256 `f01ac9485c9aeb0a9e2bae9ce5c1e883301ed722b10a3c9f5337c37c2f837dc1`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c8/runs/low_v3_c8` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c8`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C9

- 主要假设：冻结 D4 可否做真实实验资格。
- 实际实现：真实输入/独立 2D GT 与采集协议准备。
- 执行：真实序列/Query=0；0 训练；Gate0 停止。
- 最终状态：`C9_REAL_DATA_NOT_AVAILABLE`。
- 核心结果：C9_REAL_DATA_NOT_AVAILABLE。
- 失败原因与证据限制：独立真实测量数据不可用；绝对精度未验证。
- 实际贡献：制定真实采集协议并保留合成/真实区别。
- 原分支：`experiment/anydic-low-v3-c9-real-validation`；HEAD：`0d802df1bdd5c3456072d43e076efa3300ac8e46`。
- 原始 Decision：`docs/results/low_v3_c9/C9_FINAL_DECISION.json`，SHA256 `466e81cb7dac0b35ef4e610d6f31ff3c2ffe32747bad75b02b7397517d81672e`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c9/runs/low_v3_c9` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c9`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C9B

- 主要假设：真实 DIC Challenge 图像呈现哪些匹配现象。
- 实际实现：冻结 D4 的 native 12/13/16；17 原生 OOM 后 native-pitch crop。
- 执行：281 GPU 成功/282 尝试；227 科研端点；0 训练。
- 最终状态：`C9B_REAL_IMAGE_DESCRIPTIVE_EVALUATION_COMPLETE`。
- 核心结果：真实图像描述性评价完成。
- 失败原因与证据限制：无独立逐点 2D GT；16 坐标映射未核实；17 仅 crop；自洽不等于绝对准确。
- 实际贡献：识别闭合长尾、可观测支持与真实数据资源限制。
- 原分支：`experiment/anydic-low-v3-c9b-dic-challenge`；HEAD：`859d53e1b7e769f15e4ac91d397de56c4804f5ba`。
- 原始 Decision：`docs/results/low_v3_c9b/C9B_FINAL_DECISION.json`，SHA256 `8047d7059233d7cc900468a5aa0235cf2de44e031ad45f5a1f759689e76bfc6c`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c9b/runs/low_v3_c9b` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c9b`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C9C

- 主要假设：图像可观测性信号是否可预测风险。
- 实际实现：图像-only support/visibility seal、offline abstention、反向/时序审计。
- 执行：12 新 GPU 端点/14715 Query；0 训练。
- 最终状态：`{"risk_associations": "C9C_REAL_OBSERVABILITY_RISK_ASSOCIATIONS_SUPPORTED", "offline_support_rule": "C9C_SELECTIVE_ABSTENTION_DEVELOPMENT_SUPPORTED", "final_frame_annotation": "C9C_VISIBILITY_ANNOTATION_INCONCLUSIVE", "calibrated_reliability": "C9C_RELIABILITY_EVIDENCE_INSUFFICIENT"}`。
- 核心结果：风险关联与有界离线拒绝支持；visibility 标注不确定；校准可靠性不足。
- 失败原因与证据限制：自动未经专家审核；B1 范围；Sample16 reference pending；无独立 GT。
- 实际贡献：需要盲专家标注和真实参考校准，不能把 confidence 当正确概率。
- 原分支：`experiment/anydic-low-v3-c9c-observability`；HEAD：`594678f2315b1b2a2a948ef624d27145c1690648`。
- 原始 Decision：`docs/results/low_v3_c9c/C9C_FINAL_DECISION.json`，SHA256 `f30e830917e3aa01a5ee174a710be87216f08b04f9289936e450b2b432dc0534`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c9c/runs/low_v3_c9c` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c9c`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C10

- 主要假设：支持感知联合匹配能否恢复完整对应。
- 实际实现：4825 参数 support-aware 学习模块。
- 执行：24 roots：16 TRAIN/8 CHECK，1000 micro 更新；正式=0。
- 最终状态：`C10_COHERENT_MATCHING_NOT_SUPPORTED`。
- 核心结果：F4 support +3.1831pp，F1Rank@4 +1.3164pp。
- 失败原因与证据限制：均未达冻结 5pp 门槛；Gate1 失败；SELECTION/LOCKED 未生成。
- 实际贡献：局部信息增益不足以支持整场匹配修复。
- 原分支：`experiment/anydic-low-v3-c10-support-aware`；HEAD：`40ab87ed1ae3478cc32d5121b84824c014616689`。
- 原始 Decision：`docs/results/low_v3_c10/C10_FINAL_DECISION.json`，SHA256 `f149f26cf1615976b06c8e7bd9e45c2fbd98a61e8f04103b85ea1ebe8397f1e1`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-low-v3-c10/runs/low_v3_c10` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/low_v3_c10`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C11

- 主要假设：完整 SEA-RAFT 匹配能否真实修复 DIC 对应。
- 实际实现：官方 SEA-RAFT M 全 recurrent matcher，连续 GT 专项训练，任意 Query 读出。
- 执行：320 独立 TRAIN worlds，12,000 更新；独立 LOCKED 96G+128H。
- 最终状态：`C11_NATIVE_SYNTHETIC_MATCHING_REPAIR_CONFIRMED`。
- 核心结果：192×256 匹配恢复确认；LOCKED-H 恢复 90 coherent roots、48140 个 >20px 对应。
- 失败原因与证据限制：H 仍 1 coherent root/517 个 >20px，新增 19 个 >20px；上游暴露未知；无广泛分辨率/真实资格。
- 实际贡献：目前独立合成 GT 支持的主要新匹配候选；未自动替换冻结 D4。
- 原分支：`experiment/anydic-c11-matching-repair`；HEAD：`0ac7d6659b84e2ef39072e45e88f06e3a38fce51`。
- 原始 Decision：`docs/results/anydic_c11/C11_FINAL_DECISION.json`，SHA256 `19bd366f6fb0f11bd5bf824b3aec913d6d6146155f197278fb3b21387b07a48c`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-c11-matching-repair/runs/anydic_c11` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/anydic_c11`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C12

- 主要假设：C11 的跨分辨率和成像鲁棒性是否支持。
- 实际实现：连续物理 world，R1/R2/R3、旋转/周期场、OOD纹理、PSF/照明/噪声及梯度。
- 执行：冻结 C11 推理；224 LOCKED 条件；0 权重更新。
- 最终状态：`C12_ROBUSTNESS_NOT_SUPPORTED`。
- 核心结果：C12_ROBUSTNESS_NOT_SUPPORTED；R1 LOCKED 梯度热点有局部支持。
- 失败原因与证据限制：高像素位移/大旋转/Sinusoidal/Star-like 及 R2/R3 失败；纹理非完整因子矩阵。
- 实际贡献：拆开原生分辨率、物理单位精度和域泛化。
- 原分支：`experiment/anydic-c12-cross-resolution`；HEAD：`97cecd6fd3ad7b424502cfdbc0cdc09ccdee4176`。
- 原始 Decision：`docs/results/anydic_c12/C12_FINAL_DECISION.json`，SHA256 `30e3948f009aa8d64aef12e7caa7c8cb71eee3f6de36841156d953f1605c5885`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-c12-cross-resolution/runs/anydic_c12` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/anydic_c12`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C13

- 主要假设：原 SEA-RAFT 多尺度训练能否修复尺度退化。
- 实际实现：Route A 原网络、新参数 0；BF16 多分辨率训练；R3 原生 crop。
- 执行：500 micro 后丢弃；从 C11 重启正式 12000 更新；112 DEV roots。
- 最终状态：`C13_SCALE_AWARE_MATCHING_REPAIR_NOT_SUPPORTED_DEV_GATE_FAILED`。
- 核心结果：R3-G mean 1.447749→0.035808mm/coherent 5→0；R3-H 8.104436→6.848131mm/34→19。
- 失败原因与证据限制：压力原正确保护不足；R3 rotation 16→16 coherent、误差变差；DEV Gate 失败，LOCKED 未生成/运行。
- 实际贡献：像素幅度×物理特征采样交互、原生更新不稳定均需解决。
- 原分支：`experiment/anydic-c13-scale-aware`；HEAD：`c9270878b1d4e463d5823da1c92c859fef7ad3e1`。
- 原始 Decision：`docs/results/anydic_c13/C13_FINAL_DECISION.json`，SHA256 `e5e4b7556ec346ee2b5dcf0411cbb250f6311fef6c26b2c16697bec4c1264719`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-c13-scale-aware/runs/anydic_c13` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/anydic_c13`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C14

- 主要假设：排除大旋转后能否获得非旋转资格。
- 实际实现：排除 40–60° 极端刚体旋转，限定 Route B crop 专项训练。
- 执行：1000 实际更新后预注册早停；新 SELECTION 执行，LOCKED 未运行。
- 最终状态：`C14_NONROTATION_QUALIFICATION_NOT_SUPPORTED`。
- 核心结果：冻结 C13 在暴露 DEV R1/R2 常规成片匹配改善；R3 周期仍有 3 coherent 残余。
- 失败原因与证据限制：原正确保留不足；训练候选新增事件/周期 Gate 失败；后验 full R3 backward 可行不改写先前协议。
- 实际贡献：限定范围仍需要保护门槛；crop 负结果不否定全部 full-frame 训练。
- 原分支：`experiment/anydic-c14-nonrotation-cross-scale`；HEAD：`f2dbcfe8120b04ffcc30a32eba2675c865df715d`。
- 原始 Decision：`docs/results/anydic_c14/C14_FINAL_DECISION.json`，SHA256 `170ef08f751e40a617c821226dfa86247f13826543bd2676d68f4c109384b225`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-c14-nonrotation/runs/anydic_c14` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/anydic_c14`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C15

- 主要假设：完整图训练能否解除 crop 支持损失及周期失败。
- 实际实现：同协议配对 Crop600/Full600，真实完整图 backward/optimizer，near-GT 更新诊断。
- 执行：CROP/FULL 各600 GPU 更新；丢弃 smoke=3；LOCKED_GT_reads=0。
- 最终状态：`C15_FULL_FRAME_TRAINING_NOT_SUPPORTED`。
- 核心结果：16 周期R3 roots：mean 0.191353→0.083556mm，ratio 0.436658（95%CI 0.264697–0.953107），>20px 371→198。
- 失败原因与证据限制：Full 原正确 native 保留98.1654%：351 correct→wrong；Gate3 失败；crop 支持损失确认但非周期失败充分因果。
- 实际贡献：确认 C15_NATIVE_UPDATE_INSTABILITY_CONFIRMED；先诊断保护/更新再扩大训练。
- 原分支：`experiment/anydic-c15-full-frame-training`；HEAD：`c960a39379ea10d5f65825a89f4bc29e69832746`。
- 原始 Decision：`docs/results/anydic_c15/C15_FINAL_DECISION.json`，SHA256 `93dc51aa2183715a494bf68cede2aafb5f041e0a8874659d6e8edf928d2c9d8e`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-c15-full-frame/runs/anydic_c15` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/anydic_c15`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。

## C16

- 主要假设：原生迭代伤害/恢复可否被 GT-free 控制区分。
- 实际实现：实际 ConvNeXt 更新块；latent flow、hidden、相关查找及 convex upsampling 轨迹/干预诊断。
- 执行：32 暴露 C15 MICRO_DEV roots/288 轨迹；CPU 重建及 GPU 冻结终点复核；0 训练；C16-B未启动。
- 最终状态：`C16_A_MORE_DIAGNOSIS_REQUIRED`。
- 核心结果：正确→错误与错误→正确并存；现有简单退出/逐点输出/uncertainty 规则无合格联合结果。
- 失败原因与证据限制：CPU/GPU 中间轨迹 max差1.7869568px、429分类差异；periodic R3 dense oracle 保留98.522%<99%；不是新独立资格。
- 实际贡献：优先原 GPU 轨迹复核、Decoder-only 控制与 flow/hidden/upsampling 联合状态干预。
- 原分支：`experiment/anydic-c16-native-update-stability`；HEAD：`caba509f21de6f698c01e8ef685851c0b2dca887`。
- 原始 Decision：`docs/results/anydic_c16/C16_A_RESULTS_SUMMARY.json`，SHA256 `f82c9749cef4e5d1c1458609314717966daf43989eb7cc8a7b208bc39a0132e1`。
- 模型/原始结果：`${ANYDIC_WORKTREES}/anydic-c16-native-update-stability/runs/anydic_c16` → 归档中同 worktree 相对路径；checkpoint 见 [索引](ANYDIC_CHECKPOINT_INDEX.md)。
- 报告目录：`docs/research/anydic_c16`；完整精确 Markdown/PDF 列表及 Git blob 在 [来源索引](RESEARCH_SOURCE_INDEX.json)。
