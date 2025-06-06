# LaTeX Project Template

This is a clean and reusable LaTeX project template with a modern file organization and automated build setup using `latexmk`. It is optimized for use with **Visual Studio Code** and the **LaTeX Workshop** extension.

---

## 📁 Project Structure

```
.
├── main.tex             # Your LaTeX source
├── main.pdf             # Final PDF output
├── .aux/                # Build artifacts (hidden)
├── .gitignore           # Ignores build files, backups, etc.
└── .vscode/
    └── settings.json    # VS Code LaTeX Workshop config
```

---

## ⚙️ Build System with `latexmk`

This template uses [`latexmk`](https://ctan.org/pkg/latexmk) with the following configuration:

- All auxiliary and intermediate files (e.g. `.aux`, `.log`, `.toc`, `.bbl`, `.synctex.gz`, etc.) are stored in `.aux/`
- The final PDF is generated in the root folder as `main.pdf`
- Build is fully automated and supports multi-pass compilation

### Manual build (from terminal):

```bash
latexmk -pdf -output-directory=.aux main.tex
```

---

## 🧠 Why `.aux/`?

- Keeps your project folder clean
- Helps avoid accidental commits of temporary files
- Easy to clean up (`rm -rf .aux/`)

---

## 🧰 VS Code Integration

This template includes a preconfigured `.vscode/settings.json` for use with the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension.

### Features:

- Auto-build on save (optional)
- PDF preview in a VS Code tab
- SyncTeX forward/inverse search
- Hidden `.aux/` and `.synctex.gz` files in the file explorer

No need to configure anything — just open the folder in VS Code and start working.

---

## 🧹 Clean Build

You can remove temporary files with:

```bash
latexmk -C -output-directory=.aux
rm -rf .aux/
```

This keeps only your `.tex` source and final `.pdf`.

---

## 🔁 Using this as a Template

This repository is designed to be used as a GitHub **template repository**.

To create a new project:

1. Click the **"Use this template"** button on the GitHub page
2. Name your new repository
3. Clone it and start editing `main.tex`

---

## 💡 Customization

- Rename `main.tex` to match your project
- Add `.bib` files for bibliography support (BibTeX/Biber)
- Extend with additional `.sty`, `.cls`, or subfolders as needed

---

## 🧪 Tested Environments

- [x] macOS + TeX Live + VS Code
- [x] Ubuntu + TeX Live + VS Code
- [x] Windows + MiKTeX + VS Code (with `latexmk` installed via MiKTeX or `choco`)

---

## 🛡️ GitHub / Git Setup

The included `.gitignore` excludes all LaTeX build artifacts and editor backup files. Only your source files and output `.pdf` are tracked.

If you don’t want to version the PDF, just add `*.pdf` to `.gitignore`.

cmd + opt + J tex -> pdf
cmd + click   pdf -> tex
