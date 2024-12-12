# What is a TeachBook?


Anatomy of a Book


Three parts to a book:
1. A configuration file, `_config.yml`
2. A table of contents file, `_toc.yml`
3. Content for your book! Text-based files.

```{admonition} Text-based files? yml? What is that?!
:class: tip, dropdown

Text-based files are digital files on your computer that you can open in a text editor and read directly. There are many file extensions used for text-based files, a few common ones related to Jupyter Book are: Markdown (`*.md`), Jupyter Notebooks (`*.ipynb`), and YAML (`*.yml`).

YAML (or YML) is a text-based file format that is primarily used to store data. It is useful because it is easy for humans to read and write, and easy for machines to _parse_ and generate., which is why YAML is often used for configuration files. Here is an example of a YAML file...can you tell what information is being stored?


```

## How a book is made

1. Content is written in text-based files such as Markdown (`*.md`), Jupyter Notebooks (`*.ipynb`), etc.
2. Software is used to "parse" these files and create the final book (e.g., Jupyter Book)


A hint of the key tools
- Python
- Git and GitHub
- A web browser

```{admonition} Comparing and Contrasting to LaTeX

Have you ever used LaTeX? It turns out there are a lot of similarities with this document system. Here is a quick list:
1. Writing "source code" in text-based files (i.e., `*.tex` versus `*.md`, `*.ipynb`, etc) that is generally easy to read without the markup and uses special functions to format rich document objects (e.g., tables, figures, etc).
2. The "book" is created by using a piece of software that parses the source code and creates the final document (a `*.pdf` versus a `*.html` for Jupyter Book).
3. Creating the document structure using a list of files that contain source code that automatically generates the Table of Contents and Index..
4. Sometimes you can spend more time than you like troubleshooting "bugs" that turn out to be simple syntax errors.
``` 


the rest is just 