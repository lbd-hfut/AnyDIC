# 模型权威与使用范围

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

正式生产 LOW 是 **AnyDIC V2.0 Final**，继承主项目 架构文档 `docs/CURRENT_ARCHITECTURE.md`（原完整仓库文件，不含于本快照） 与 模型卡 `docs/releases/ANYDIC_V2_MODEL_CARD.md`（原完整仓库文件，不含于本快照）。本次不改变任何生产源码、配置、权重或 main 指针。

| 身份 | 权威/资格 | 使用边界 |
| --- | --- | --- |
| AnyDIC V2.0 Final | 当前正式 LOW；冻结科学 tag anydic-v2.0-final | 原始资格和已披露回归/长尾保持；不声称普适计量精度 |
| LOW_V3_D4_DIRECT | 冻结历史研究基线 | LOW_V3_C2_BOUNDED_SYNTHETIC_QUALIFIED；IID192/Query 有界支持，无广泛真实/尺度资格 |
| C11_SEA_12000 | C11_NATIVE_SYNTHETIC_MATCHING_REPAIR_CONFIRMED | 独立192×256连续合成 GT 下主要新匹配候选；不能自动替换 D4 或生产 LOW |
| C13_MAIN_12000 | DEV Gate 失败 | 可作为新协议对照/诊断初始化，不是跨尺度合格模型 |
| C14_STEP1000 | 非大旋转资格失败 | 负结果；不能成为默认 matcher |
| C15 Crop600 / Full600 | 配对训练真实执行，Full gate 失败 | 保存周期收益与正确点保护回归，用于轨迹诊断 |
| C16-A | MORE_DIAGNOSIS_REQUIRED | 诊断源码/结果；没有新训练模型，也没有完成 C16-B |
| GMFlow + SEA-RAFT 联合求解器 | 未来方案 | 未实现、未训练、未获得科学资格 |

C11 confidence 是预测 target 在界有效性，不是经校准的正确概率。D4/C11 都保留原合格人口和残余失败，平均改善不得抵消 correct→wrong、严重尾部或 coherent 回归。
