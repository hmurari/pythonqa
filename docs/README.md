# Pandoc Book Maker Template
Template for creating epub books from markdown using `pandoc`.

[![forthebadge](http://forthebadge.com/images/badges/built-by-hipsters.svg)](http://forthebadge.com)

## Instructions

### Install Pandoc

#### Debian, Ubuntu, and derivatives
- With package: [pandoc-1.19.2.1-1-amd64.deb](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-1-amd64.deb)

#### macOS
- With `brew`:
```bash
brew install pandoc
```
- With package: [pandoc-1.19.2.1-osx.pkg](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-osx.pkg)

#### Windows
- With MSI: [pandoc-1.19.2.1-windows.msi](https://github.com/jgm/pandoc/releases/download/1.19.2.1/pandoc-1.19.2.1-windows.msi)

### Create Book
1. Change to `docs` directory.
2. Run `make content` command to create `contents.markdown` file.
3. Run `make pdf` command to create `book.pdf` file.
4. Run `make book` command to create `book.epub` file.



## Mermaid extensions

1. Install the mermaid filter extension
``` bash
npm install --global mermaid-filter
```

2. Run pandoc with the mermaid filter
``` bash
pandoc -F mermaid-filter <rest of the command>
```

Other details available at: https://github.com/raghur/mermaid-filter


## Pandoc & Latex Information

- The PDF file usually does not look like a book. In order to add title page, back cover page etc., we will be modifying the PDF file template that Pandoc uses. 
``` bash
pandoc -D latex > pdf-book-template.tex
```

- And make a few modifications to it. So it looks like the `pdf-book-template.tex` file provided in this repo .


## Book Latex Templates

- https://github.com/Wandmalfarbe/pandoc-latex-template

- https://github.com/wikiti/pandoc-book-template


