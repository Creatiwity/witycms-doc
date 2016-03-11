# Build a theme

wityCMS has a very simple files structure. You can have as many files and folders as you want in your theme, as long as a few required theme files are present.

The best point of reference is usually the default theme bundled with your wityCMS installation, since it’s always kept up to date, and it’s a fairly minimal theme. Just duplicate the folder, remove the CSS, and adjust markup as needed.

## Required theme files

It's mandatory you have the templates folder with the index.hmtl.
If you don't have these files, your theme won't work properly, or just won't show up at all.  

![](02-folders-template.png)

Templates folder contain all the"*.html*" index you need for the different theme page of your website.

```html
<body>
    <div class="container">
        <header class="theme-header">
            <img src="/themes/grafx/img/logo.png" alt="logo" />
            <div class="inner">
                <p class="site-name">{$wity_site_title}</p>
            </div>
            <div class="clear"></div>
        </header>

        <nav class="navbar" role="navigation">
            <div class="container-fluid">
                <div class="navbar-header">
                    <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                        <span class="sr-only">{lang Toggle navigation}</span>
                    </button>

                <div class="collapse navbar-collapse">
                    <ul class="nav navbar-nav">
                        <li><a href="/"><span>{lang Home}</span><br />
                            <em>{lang starting page}</em></a></li>
                        <li><a href="/about"><span>{lang About}</span><br />
                            <em>{lang the company}</em></a></li>
                        <li><a href="/services"><span>{lang Services}</span><br />
                            <em>{lang our skills}</em></a></li>
                        <li><a href="/portfolio"><span>{lang Portfolio}</span><br />
                            <em>{lang our works}</em></a></li>
                        <li><a href="/team"><span>{lang Team}</span><br />
                            <em>{lang our members}</em></a></li>
                        <li><a href="/news"><span>{lang News}</span><br />
                            <em>{lang latest posts}</em></a></li>
                        <li><a href="/contact"><span>{lang Contact}</span><br />
                            <em>{lang send us an email}</em></a></li>
                    </ul>

                    <form class="navbar-form navbar-right" role="search" action="/search" method="get">
                        <div class="form-group">
                            <input type="text" name="query" class="form-control" placeholder="{lang Search the website}" size="30" />
                        </div>
                        <button type="submit" class="btn btn-default"><span class="glyphicon glyphicon-search"></span></button>
                    </form>
                </div><!-- /.navbar-collapse -->
            </div>
        </nav>

        <div class="row">
            <div id="column-content" class="col-md-8">
                <div class="block">
                    {$notes}
                    {$include}
                </div>
            </div>

            <div id="column-blocks" class="col-md-4">
                {if !{$wity_user}}
                <aside id="grafx-user" class="block block-user">
                    <p class="text-center buttons">
                        <a class="button-register" href="#grafx-register" data-toggle="collapse" data-parent="#grafx-user">{lang Sign up} <img src="/themes/grafx/img/sign-in.png" alt="Sign in" /></a>
                        <a class="button-login" href="#grafx-login" data-toggle="collapse" data-parent="#grafx-user"><img src="/themes/grafx/img/login.png" alt="Login" /> {lang Login}</a>
                    </p>
                    <div class="panel">
                        <div id="grafx-register" class="register collapse">
                            {retrieve_view user/register}
                        </div>
                        <div id="grafx-login" class="login collapse">
                            {retrieve_view user/login}
                        </div>
                    </div>
                </aside>
                {else}
                <aside class="block block-user text-center">
                    <p>{lang welcome_user|{$wity_user_nickname}}</p>
                    <p><a href="/user/logout/">{lang Logout}</a>{if !empty({$wity_user_access})} - <a href="/admin/">{lang Administration}</a>{/if}</p>
                </aside>
                {/if}
            </div>
        </div>

        <footer class="text-center">
            <p>{$wity_site_title}&copy; 2016<br />
                {lang All rights reserved.}</p>
        </footer>
    </div>
</body>
```

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