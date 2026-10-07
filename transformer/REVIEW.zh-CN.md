# Transformer 课件核对修改说明

核对对象：transformer-study-guide.html；原始来源：Alan Ritter 的 nn_text.pdf（203 页）。页码按 PDF 阅读器从 1 开始计数。

整体教学顺序正确，主要需要修正的是记号对应、过度概括和原课件内容的归属。

| 位置 | 原稿问题 | 修订 |
|---|---|---|
| Attention | 加性打分 tanh 输出缺少标量投影 | 补写 vᵀ tanh(...)，修正双线性转置记号 |
| Self-Attention 图 | great 自身的加权求和路径漏画，权重无说明 | 重绘四个位置全部参与的示意图，注明非实测 |
| Q/K/V | 将老师的 W_k 等同于 Key 投影 W_K | 说明 W_k 是双线性打分矩阵，对应 Query/Key 投影的乘积 |
| 缩放 | 方差推导未给假设，饱和结论过于绝对 | 补独立、零均值、单位方差假设，用“可能”描述训练问题 |
| 多头 | 说成直接切分向量，Big 写 1000 维 | 改为不同学习投影，Big 精确为 1024 维；补输出投影公式 |
| 位置编码 | 距离近点积必然大、one-hot 等同原论文比较 | 补振荡点积公式；原论文比较的是 learned positional embedding |
| 原课件归属 | 声称老师没画 Encoder 内部结构 | 第 161 页实际有 Attention、FFN、Add & Norm 图 |
| Encoder | 未区分 Post-LN/Pre-LN；LayerNorm 输出被说成固定均值方差 | 标明原版 Post-LN，补常见 Pre-LN；补 γ、β、ε |
| FFN | 一概说占一半参数 | 原版 Encoder Block 中约 2/3 权重，注明统计范围 |
| Decoder 图 | 缺 embedding/位置编码、多层堆叠、输出 Linear | 补完整流程，注明 GPT 通常无 Cross-Attention |
| Teacher Forcing | 容易让人以为 RNN 也能全序列并行 | 说明 RNN 状态仍递推；新增右移输入/标签对齐表 |
| Tokenization | 声称老师完全没提、Transformer 从不按完整词 | 第 185 页提到 WordPiece；说明 token 可对应完整词等多种单位 |
| BPE/WordPiece | 字符级和字节级混用；WordPiece 训练规则过于确定 | 区分两类 BPE；说明 BERT 未公开完整词表训练实现 |
| ELMo | 整体被称为单向 | 区分两个单向 LM 与组合后的 biLM |
| BERT | 将 15% 全说成 [MASK] | 15% 是预测目标；其中 80/10/10，整体约 12% 换 [MASK]；老师第 183 页已讲 |
| BERT 位置 | 容易误套 sin/cos | 补可学习位置与 segment embedding |
| T5 | 自测问训练目标，正文没有答案 | 新增 span corruption 与 sentinel 说明 |
| 历史与拓展 | 旧成本像当前报价；RLHF 起点和商业模型结构断言不准确 | 标明历史估计，修正时间归属，移除未证实的精确结构断言 |

已检查桌面浏览器中的 Self-Attention 图和 Decoder 流程，并验证目录链接、唯一 ID 和 SVG 结构。修订版保留原稿中文复习风格及颜色布局，补充原 PDF 页码和论文链接。
