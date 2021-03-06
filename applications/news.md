# News

***News*** application lets you manage a collection of articles or posts ordered by publication date and sorted by categories.

Using ***News*** application is helpful if you want to create and manage your site's news, like a blog.

## News listing
![](../images/news-listing.png)
The list contains all news created on your website. It gives you an overview of:

* The title
* Author
* Category it belongs
* State of publication
* The number of views
* The last modification date

For each news you can edit or delete it using the action button at the end of the row.
Moreover you can add a news by clicking the **Add a news** button.

![](../images/news-button.png)

## Create and edit news

### Edition

After clicking the button **Add** or **Edit** a news, you can write the content:

![](../images/news-listing-empty.png)

* **Title***: Start by indicating the news title *(it cannot exceed 140 characters)*.
* **URL***: The URL will be automatically generated with the information you filled in the title form. If you want, you can change this URL.
* **Content**: with **[CKEditor](http://docs.ckeditor.com/)** you are able to write, layout your news and add some pictures and videos as you wish.

### Details

On the right side, you have the details about your current news:

* **Published**: yes / no (this enables you to write news without publishing it on your website).
* **Date of publication***: automatically filled. You can also edit the date of publication.
*  **Hour of publication***: automatically filled. You can edit the time of publication.
* **Author**: by default the author is the name of the account with which you are logged in. You can change the author.
* **Image**: You can upload a main image (used like header / news preview etc., depending on your template, it cannot exceed 2 MB).

### Categories

Categories enable to classify your news according to the news content.

The configuration of categories will be explained later.

### SEO

The `Title` and `Description` meta tags are **`HTML`** tags inserted in the `<head>` section of a web page (before the `<body>`).

They help you to provide information for the search engines, social networks and other systems using *metadata*. The information on those tags are not visible on your website, but it appears in the source code of the page.

* **Meta title**: by default it is the news name
* **Meta description**: Input a short description of your news (optional). 125 characters maximum.

### Post your news

To finalize the edition of your news, click on **Submit** button.

## Categories

wityCMS offers you the possibility to sort your news in different categories according to the content.

This list includes all the categories and gives you the name, shortname and the parent category, if any.

![](../images/news-categories.png)
You must click on the green button **Add a category** to create a new category.

![](../images/news-categories-add.png)

* **Name**: fill with the name of your category (e.g: Geek)
* **Shortname**: specify a "shortname" if you want (e.g: geek)
* **Parent**: specify if it is a sub category (e.g: Game)
* **Actions**: *create* or *abandon*

A notification inform you that *The category **Geek** was successfully created*.
![](../images/news-categories-add-success.png)
You can also delete a category when you want with the action button **Delete**.
![](../images/news-categories-buttons.png)
To confirm deletion, a pop-up appear asking you: *Do you really want to delete this category?*.
If you are certain, click on **Delete** if not click on **Cancel**.
![](../images/news-delete-confirm.png)
After your deletion, a notification appears to inform you that the *Category [was] successfully deleted*.
![](../images/news-delete-success.png)
