# File Structure

wityCMS has a fairly loose file structure — you can have as many files and folders as you want in your theme, as long as a few required theme files are present.

## Required theme files
If you don’t have these files, your theme won’t work properly, or just won’t show up at all. It’s vital you have these files.

### about.txt
This text file holds the basic details about your theme. For example:

* Theme Name: Grafx
* Theme URI: https://creatiwity.net
* Description: Theme for wityCMS
* Author: Creatiwity
* Author URI: https://creatiwity.net
* Version: 1.1.0

### Style.css

### Img

### Lang

### Templates

## WTemplate

### WTemplate.php

WTemplate is the template engine used by wityCMS.

### WTemplateCompiler.php

WTemplateCompiler compiles the nodes used in the templates parsed ba WTemplate.

### WTemplateFile.php

WTemplateFiles is the template file manager.

### WTemplateParser.php

WTemplateParser is the part of WTemplate.