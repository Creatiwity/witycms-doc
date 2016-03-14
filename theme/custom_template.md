# Overriding application template

For each application ***Page*** you want to customize you need to create a new file with this specification : 

By default each action of each app has a template, but if you want to overwrite one of them, you'll need to create a new **`HTML`** file.

![](images/02-folders-theme-app.png)

To find out how to name your **`HTML`** file select the app file (e.g: News) located in `/apps/news/front/templates/listing.html`.

![](images/02-folders-theme-news.png)

Once you know how to name the file (e.g: News -> `listing.html`), you can create a new file located in `/theme/theme_name/templates/news`. Now you can drop your `listing.html` to override the one contained in the `apps` folder.

