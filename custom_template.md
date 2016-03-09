# Custom template

WTemplate is the template engine used by wityCMS.
If you want to modify the theme you need to respect all the restriction imposed by WTemplate. 

For each application page you want to customize you need to create a new file with this specification : 

##Applications theme

By default each app have a theme but if you want to overwrite to process like this : 

### Conatct

1. "template_name"
2. "templates"
3. "contact"
4. Create your file **form.html**

### News

1. "template_name"
2. "templates"
3. "news"
4. Create your file **listing.html**

### Newsletter

1. "template_name"
2. "templates"
3. "newsletter"
4. Create you file **add.html**

### Pages

1. "template_name"
2. "templates"
3. "pages"
4. Create you file **display.html**

### Search

1. "template_name"
2. "templates"
3. "search"
4. Create your file **form.html**

### Slideshow

1. "template_name"
2. "templates"
3. "slideshow"
4. Create your file **block.html**

### Team

1. "template_name"
2. "templates"
3. "team"
4. Create your file **members.html**

### User

1. "template_name"
2. "templates"
3. "user"
4. Create your files **register.html** // **password_lost.html** // **connexion_form.html** // **reset_password.html**

## Font

The Google Fonts API will generate the necessary browser-specific CSS to use the fonts. All you need to do is add the font name to your CSS styles. For example:

```font-family: 'Open Sans', sans-serif;
```

Here's an example. Copy and paste the following HTML into a file:

```<html>
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