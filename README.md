![](wityCMS-logo.png)

wityCMS is a lightweight Content Management System (CMS) in PHP, Model-View-Controller oriented.

This CMS uses its own templating system, named [WTemplate](https://github.com/Creatiwity/WTemplate), developed as [a separate GitHub project](https://github.com/Creatiwity/WTemplate) but included here as a submodule.

## Installation

### Minimum requirements

* An **Apache server** with PHP 5.3+, *mod_rewrite* enabled and .htaccess files allowed;
* A **SQL server**, like *MySQL* or *MariaDB*, with a database available;
* A **FTP client**, like [FileZilla](https://filezilla-project.org/), to upload the **wityCMS** files;
* Download the latest version of **wityCMS**: [zip](https://github.com/Creatiwity/wityCMS/archive/0.5.0.zip).

### Let's go

1. **Unzip** and **copy** wityCMS files on your web server using FileZilla.
2. Open a navigator and **go to the URL** of your web server.
3.  On the **installation page**, you will be asked to give information about your server and your admin account. Fill in all the required fields until all the tabs are marked as valid.
4. **Click** on "Launch install".
5. **Congratulations!** wityCMS has just generated its configuration files (in `system/config`), created all its tables in the database and inserted the first user (you!) as an administrator. The system is ready to be used.
