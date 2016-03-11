# Build a theme

wityCMS has a very simple files structure. You can have as many files and folders as you want in your theme, as long as a few required theme files are present.

## Getting started

The best point of reference is usually the default theme bundled with your wityCMS installation, since it’s always kept up to date, and it’s a fairly minimal theme. Just duplicate the folder, remove the CSS, and adjust markup as needed.

Alternatively, you can check out some themes made by the community, or create your own from scratch. It‘s up to you.

![](02-witycms-folders-theme.png)

## Required theme files

If you don't have these files, your theme won't work properly, or just won't show up at all. It's mandatory you have these files. 

* **templates/index.html**: The folder contain all the"*HTML*" index you need for the different theme page of your website.

EXEMPLE
Balise content

## Best practice 

### CSS Style

* **css**: The folder will allow to apply different "*HTML*" style element. They allow you to define any style property as the border , background color, typeface, the space between letters, etc. Through this method, all pages that reference the external style sheet will inherit all definitions.

**Font**

The Google Fonts API will generate the necessary browser-specific CSS to use the fonts. All you need to do is add the font name to your CSS styles. For example:

```css
font-family: 'Open Sans', sans-serif;
```

Here's an example. Copy and paste the following HTML into a file:

```html
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="https://fonts.googleapis.com/css?family=Tangerine">
    <style>
      body {
        font-family: 'Tangerine', serif;
        font-size: 48px;
      }
    </style>
  </head>
</html>
```

### Images 

* **img**: The folder contain all the asset you need to custom your theme like the logo, etc.



## Internationalize your theme

* **lang**: The folder contain all the translation you need to switch you theme between different languages.