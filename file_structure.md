# File Structure

wityCMS has a fairly loose file structure — you can have as many files and folders as you want in your theme, as long as a few required theme files are present.

## Required theme files
If you don’t have these files, your theme won’t work properly, or just won’t show up at all. It’s vital you have these files (at least).

### about.txt
This text file holds the basic details about your theme. For example:
Theme name: Default
Description: This is the default, shiny theme for Anchor CMS.
Author name: Visual Idiot
Author site: http://visualidiot.com
License: http://licence."...".com

### 405.404.php
When a post, page or article is not found, this template will be used.

### article.php
The generic single post template. Used on single post/article pages.
This template is customisable.
You can have custom article templates by appending the article slug to the file name, such as article-this-is-my-article.php.

### page.php
The generic page template.
This template is customisable
You can also have custom page templates by appending the page’s slug to the file name, such as page-this-is-my-page.php.

### posts.php
This is the blog listing (and usually the index) template for your site. Used in conjunction with the loop to show the latest posts.

### functions.php
This is where you can customise fragments of content by placing your own helper functions in this file and calling them in your templates.
Optional theme files

### header.php
The very first part of your theme. Included at the very start of every template, and is used to start a HTML document (the <!doctype HTML> bit).

### footer.php
The opposite to header.php; included at the end of every template, and is normally used to close the document and insert any tracking/analytics code, or external JavaScript.

### search.php
This template shows the results for a user’s search. Used in conjunction with the loop to show the search results.
