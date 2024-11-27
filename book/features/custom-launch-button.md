# Sphinx Extension: Custom Launch Button 

The custom launch button extension allows you to create a customizable button in the top right of your jupyter book. 
This may have many applications, one of them being that you can create different language versions of the book available for the user. 

This section will explain how to create a "Languages" button, like you might be used to seeing on just about any website. The use of the button, however, is completey customizable and may be used in many different ways.

## Installation

1. Install the Sphinx Launch Buttons extension from the GitHub repository.

`pip install git+https://github.com/TeachBooks/Sphinx-launch-buttons.git`

2. To use the extension in your book, you need to include it in your `_config.yml` file.

```
sphinx:
  extra_extensions:
    - custom-launch-buttons
```

3. Then you need to include a `_launch_buttons.yml` file in the same location as your `_config.yml` file. 

```
buttons:
  - type : dropdown

  - type : button
```

Where `buttons` is an array of launch buttons, each can be identified using 2 types: 'dropdown' or 'button'. The cell above shows 2 buttons, one of type `dropdown` and one of type `button`.

The button/dropdown can be visualised using either an [svg icon](https://icons.getbootstrap.com/#icons) or text.

```
buttons:
  - type : dropdown
    label: Language
  - type : button
    label : <svg></svg> 
```

## Setting up your repository

For the implementation to your book, it is handy to create a branch for each language version you want to offer. Make a new branch using for example main as a source. Assuming we want to create a dutch version of you can call this branch `Dutch` or `Nederlands`. 

You will then need to translate the content in the dutch branch to dutch which can take some time. From experience, [DeepL](https://www.deepl.com/en/translator) is a good tool for this but any AI chatbot might be helpful as well. Make sure to proofread the translation.



## 