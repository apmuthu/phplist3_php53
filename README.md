# phplist3_php53
phpList v3 for PHP v5.3.x

[![Build Status](https://travis-ci.org/phpList/phplist3.svg?branch=master)](https://travis-ci.org/phpList/phplist3)

[![StyleCI](https://styleci.io/repos/32042787/shield)](https://styleci.io/repos/32042787)

* This version starts by keeping track of phplist v3.x releases
* The original project is at [SourceForge](https://sourceforge.net/projects/phplist/) - their [commercial offering](http://www.phplist.com)
* It is being developed at [GitHub](https://github.com/phpList/phplist3)
* Retention of compatibility with **PHP 5.3.x** is pursued in this repo
* This distribution is served under the [GPL v3.0 license](https://www.gnu.org/licenses/gpl-3.0-standalone.html).

---

## What is phpList

phpList is a set of PHP pages that implement a simple mailinglist system. It uses MySQL for storing the information.

Particular aspects of the system are:

* Posting to the mailinglist is via a webpage. It is therefore more a kind of "announcements" list system than an actual email mailinglist.
* It is designed to be able to deal with a very large amount of email addresses.
* Users can sign up to multiple lists. If a message is sent to multiple lists, they will only receive one copy of the email and not as many as the number of lists they are subscribed to.
* Geographical information. If people sign up, they can identify the geographical location they're in and when sending an email you can determine which locations need to receive the message.
* Personalised emails. You can specify "variables" in your emails, which will at send time be replaced by the appropriate values for specific to the email recepient.

---

## Requirements
To use phpList you need a webserver which supports PHP version 5, and a MySQL database.

phpList should work with a standard PHP environment, but some functionality may require additional modules. 

More detailed requirements can be found in the [Reources Wiki](https://resources.phplist.com/system)

## Installation
Read the installation instructions with abundant help at: 

https://www.phplist.org/manual/ch028_installation.xhtml

## Upgrade

phpList upgrade process.

How to upgrade from any previous version to the latest version

Step 1. BACKUP your database
(e.g. # mysqldump -u[user] -p[password] [database] > phplist-backup.sql)

Step 2. Copy your old configured files to some safe place

These files are:
	lists/config/config.php
        possibly lists/texts/english.inc or any other language.inc if you have edited it

Step 3. Copy the files from the tar file to your webroot.

You can copy everything in the "lists" directory in the tar file to your website.
To facilitate future upgrades, ie to make it easier for you to simply copy
everything I have now put the "configurable" files in their own directory. They
reside in "lists/config". This is hopefully going to be the directory thay you can
keep between upgrades, and that will contain the only information that you want
changed in order to make it work for your own site.

Step 4. Copy your configuration files to lists/config or re-edit the new config file
sometimes new features are added to the config file, so it's better to use
the new config file and re-adapt it to your situation.

I have put an example .htaccess file in this directory. You should not allow
access to this directory from the webserver at all. The example will work with
apache.

You can overwrite the files that are there. They are example files.

Step 5. Go to http://yourdomain/lists/admin/ and choose the Upgrade link

Step 6. Click the link in this page.

This process may take quite a while if your database is large. Don't interrupt it.

## Languages
In the directory `phplists/lists/texts` you will find existing translations of the public
pages of phpList. You can use them in your config file to make the frontend of the system
appear in the language of your choice.

In the config file there are a lot of choices to make about your particular
installation. Make sure to read it carefully and step by step work your way through
it. A lot of information is provided with each step.
