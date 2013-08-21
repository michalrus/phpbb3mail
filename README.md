phpbb3mail
==========

Perl mail notifications for your new unread posts of a phpBB3 site.
----

What this script simply does is send *one* e-mail message for each found unread post. For phpBB3 to track your unread posts, you need to have an account on a chosen site.

Furthermore, messages for posts of one thread are *grouped together* by means of `References:` and `In-Reply-To:` mail headers. This approach renders *conversations* in Gmail.

It will also inform you *once* when the site goes down and *once* when it's back.

Tested successfully "in production" with [Stosowana.pl board](http://www.forum.stosowana.pl/).

How to install
----
1. Clone this repo: `$ git clone https://github.com/michalrus/phpbb3mail.git`.
1. Copy `config.cfg.sample` to `config.cfg` and modify it to suit your needs.
1. Test `./run`, install missing Perl modules if any (on Debian-like system the ones you might not already have are `libdbi-perl`, `libwww-perl`, `libnet-smtp-ssl-perl`, `libbytes-random-secure-perl`).
1. Add `./run` to your crontab: `$ crontab -e` and append something like `* * * * * /your/path/to/phpbb3mail/run` to it.

Bugs
----

Pull request are welcome if this doesn't work with your chosen site.

Licensing
----

Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).


Screenshots
----

![phpbb3mail Gmail screenshot][1]


  [1]: http://i.stack.imgur.com/48m2K.png
