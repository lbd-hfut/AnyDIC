# 科研资格矩阵

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

| 阶段 | 原始最终状态 | 执行/人口 | 资格限制 |
| --- | --- | --- | --- |
| C0 | LOW_V3_C0_GENERALIZATION_PARTIALLY_SUPPORTED | 120 合成 world 推理；0 训练 | 纹理 OOD、原生收敛和复杂场不全面支持；无真实资格 |
| C1 | LOW_V3_C1_DEVELOPMENT_NOT_SUPPORTED | 各 12,000 GPU 更新；选择 step9000 | 大位移、高梯度、标准化非回归、star-like Gate 失败 |
| C1G | C1G_AFFINE_COMPENSATION_UPPER_BOUND_INSUFFICIENT | 推理诊断；0 训练；B2/B3/B4 和 LOCKED 未运行 | 即使有 GT 上界也不足；不能部署 oracle |
| C2 | LOW_V3_C2_BOUNDED_SYNTHETIC_QUALIFIED | 执行推理和独立核验；0 训练 | Wilson 下界约 68.996%，不能证明普遍成功率≥80%；跨原生尺度、复杂场、真实实验未全面资格 |
| C3A | C3A_ENGINEERING_INCONCLUSIVE | 24 校准 roots，48 选择 roots；拟合和推理执行，未进入全场 B2/LOCKED | 整体判别失败，严格 Query bitwise 失败；5 纹理条件不构成 240 独立 roots |
| C3D | C3D_STAGE_FAILURE_MECHANISM_ATTRIBUTED | 0 训练；实际阶段推理和 12-root 单独受控人口 | 暴露开发人口；bitwise 失败但容差/候选身份/selector 决策一致；oracle 仅上界 |
| C3E | LOW_V3_C3E_MULTI_HYPOTHESIS_NOT_SUPPORTED | 推理执行；0 训练；Gate2 停止，LOCKED 未运行 | GT-free 部署规则不合格，仅暴露开发数据 |
| C4 | C4_FEATURE_IDENTIFIABLE_FIELD_UNPROVEN | 实际诊断推理；0 训练；新校准/新 LOCKED 未运行 | 成片错误未可靠减少；完整反向与锚点成本不满足部署 |
| C4B | C4B_LOW_COST_BIDIRECTIONAL_EVIDENCE_INSUFFICIENT | 推理执行；0 训练；Gate1 失败 | 冻结信息充分性门槛未过；未启动独立新人口 |
| C5 | LOW_V3_C5_ENGINEERING_INCONCLUSIVE | 100 GPU smoke 更新；正式训练 0；2000-step Gate 未运行 | 共享硬件下工程不确定；5 roots/6400 Query smoke 不构成正式资格 |
| C5R | C5R_MICRO_LEARNABILITY_NOT_SUPPORTED | 早期 0 optimizer；resume A=600，B=0，正式=0 | 补充 backend parity 失败；不是所有 Refiner 不可能的证明；无独立人工审查 |
| C6 | C6_LOCAL_INFORMATION_MECHANISM_CONFIRMED | 48 新独立 roots/96 条件机制推理；0 训练 | 不能宣称所有图像信息消失或未见生成器资格；判别解释为分析后规则 |
| C7 | C7_LOCAL_FEATURE_LEARNABILITY_NOT_ESTABLISHED | 800 micro 更新；8 TRAIN roots，同 root heldout Query；正式训练 0 | 单一结构/有限训练，不是理论不可能；SELECTION/LOCKED 未生成 |
| C8 | C8_RUNTIME_NOT_SUPPORTED | 3 工程 smoke 更新后丢弃；micro/正式训练 0 | 单一工程图像对及 3 历史 GT-free replay；没有科学 learnability 否定 |
| C9 | C9_REAL_DATA_NOT_AVAILABLE | 真实序列/Query=0；0 训练；Gate0 停止 | 独立真实测量数据不可用；绝对精度未验证 |
| C9B | C9B_REAL_IMAGE_DESCRIPTIVE_EVALUATION_COMPLETE | 281 GPU 成功/282 尝试；227 科研端点；0 训练 | 无独立逐点 2D GT；16 坐标映射未核实；17 仅 crop；自洽不等于绝对准确 |
| C9C | {"risk_associations": "C9C_REAL_OBSERVABILITY_RISK_ASSOCIATIONS_SUPPORTED", "offline_support_rule": "C9C_SELECTIVE_ABSTENTION_DEVELOPMENT_SUPPORTED", "final_frame_annotation": "C9C_VISIBILITY_ANNOTATION_INCONCLUSIVE", "calibrated_reliability": "C9C_RELIABILITY_EVIDENCE_INSUFFICIENT"} | 12 新 GPU 端点/14715 Query；0 训练 | 自动未经专家审核；B1 范围；Sample16 reference pending；无独立 GT |
| C10 | C10_COHERENT_MATCHING_NOT_SUPPORTED | 24 roots：16 TRAIN/8 CHECK，1000 micro 更新；正式=0 | 均未达冻结 5pp 门槛；Gate1 失败；SELECTION/LOCKED 未生成 |
| C11 | C11_NATIVE_SYNTHETIC_MATCHING_REPAIR_CONFIRMED | 320 独立 TRAIN worlds，12,000 更新；独立 LOCKED 96G+128H | H 仍 1 coherent root/517 个 >20px，新增 19 个 >20px；上游暴露未知；无广泛分辨率/真实资格 |
| C12 | C12_ROBUSTNESS_NOT_SUPPORTED | 冻结 C11 推理；224 LOCKED 条件；0 权重更新 | 高像素位移/大旋转/Sinusoidal/Star-like 及 R2/R3 失败；纹理非完整因子矩阵 |
| C13 | C13_SCALE_AWARE_MATCHING_REPAIR_NOT_SUPPORTED_DEV_GATE_FAILED | 500 micro 后丢弃；从 C11 重启正式 12000 更新；112 DEV roots | 压力原正确保护不足；R3 rotation 16→16 coherent、误差变差；DEV Gate 失败，LOCKED 未生成/运行 |
| C14 | C14_NONROTATION_QUALIFICATION_NOT_SUPPORTED | 1000 实际更新后预注册早停；新 SELECTION 执行，LOCKED 未运行 | 原正确保留不足；训练候选新增事件/周期 Gate 失败；后验 full R3 backward 可行不改写先前协议 |
| C15 | C15_FULL_FRAME_TRAINING_NOT_SUPPORTED | CROP/FULL 各600 GPU 更新；丢弃 smoke=3；LOCKED_GT_reads=0 | Full 原正确 native 保留98.1654%：351 correct→wrong；Gate3 失败；crop 支持损失确认但非周期失败充分因果 |
| C16 | C16_A_MORE_DIAGNOSIS_REQUIRED | 32 暴露 C15 MICRO_DEV roots/288 轨迹；CPU 重建及 GPU 冻结终点复核；0 训练；C16-B未启动 | CPU/GPU 中间轨迹 max差1.7869568px、429分类差异；periodic R3 dense oracle 保留98.522%<99%；不是新独立资格 |

机制支持、工程通过、描述性关联、开发集收益和独立资格分别解释；Query/像素/分辨率/迭代次数不增加独立物理 root 数。所有停止实验均保留，重新启动需要新的独立协议。
