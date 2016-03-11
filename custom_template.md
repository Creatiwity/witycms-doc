# Custom template

"**WTemplate**" is the template engine used by wityCMS.
If you want to modify the theme you need to respect all the restriction imposed by "**WTemplate**". 

For each application page you want to customize you need to create a new file with this specification : 

## Overriding application template

By default each app have a theme but if you want to overwrite, process like this : 

### News

1. "template_name"
2. "templates"
3. "news"
4. Create your file **listing.html**

## Font

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