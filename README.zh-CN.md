# Latex Academic Template
我在这个模板仓库定义了一个结构清晰、内容易于复用的 **LaTeX 项目模板**。
它遵循一套标准化的项目结构，以能够更高效地撰写学术论文、报告或进行学术演讲。


## 设计特性
- **结构化管理**: 将不同类型的内容（如章节、图表、算法等）分门别类地组织，避免单个`main.tex`文件过长而难以控制和管理。
- **内容复用**: 轻松地在不同项目或模板间复用已有的内容，如将整个`contents`文件夹复制到新项目中，或在学术演讲(使用`beamer`)中直接调用已构建的图表和算法。
- **易于维护**: 清晰的文件结构使项目更易于维护和更新，尤其是多人合作的场景。


### 项目结构
```bash
.
├── main.tex                 # 主文件，通过 input 导入 contents 中的内容
└── contents/
    ├── sections/            # 论文的主要章节内容（如引言、方法、实验等）
    ├── references/          # 参考文献文件（.bib）
    ├── figures/             # 图片文件及其对应的 LaTeX 代码
    │   ├── original_figures/  # （可选）存放原始图片文件（如 .svg, .ai 等）
    │   └── ...
    ├── tables/              # 表格文件及其对应的 LaTeX 代码
    └── algorithms/          # 算法伪代码文件
```

### 使用场景
1. **新建项目**: 将整个仓库克隆(`git clone`)到本地，然后开始编辑 `contents` 文件夹中的文件。
1. **切换模板**: 
   - 当需要将论文提交到不同会议或期刊时，只需将整个 `contents` 文件夹复制到新的模板项目中。
   - 必要的，在新模板的 `main.tex` 或主文件中，使用`\input{contents/sections/specific_section.tex}`等命令导入所需的内容(正如`main.tex`文件示例)。
1. **学术演讲**：
   - 构建`beamer`幻灯片时，可以直接引用`figures`、`tables`或`algorithms`文件夹中已有的文件，无需重新编写。


## 更多说明
- **参考文献**: 本项目默认使用 **BibTeX**，它兼容多种文献管理系统。可以将`.bib`文件放置在`contents/references`文件夹中。
- **图片**: 建议在`figures`文件夹下创建`original_figures`子文件夹，用于存放图片的原始编辑文件(如`.svg`、`.ai`等)，以便后续修改。每个`.tex`文件可以直接包含图片和对应的`caption`，方便在`main.tex`中直接`\input`导入。
- **算法**: 本项目主要使用`{algorithm, algpseudocode}`环境。如果使用其他宏包(如 `{algpseudocode}`)，可以根据需要进行调整。


## 其他项目
除了 LaTeX 模板，我还构建了一个基于**Typst**的学术模板[Typst-Academic-Template](https://github.com/yuliu625/Yu-Typst-Academic-Template)。尽管Typst是一种更现代、高效的排版工具(当然也存在一些问题)，但目前LaTeX仍然是学术界的主流规范。你可以:
- 使用Typst快速构建内容。
- 利用相关工具将Typst项目转换为LaTeX格式。(对于个人论文如此，合作论文可能需要共同使用LaTeX在线编辑工具。)

这个模板系列的目的，是为了能够轻松地在不同排版工具间转换和复用内容，以适应不同的合作和投稿需求。

