# Custom template

WTemplate is the template engine used by WityCMS.
If you want to modify the theme you need to respect all the restriction imposed by WTemplate. 

For each application page you want to customize you need to create a new file with this specification : 

##Applications theme
TOPO sur les apps... lorem ipsum

### Conatct

1. "template_name"
2. "templates"
3. "contact"
4. Create you file **form.html**

### News

1. "template_name"
2. "templates"
3. "news"
4. Create you file **listing.html**

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
4. Create you file **form.html**

### Slideshow

1. "template_name"
2. "templates"
3. "slideshow"
4. Create you file **block.html**

### Team

1. "template_name"
2. "templates"
3. "team"
4. Create you file **members.html**

### User

1. "template_name"
2. "templates"
3. "user"
4. Create you file **register.html** // **password_lost.html** // **connexion_form.html** // **reset_password.html**

## Font

Here's an example. Copy and paste the following HTML into a file:

```
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

## Onepage theme 