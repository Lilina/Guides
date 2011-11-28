## Getting Started
This guide is designed to run through getting Lilina set up, and getting
you reading your feeds.

By the end of this guide, you should have Lilina installed and have your
first feeds all ready to go.

### Before We Start
Before we start, we need to make sure that you're actually able to run
Lilina. If you can't, the rest of the guide is useless!

If you are unsure about any of the below, download and run Lilina and
the installer will inform you if you meet these requirements.

#### Minimum Requirements
* [PHP](http://php.net/) 5.2 or higher
* PHP's [XML extension](http://php.net/xml) (enabled by default)
* PHP's [PCRE extension](http://php.net/pcre) (enabled by default)
* PHP's [JSON extension](http://php.net/json) (enabled by default)

#### Recommended
* Both PHP's [multibyte string extension](http://php.net/mbstring) *and*
  [iconv extension](http://php.net/iconv)
* PHP's [cURL extension](http://php.net/curl) (disabled by default)
* PHP's [Zlib extension](http://php.net/zlib) (disabled by default)

### Installing Lilina
The first proper step to getting started with Lilina is actually
installing it.

These instructions do not cover [installation of plugins][installplugin]
or [installation of templates][installtemplate], which have their own
separate guides. These instructions also do not cover [upgrading to
the latest version][upgrading].

[installplugin]: /plugin_installation
[installtemplate]: /template_installation
[upgrading]: /upgrading

#### Download Lilina
[Download the latest version](http://getlilina.org/download/) of Lilina.
As of the writing of this document, 1.0-bleeding is the latest
stable version.

<div class="note" markdown="1">
If you'd prefer to keep up to date with the very latest features as
they're developed, try the development or nightly archives.
</div>

#### Uploading
Launch your FTP program, and browse into the web-accessible root
directory of your site. Extract the `lilina/` directory from the archive
you downloaded in step 2 and upload it to this directory.

<div class="note" markdown="1">
This document assumes that you're installing to `/public_html/lilina/`,
which is accessible from the web from `http://example.com/lilina/`. You'll
need to adjust these to your own server settings.
</div>

#### Setting Permissions
The `content/` directory is used by Lilina to store all configuration,
plugins and templates. In order for Lilina to be able to use this directory,
you need to make it writable by the server.

Making this directory writable changes depending on how your host is set
up. Typical settings for this directory are to `chmod` the directory and
subdirectories to 755, 775 or 777.

<div class="warning" markdown="1">
Setting this to 777 will enable any user to modify the files. Only do
this if you're on a dedicated server, or if you must.
</div>

<div class="note" markdown="1">
After installation, you may want to remove the write permissions on
`content/system/config/settings.php` for security. This file contains
only your authentication information and the base URL for the installation,
and Lilina does not need to change this file after installing.
</div>

#### Installation

Head to your Lilina installation in your browser
(e.g. http://example.com/lilina/). Follow the in-browser installation
process to complete the installation.

### Adding Feeds
So now that you have Lilina installed, it's time to start adding feeds.

Let's say you want to add CNN's feed. You can do this in one of a few
different ways.

#### Bookmarklet
Grab the bookmarklet off the admininistation panel, and drag it to your
bookmark toolbar. Then, head over to the site you want to add, and click
the bookmarklet.

A handy window will appear which will allow you to confirm adding the
feed. If more than one feed is on the site, you'll be able to pick
which one you'd like.

#### Admin Panel
Head into the admin panel and click through to the Feeds page. At the
bottom, you'll find the add feed form.

Simply type in the URL to the site, or to the feed directly, and you'll
add it.

For example, for CNN, we could type in `cnn.com`, `http://cnn.com/`,
or `http://rss.cnn.com/rss/edition.rss`

#### Via Your Template
Some templates include a subscription panel of their own. For those,
you won't even need to touch the administation panel.

This changes depending on which template you're using, so check the
documenation for the template on how to do that.

### Extending
So, you've gotten your installation loaded up with your feeds. The next
step is to make Lilina your own. One of the great strengths of Lilina
is the ability to add and remove functionality with plugins.

Managing your plugins is done via the administration panel. Simply click
through to the Plugins section, and you'll see your currently available
plugins. By clicking the Activate link for a plugin, you will enable
that plugin and its functionality.

These plugins included with Lilina are some of our favourites, but there
are many more available on the [plugin
repository](http://extend.getlilina.org/). To use these, simply download
them and extract into your `content/plugins/` directory. They will then
appear in your administration panel.

### Reading
Now that everything is set up, it's time to start using Lilina!

Depending on which template you're using, this can be different, so
refer to the documentation included with it.

Thanks for sticking with it. Have fun, and happy reading!