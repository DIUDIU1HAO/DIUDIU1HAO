# 你好，我是 <你的名字>

用 Python 写面向开发者的检查工具。做这类工具有个固定顺序：先定义「什么算错」，再写检查，最后保证工具能通过对自己的检查。

下面两个工具，都是自己在工作里反复踩到同一个坑之后写的。

---

### deadcite · 找出 AI 报告里的假引用

AI 生成的调研报告里，引用常常是编的：编号悬空、链接死掉、数字和原文对不上。

`deadcite` 输入报告与信源，逐条给出判定，并且**把「确证」和「可疑」严格分开**——只做机械可验证的检查，不调用大模型。零第三方依赖，24 项测试，`--json` 可直接接 CI。

`Python` · `CLI` · `文本解析` · `pytest`

[代码](https://github.com/DIUDIU1HAO/deadcite) · [Release v0.1.0](https://github.com/DIUDIU1HAO/deadcite/releases/tag/v0.1.0)

### hancheck · 中文项目的代码体检

全角标点进了语法、全角空格被当缩进、函数名里藏零宽字符、文件是 GBK、测试代码里写着真实身份证号——这些问题不报错，只让结果悄悄错掉。

12 条规则，按「代码结构 / 字符串 / 注释 / 正文」分区定级，所以注释里的中文标点不会被误报。

`Python` · `静态分析` · `pre-commit`

[代码](https://github.com/DIUDIU1HAO/hancheck)

---

## 技术栈

- **主要**：Python，标准库为主（argparse、re、urllib），CLI 与文本解析
- **用过**：PyTorch、Transformers、scikit-learn、FastAPI（BERT 文本分类，训练到接口的完整链路）
- **工程**：Git（分支 / tag / Release）、pytest、pre-commit、打包与元数据

## 其他项目

- [product-title-classifier](https://github.com/DIUDIU1HAO/product-title-classifier)：BERT 商品标题分类的端到端练习。小样本，用于跑通数据 → 训练 → 评估 → 接口，不是生产模型。

## 联系

- 邮箱：<you@example.com>
- 其他：<掘金 / V2EX / 博客主页>
