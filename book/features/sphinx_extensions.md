# Sphinx Extensions

Sphinx extensions are plugins developed for the Sphinx documentation ecosystem (which Jupyter Book is built upon). They extend or modify Sphinx’s capabilities and can be added to Jupyter Book for extra functionality. Since Sphinx extensions are not an integral part of jupyter-book, as opposed to original jupyter-book features, they must be installed and configured explicitly, for example in the `_config.yml` file.

At TeachBooks, we have many TA's working on developing cool and handy extensions to use in our books. Here's an overview:

- Download link replacer: Controls the download options of the chapters in your book.

- Image Inverter: Makes it possible to distinguish figures and graphs that shouldn't automatically be converted by the dark/light mode.

- Custom Launch Button: Allows you to add buttons to your book which you can use as quick access or settings options.

- JupyterBook Patches: Fixes an issue where drop down menus would still take up space after being minimized.

- TU Delft theme: Provides a simple solution to have a uniform theme across all the books created at Delft University of Technology that matches the TU Delft identity.

- Rich hover over tips: This TeachBooks Tippy extension utilizes Sphinx-tippy and makes it plug-and-play within a JupyterBook.