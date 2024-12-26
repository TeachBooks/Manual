# Badges, Buttons & Icons

<a href="https://jupyterbook.org/"><img  style="display:inline-block; height:1.5em; width:auto; transform:translate(0, -0.15em)" src="../images/logo-wide.svg" alt="Jupyter book"></a> provides a range of features which are visually appealing and functional. These elements can enhance the interactivity and visual design of your book, offering additional information or links in a compact and visually engaging way. The badges, buttons and icons are made available through Sphinx and they themselves wrote a [documentation](https://sphinx-design.readthedocs.io/en/latest/badges_buttons.html) about it.

## Badges

Badges are small visual indicators often used to convey concise or important information. They can be very useful for categorising or tagging content for the reader like has been done for the subchapters under the [features](../features/overview.md) chapter of this manual. There are three types of badges: plain, link and reference. They are fully customizable and can simply be added with Markdown syntax:

| Badge Preview                                                   | Code Syntax                   |
|-----------------------------------------------------------------|-------------------------------|
| {bdg-primary}`plain_text`                                       | `{bdg-primary}`plain_text``                |
| {bdg-link-primary}`https://teachbooks.io/`                      | `{bdg-link-primary}`https://teachbooks.io/``        |
| {bdg-link-primary}`TeachBooks <https://https://teachbooks.io/>` | `{bdg-link-primary}`TeachBooks <https://https://teachbooks.io/>``     |
| {bdg-ref-primary}`my_ref`                                       | `{bdg-ref-primary}`my_ref``   |


| Badge Preview                 | Code Syntax                   |
|-------------------------------|-------------------------------|
| {bdg}`my_text`                | `{bdg}`my_text``                |
| {bdg-primary}`my_text`        | `{bdg-primary}`my_text``        |
| {bdg-primary-line}`my_text`   | `{bdg-primary-line}`my_text``  |
| {bdg-secondary}`my_text`      | `{bdg-secondary}`my_text``      |
| {bdg-secondary-line}`my_text` | `{bdg-secondary-line}my_text` |
| {bdg-success}`my_text`        | `{bdg-success}my_text`        |
| {bdg-success-line}`my_text`   | `{bdg-success-line}my_text`   |
| {bdg-info}`my_text`           | `{bdg-info}my_text`           |
| {bdg-info-line}`my_text`      | `{bdg-info-line}my_text`      |
| {bdg-warning}`my_text`        | `{bdg-warning}my_text`        |
| {bdg-warning-line}`my_text`   | `{bdg-warning-line}my_text`   |
| {bdg-danger}`my_text`         | `{bdg-danger}my_text`         |
| {bdg-danger-line}`my_text`    | `{bdg-danger-line}my_text`    |
| {bdg-light}`my_text`          | `{bdg-light}my_text`          |
| {bdg-light-line}`my_text`     | `{bdg-light-line}my_text`     |
| {bdg-muted}`my_text`          | `{bdg-muted}my_text`          |
| {bdg-muted-line}`my_text`     | `{bdg-muted-line}my_text`     |
| {bdg-dark}`my_text`           | `{bdg-dark}my_text`           |
| {bdg-dark-line}`my_text`      | `{bdg-dark-line}my_text`      |
| {bdg-white}`my_text`          | `{bdg-white}my_text`          |
| {bdg-white-line}`my_text`     | `{bdg-white-line}my_text`     |
| {bdg-black}`my_text`          | `{bdg-black}my_text`          |
| {bdg-black-line}`my_text`     | `{bdg-black-line}my_text`     |


## Buttons
Buttons provide a way to create clickable elements that are more attractive than links. Jupyter-Book supports buttons using Markdown or HTML, making them highly customizable.

Adding Buttons with Markdown
To create a button in Markdown, you can use HTML for full flexibility. For example:

markdown
Code kopiëren
<a href="https://jupyterbook.org" class="btn btn-primary">Visit Jupyter-Book</a>
This will produce a styled button that links to the Jupyter-Book site.

Predefined Button Classes
Jupyter-Book uses Bootstrap for styling, so you can apply classes such as:

btn-primary (blue)
btn-secondary (gray)
btn-success (green)
btn-danger (red)
btn-warning (yellow)
You can experiment with these styles to create buttons that align with your book's theme.

3. Icons
Icons can be included to visually represent actions or categories. Jupyter-Book supports FontAwesome icons, which can be integrated using HTML syntax.

Adding Icons
To add an icon, use the following syntax:

markdown
Code kopiëren
<i class="fas fa-book"></i> Jupyter-Book
This example adds a "book" icon before the text "Jupyter-Book."

Combining Buttons and Icons
Icons can also be included within buttons for a modern, professional look:

markdown
Code kopiëren
<a href="https://jupyterbook.org" class="btn btn-primary">
    <i class="fas fa-download"></i> Download Book
</a>
This button includes a "download" icon alongside text.

4. Use Cases
Here are some practical use cases for badges, buttons, and icons in a Jupyter-Book:

Badges: Highlight software version, repository status, or contributors.
Buttons: Link to key sections of your book, such as downloads or external resources.
Icons: Add visual appeal or clarity to navigation links or labels.
Incorporating these elements into your Jupyter-Book improves both the aesthetic and functionality of your book, creating a more engaging experience for readers.