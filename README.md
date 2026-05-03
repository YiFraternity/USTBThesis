# 北京科技大学硕士学位论文非官方模板

本项目是北京科技大学学位论文非官方模板，由「北京理工大学」学位论文模板 [BITNP/BIThesis](https://github.com/BITNP/BIThesis) 修改而来。当前封面、题名页、页眉、前置部分和正文结构等内容按《北京科技大学硕士学位论文模板》规范进行调整。

> [!NOTE]
> 本项目不是北京科技大学官方发布的模板；实际排版要求以《北京科技大学硕士学位论文模板》规范为准。

## 特性

- 面向北京科技大学硕士学位论文排版。
- 按《北京科技大学硕士学位论文模板》规范调整封面、题名页、页眉等前置部分。
- 正文部分的行间距、表格和图片 caption 等格式已按规范完成。
- 内容和样式分离，论文信息和正文入口集中在 `main.tex`。
- 支持 XeLaTeX 与 Biber 编译。

## 项目结构

```sh
.
├── README.md                         # 项目说明
├── latexmkrc                         # latexmk 编译配置
├── main.tex                          # 论文主文件
├── main.pdf                          # 编译生成的论文 PDF
├── ustbthesis.cls                    # 北京科技大学学位论文模板类文件
├── chapters                          # 正文章节
│   ├── abstract.tex                  # 中英文摘要
│   ├── chapter1.tex                  # 第 1 章
│   └── chapter2.tex                  # 第 2 章
├── figures                           # 论文插图
│   └── figure1.png
├── images                            # 模板图片资源
│   └── header.pdf
├── misc                              # 后置部分和辅助内容
│   ├── 0_symbols.tex                 # 主要符号对照表
│   ├── 1_conclusion.tex              # 结论
│   ├── 2_reference.tex               # 参考文献入口
│   ├── 3_appendices.tex              # 附录
│   ├── 4_pub.tex                     # 攻读学位期间成果
│   ├── 5_resume.tex                  # 作者简介
│   ├── acknowledgements.tex          # 致谢
│   ├── dataset.tex                   # 数据集说明
│   ├── statement.tex                 # 声明页内容
│   ├── icon_academic.jpg             # 学术型图标资源
│   └── icon_professional.jpg         # 专业型图标资源
└── reference                         # BibTeX 数据库
    ├── main.bib                      # 参考文献
    └── pub.bib                       # 成果清单
```

## 编译方式

方式一（推荐）：

```sh
latexmk -xelatex -interaction=nonstopmode -halt-on-error main.tex
```

方式二：

```sh
xelatex -interaction=nonstopmode -halt-on-error main.tex
biber main
xelatex -interaction=nonstopmode -halt-on-error main.tex
xelatex -interaction=nonstopmode -halt-on-error main.tex
```

- 不推荐使用 `pdflatex` 编译。

## 排版参考

- 《北京科技大学硕士学位论文模板》
