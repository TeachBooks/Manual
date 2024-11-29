# Adding interactive h5p elements

```{admonition} User types
:class: tip
This section is useful for user type 3-5.
```

{bdg-info}`iframe`

## Instruction
H5p elements are interactive HTML-blocks which can be embedded in a Jupyter Book using an iframe. An H5p element can be created in the [TU Delft portal on the H5p website](https://tudelft.h5p.com/content) (sign in via Brightspace to H5p required first). The iframe code can be copied at Edit - Publish - Public - Embed code. This html code can be directly added to your markdown file:

```html
<iframe src="https://tudelft.h5p.com/content/.../embed" aria-label="..." width="1088" height="200" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>
```

A full list of all available interactive elements is available on the website of [H5p](https://h5p.org/content-types-and-applications), these include among others:
- Multiple choice questions
- Fill in the blanks
- Drag and drop
- Interactive video
- Image hotspot

More information on H5p: [Teaching Support - Educational Tools - H5P](https://www.tudelft.nl/teaching-support/educational-tools/h5p)

## Example
Truss structures are modelled as rigid bars (so elements which cannot deform) connected by hinges (so elements can rotate with respect to one each other). In our model, hinges are indicate with a circle, and bars with a line. For example, the structure you've seen in the second example (with two diagonal bars removed) is modelled as follows:

```{figure} ../images/Truss1.svg
:name: truss structure

Bars and hinges in truss structure
```

Now that you've been introduced to truss structures, answer the following question:


<iframe src="https://tudelft.h5p.com/content/1291910926067816717/embed" aria-label="Modelling truss structures" width="1088" height="200" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>