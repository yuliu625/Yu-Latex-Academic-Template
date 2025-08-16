# Latex Academic Template
In this template repository, I have defined a **LaTeX project template** with a clear structure and reusable content.
It follows a standardized project structure to efficiently write academic papers, reports, or prepare academic presentations.


## Design Features
- **Structured Management**: Organizes different types of content (such as chapters, figures, and algorithms) into separate categories, avoiding a single, overly long `main.tex` file that is difficult to control and manage.
- **Content Reusability**: Easily reuse existing content across different projects or templates. For example, you can copy the entire `contents` folder to a new project, or directly use pre-built figures and algorithms in an academic presentation (using `beamer`).
- **Easy Maintenance**: A clear file structure makes the project easier to maintain and update, especially in a collaborative environment.


### Project Structure
```bash
.
├── main.tex                 # The main file, which imports content from the contents folder
└── contents/
    ├── sections/            # Main chapters of the paper (e.g., introduction, methods, experiments)
    ├── references/          # Bibliography file (.bib)
    ├── figures/             # Figure files and their corresponding LaTeX code
    │   ├── original_figures/  # (Optional) Stores original image files (e.g., .svg, .ai)
    │   └── ...
    ├── tables/              # Table files and their corresponding LaTeX code
    └── algorithms/          # Algorithm pseudocode files
```


### Usage Scenarios
1. **New Project**: Clone (`git clone`) the entire repository locally, then start editing the files in the `contents` folder.
2. **Switching Templates**:
   - When submitting a paper to different conferences or journals, simply copy the entire `contents` folder to the new template project.
   - If necessary, use commands like `\input{contents/sections/specific_section.tex}` in the new template's `main.tex` or main file to import the required content (as shown in the `main.tex` file example).
3. **Academic Presentations**:
   - When building `beamer` slides, you can directly reference existing files in the `figures`, `tables`, or `algorithms` folders without rewriting them.


## More Information
- **Bibliography**: This project uses **BibTeX** by default, which is compatible with various citation management systems. You can place the `.bib` file in the `contents/references` folder.
- **Figures**: It is recommended to create an `original_figures` subfolder under the `figures` folder to store the original editable files of the figures (e.g., `.svg`, `.ai`), for easy future modification. Each `.tex` file can directly include the figure and its corresponding caption, making it easy to `\input` it directly in `main.tex`.
- **Algorithms**: This project primarily uses the `{algorithm, algpseudocode}` environment. If you use other packages (like `{algpseudocode}`), you can adjust it as needed.


## Other Projects
In addition to the LaTeX template, I have also built an academic template based on **Typst**: [Typst-Academic-Template](https://github.com/yuliu625/Yu-Typst-Academic-Template). Although Typst is a more modern and efficient typesetting tool (of course, it has some issues), LaTeX is still the mainstream standard in academia. You can:
- Use Typst to quickly build content.
- Use related tools to convert the Typst project into LaTeX format. (This applies to personal papers; collaborative papers may require a shared LaTeX online editor.)

The purpose of this template series is to easily convert and reuse content between different typesetting tools to meet various collaboration and submission needs.

