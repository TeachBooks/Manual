# What is a TeachBook?

Never seen a TeachBook before? Here's a small demo of our MUDE-book!


<div style="display: flex; justify-content: center;">
    <div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%;">
        <iframe
            src="https://www.youtube.com/embed/gbBsWo6em4c?si=ayKhISsx06LmGbDD"
            style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
        ></iframe>
    </div>
</div>

So what are you looking at? It's a website generated with the [Jupyter Book package](https://jupyterbook.org/). Various extensions have been added to improve the student-experience, especially for technical topics!

The source files of this book consists of three parts:
1. A configuration file to define functionalities, `_config.yml`
2. A table of contents file to list which files should endup in the book, `_toc.yml`
3. Content for your book! Text-based files which allows you to embed figures, videos, math and interactive elements.

```{admonition} Text-based files? yml? What is that?!
:class: tip, dropdown

Text-based files are digital files on your computer that you can open in a text editor and read directly. There are many file extensions used for text-based files, a few common ones related to Jupyter Book are: Markdown (`*.md`), Jupyter Notebooks (`*.ipynb`), and YAML (`*.yml`).

YAML (or YML) is a text-based file format that is primarily used to store data. It is useful because it is easy for humans to read and write, and easy for machines to _parse_ and generate., which is why YAML is often used for configuration files. Here is an example of a YAML file...can you tell what information is being stored?


```

A book is made by by writing content in text-based files such as Markdown (`*.md`), Jupyter Notebooks (`*.ipynb`), etc. After that, software is used to "parse" these files and create the final book (e.g., Jupyter Book)

```{admonition} Comparing and Contrasting to LaTeX

Have you ever used LaTeX? It turns out there are a lot of similarities with this document system. Here is a quick list:
1. Writing "source code" in text-based files (i.e., `*.tex` versus `*.md`, `*.ipynb`, etc) that is generally easy to read without the markup and uses special functions to format rich document objects (e.g., tables, figures, etc).
2. The "book" is created by using a piece of software that parses the source code and creates the final document (a `*.pdf` versus a `*.html` for Jupyter Book).
3. Creating the document structure using a list of files that contain source code that automatically generates the Table of Contents and Index..
4. Sometimes you can spend more time than you like troubleshooting "bugs" that turn out to be simple syntax errors.
``` 

Let's see how these books are made!