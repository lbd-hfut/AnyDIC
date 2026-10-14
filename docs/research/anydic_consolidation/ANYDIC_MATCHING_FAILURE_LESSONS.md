# 匹配失效与保留教训

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

1. D4 的 F4 hard winner 会丢失正确支持，F1/E1 辨别不足与 F8 大旋转覆盖损失同时存在。C3D/C6 的 oracle 是诊断上界，不能进入推理或成为可部署收益。
2. 相似度、TopK 召回、loss 或单点平均改善不充分。C3A/C3E/C4/C4B/C10 没有证明合法输出决策可稳定恢复完整场；双向一致性和 confidence 也不是绝对准确度。
3. C5 的工程不确定、C5R/C7 的有界学习负结果、C8 的 runtime 停止含义不同。不得将未训练工程停止概括为局部学习不可能。
4. C11 证实完整 recurrent matcher 的真实合成对应恢复，但仍有 stress 的 coherent 和 >20px 错误。C12 暴露跨原生尺度、周期/旋转/纹理/成像问题。
5. 像素幅度与物理特征采样交互。相同约84.8px平移在 C13 机制对照中 R1/R2/R3 误差约0.109/6.547/71.562px；不能只靠缩放 flow 宣称物理收敛。
6. 改善粗初始化可能被原生更新破坏。C13/C14/C15 原正确点保护失败必须单独报告。C14 的完整 R3 backward 后验可行，不能将共享 GPU 下早期 OOM 扩大为结构不可行。
7. C15 确认 crop 对应支持损失，却没有确认它是周期失败充分根因；Full600 有实际周期收益仍不合格。C16 发现 latent flow、hidden、相关查询和 convex upsampling 共同演化，不能用 flow-only gate 声称原生像素保护。
8. C16 CPU 重建存在 GPU 数值差异，原 GPU 终点仍权威。提前退出、逐点输出 oracle 和 uncertainty 阈值的负结果限于已暴露的32 roots，不排除新 controller 生成不同轨迹。
9. C9B/C9C 真实图像是描述性/风险关联证据，缺少独立逐点2D GT。后续独立科学协议需物理 world 级划分、训练/选择/锁定隔离和分辨率/族级正确点保护。

每项结论的原始分支、Decision、人口和执行状态见 [历史](ANYDIC_RESEARCH_HISTORY_C0_C16.md) 与 [来源](RESEARCH_SOURCE_INDEX.json)。
