Mautic WordPress plugin
=======================

[Mautic](http://mautic.org) [Wordpress Plugin](https://wordpress.org/plugins/wp-mautic/) inserts Mautic tracking image and forms to the WP website. Your Mautic instance will be able to track information about your visitors that way.

## Installation

1. Download ZIP package form right column of [this](https://github.com/mautic/mautic-wordpress) page.
2. At your WP administration go to Plugins / Add New / Upload plugin.
3. Select the ZIP package you downloaded in step 1.
4. Go to Plugins and enable WP Mautic plugin.
5. Go to Settings / WPMautic and fill in the Base URL of your Mautic instance.

## Usage

### Mautic Tracking Image

Tracking image works right after you finish step 5 of Installation above. That means it will insert 1 px gif image loaded from your Mautic instance. You can check HTML source code (CTRL + U) of your WP website to make sure the plugin works. You should be able to find something like this:

```html
<img src="http://yourmautic.com/mtracking.gif" />
```

Plugin adds more information (current url, referal url, page title, user language) to the image URL query encoded in base 64 (not humanly readable). This way your Mautic instance receives more valuable data.

### Mautic Forms

To load a Mautic Form to your WP post, insert this shortcode to the place you want the form to appear:

```
[mauticform id="1"]
```

Replace "1" with the form ID you want to load. To get the ID of the form, go to your Mautic, open the form detail and look at the URL. The ID is right there. For example in this URL: http://yourmautic.com/s/forms/view/3 the ID = 3.
