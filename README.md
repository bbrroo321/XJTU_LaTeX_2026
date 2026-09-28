# 西安交通大学 2026 届本科毕业论文 LaTeX 模板

> **XJTU Bachelor's Degree Thesis LaTeX Template (2026)**
> 西安交通大学本科毕业设计（论文）LaTeX 模板 · 西交大 2026 届毕设排版模板

在线预览主页：<https://bbrroo321.github.io/XJTU_LaTeX_2026/>

---

## 目录

- [简介](#简介)
- [快速开始](#快速开始)
- [目录结构](#目录结构)
- [相较 2022 版的修改](#相较-2022-版的修改)
- [已知问题](#已知问题)
- [中文字数统计工具](#中文字数统计工具)
- [致谢与来源](#致谢与来源)
- [联系方式](#联系方式)
- [许可协议](#许可协议)
- [English](#english)

---

## 简介

本模板面向**西安交通大学 2026 届本科毕业设计（论文）**，提供一个可以直接使用的 LaTeX 排版方案，用于替代 WPS / Word 繁琐的格式调整流程。

本模板的标准参考是西安交通大学提供的 Word 模板 **《本科毕业设计（论文）模版 + (2025 修订版)》**（见仓库中的 `2025年本科毕业设计模版` 文件夹）。**2026 届的毕设格式要求仍与 2025 年一致。**

> ⚠️ **免责声明**
> 本模板仅作参考，作者对使用本模板可能产生的任何格式错误不负责任。在使用本文件之前，请务必检查你的论文格式要求。

**测试环境**：TeX Live 2026-03-01，Windows 11 23H2。未在 Linux、macOS 上测试。

## 快速开始

1. 打开 `XJTU-BSThesis_latex_2026/xjtuBS.tex`。
2. **编译前请仔细阅读文件开头的使用说明**，并根据你的系统修改 `\documentclass` 选项：

   | 系统 | 写法 |
   | --- | --- |
   | Windows | `\documentclass[Win]{xjtuBSThesis}` |
   | macOS | `\documentclass[Mac]{xjtuBSThesis}` |
   | Linux | `\documentclass[Linux]{xjtuBSThesis}` |

3. 使用 **XeLaTeX** 编译（文件头已标注 `%!TEX TS-program = xelatex`）。
4. 参考文献按 `sample.bib` 的写法填写，例如：

   ```bibtex
   @article{陈润泽2014含储热光热电站的电网调度模型与并网效益分析,
     title={含储热光热电站的电网调度模型与并网效益分析},
     author={陈润泽 and 孙宏斌 and 李正烁 and 刘一兵},
     journal={电力系统自动化},
     volume={19},
     pages={001},
     year={2014}
   }
   ```

5. `xjtuBS.tex` 的第二个 section 给出了常用功能的用法示范，可直接照抄。

**导入任务书 / 考核评议书 / 答辩结果**：使用系统下载的 Word 文件制作 PDF 后导入即可（见下方第 9 条修改说明）。

## 目录结构

```
.
├── README.md
├── LICENSE
├── XJTU-BSThesis_latex_2026/
│   ├── xjtuBS.tex                      # 主文件，从这里开始
│   ├── xjtuBSThesis.cls                # 文档类（格式定义）
│   ├── sample.bib                      # 参考文献示例
│   ├── gbt7714-numerical.bst           # 国标参考文献样式
│   └── figure/                         # 校徽等图片资源
├── Counting_Chinese/                   # 中文字符统计脚本
│   └── Chinese_Character_Counter_linux_mac.sh
└── 2025年本科毕业设计模版/              # 官方 Word 模板（格式参考基准）
```

## 相较 2022 版的修改

本模板主体来自 [ChenjieGump/XJTU-BSThesis_latex_2022](https://github.com/ChenjieGump/XJTU-BSThesis_latex_2022)（作者：ChenjieGump，干晨劼）。

本项目作者根据《本科毕业设计（论文）模版 + (2025 修订版)》的具体要求进行了详细修改，主要修改内容如下：

1. 调整了目录中「摘要」「致谢」「附录」字段的样式
2. 调整了行距与各级标题段落前后间隔
3. 修复了表格宽度与正文版面不平齐的问题
4. 调整了参考文献编码制
5. 调整了参考文献表的排版、字号等
6. 调整了页眉中部分字段的样式
7. 调整了正文距离页眉的距离
8. 调整了奇偶页排版的规则，使得绪论之后的正文章节从新一页而非新的奇数页开始
9. 添加了导入「任务书」「考核评议书」「答辩结果」的方法，使用系统下载的 Word 文件制作 PDF 并导入即可
10. 修复了公式中加粗字体显示错误的问题

## 已知问题

1. 主要符号表（denotation）无法使用
2. 行距与各级标题段落前后间隔可能有问题，请认真对照模板，检查它们看起来是否一样
3. 附录目前只支持纯文本

## 中文字数统计工具

`Counting_Chinese` 文件夹用于统计中文字符，**目前只支持 macOS 和 Linux**。请先用记事本打开，里面有说明使用方法。

> ⚠️ **注意不要修改该文件夹的名称！**

## 致谢与来源

本模板站在多位前人的工作之上：

| 版本 | 作者 | 来源 |
| --- | --- | --- |
| 2022 版 | Chenjie Gan（干晨劼） | <https://github.com/ChenjieGump/XJTU-BSThesis_latex_2022> |
| 2016 版 | Lingxiao Zhao（赵令霄） | <https://github.com/LingxiaoShawn/XJTU_LaTeX> |
| 更早 | XJTU CTex Model（MCMTHESIS.cls, 2011） | wanghongxin 等 |
| 更早 | NJU LaTeX Model | 张楚珩 Chuheng Zhang |

另外感谢 Hu Haixing 提供的南京大学硕博学位论文模板。

## 联系方式

| 版本 | 作者 | 邮箱 |
| --- | --- | --- |
| 2026 版 | wangqiaozhi | wangqiaozhi@stu.xjtu.edu.cn |
| 2022 版 | ChenjieGump | ganchenjie@stu.xjtu.edu.cn / chenjie_gan@brown.edu |
| 2016 版 | Lingxiao | lingxiao@cmu.edu |

如遇问题欢迎提 [Issue](https://github.com/bbrroo321/XJTU_LaTeX_2026/issues)。

## 许可协议

[MIT License](LICENSE) © 2026 bbrroo321

---

## English

**XJTU Bachelor's Degree Thesis LaTeX Template (2026)** — a LaTeX template for the bachelor's degree thesis of Xi'an Jiaotong University (XJTU), class of 2026. Tailored to the official Word template *本科毕业设计（论文）模版 + (2025 修订版)*.

- Main file: [`XJTU-BSThesis_latex_2026/xjtuBS.tex`](XJTU-BSThesis_latex_2026/xjtuBS.tex), compile with **XeLaTeX**
- Set your OS in `\documentclass[Win|Mac|Linux]{xjtuBSThesis}`
- Based on [XJTU-BSThesis_latex_2022](https://github.com/ChenjieGump/XJTU-BSThesis_latex_2022) by Chenjie Gan
- Tested on TeX Live 2026-03-01 / Windows 11 23H2; not tested on Linux or macOS
- This template is for reference only. Always verify your formatting against the official requirements.
- Licensed under the [MIT License](LICENSE).

**Keywords**: XJTU LaTeX template, Xi'an Jiaotong University thesis template, bachelor thesis LaTeX, Chinese thesis, gbt7714, xelatex, 西安交通大学 LaTeX 模板, 西交大毕业论文模板.
