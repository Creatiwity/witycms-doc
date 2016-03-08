# Pages

This is the essential application of wityCMS. If you want to make a website with lot of pages, the application "**Pages**" are here for. Each page created with the back-office is a web page.

## Pages list

The list contains all the pages created on your website. It gives you a rapid view of: 

* Title
* Author
* Views
* Date of the last modification 

![](pages-01.png)
The action button "**Edit**" allow you to *edit* or *delete* a page (according to permissions granted by your administrator).
![](pages-02.png)
## Create or edit page

If you want to add a page: Click on green button **"Add a page"**.

### Editing:

After clicking the button "**Add a page**" in the upper right of the back-office. You can write a new page.

![](pages-03.png)

* **Title***: Start by indicating the title of your page (less is better).
* **URL***: The URL will be automatically generated with the information you fill in the title form. If you want, you can change this URL.
* **Content**: Thanks to **[CKEditor](http://docs.ckeditor.com/)** you are able to write, layout your news and add some pictures and videos as desired.

### Details:

On the side, you find the details information about your current page:

* **Author**: by default the author is the name of the account with which you are log in. Moreover, you can edit yourself the author as desired.
* **Subtitle**: use for *SEO*.
* **Image**: You can upload a main image for your page (use like header / page preview etc., that depends of your template).

### SEO:

Meta tags, Title and Link are "**html**" tag inserted in the ```<head >``` section of a web page (before the ```<body>```. 

They help to provide "*guide*" for the search engines, social networks and other systems using "*metadata*". The information in these tags are not visible on your website, but appear in the source code of the page.

* **Meta title**: by default is the name of your page
* ** Meta description**:

### Submit your page:

* **Submit**:
* **Cancel**:

## Index your page

To index your page to your "*navbar*" (navigation bar / menu), you need to open your FTP client (e.g: FileZilla). 

Open the folder containing website sources:

1. "**Themes**" folder
2. Name of your theme (here "***grafx***") 
3. **Templates**
4. Download the **index.html** 

![](pages-04.png)

5. Open it with an text editor (e.g: [**Sublime Text**](https://www.sublimetext.com/))
6. Add the name of your new page like this
```
<ul class="nav navbar-nav">
    <li><a href="/"><span>{lang Home}</span><br />
        <em>{lang starting page}</em></a></li>
    <li><a href="/about"><span>{lang About}</span><br />
        <em>{lang the company}</em></a></li>
    <li><a href="/services"><span>{lang Services}</span><br />
        <em>{lang our skills}</em></a></li>
    <li><a href="/portfolio"><span>{lang Portfolio}</span><br />
        <em>{lang our works}</em></a></li>
    <li><a href="/news"><span>{lang Blog}</span><br />
        <em>{lang latest posts}</em></a></li>
    <li><a href="/contact"><span>{lang Contact}</span><br />
        <em>{lang send us an email}</em></a></li>
</ul>
```


