# phplist3_php53
phpList v3 for PHP v5.3.x

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

## Installation
See file: docs/INSTALL

## Upgrade
See file: docs/UPGRADE

## Security
See file: docs/README.security

## Languages
In the directory `public_html/lists/texts` you will find existing translations of the public
pages of PHPlist. You can use them in your config file to make the frontend of the system
appear in the language of your choice.

In the config file there are a lot of choices to make about your particular
installation. Make sure to read it carefully and step by step work your way through
it. A lot of information is provided with each step.
