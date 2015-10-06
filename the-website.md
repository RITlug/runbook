# The Website
RITlug's website is powered by Github pages and stored in a repository in the RITlug Github organization.
It is powered by vanilla Jekyll (no plugins) as Github pages does not allow plugins for security reasons.
In order to update any aspect of the site, simply push or merge changes to the repository and the
changes will take effect within a few minutes.

Announcements
------------------
This is a quick rundown of how to post an announcement on the RITlug website. See also [Announcements](announcements.md).

* Fork the repository to your own Github account (go to the RITlug repository and click "fork")
* Clone the repository locally (if desired - you can also create it online)
* Create a new file in announcements/_posts named with the convention 2015-10-02-new-website.md
* Add front matter to the file

        ---
        title: title of your announcement
        author: your name
        date: date, in the format 2015-10-03
        tags: [a, list, of tags] (optional)
        layout: post
        ---

* Add a blank line, then type your announcement
* Add the new file to git
* Git commit
* Git push to your repository
* Open a pull request against the master branch (which is default) of the RITlug copy of the repository
* When your pull is merged, the site will update within a few minutes

Talks
------------------
This follows the same process as announcements, with a couple of small tweaks:

* The files will be put in talks/_posts
* There is an extra line in the frontmatter called 'slides' which provides a link to where
the slides for the talk can be viewed. This should be a URL, usually along the lines of /talks/your-talk-name.pdf
if hosted on the RITlug site
* The slides (if hosted on the RITlug site) should be put in the talks folder, prefaced with the year and semester.
Something like 2015-fall-<your title>
* If hosted on the RITlug site, the slides should also be committed

Site Source
------------------
This is the structure of the source code for the site, e.g. where to find anything.
Most of the structure should be pretty self explanatory.

The site uses Google's [Material Design Light template](http://getmdl.io), version 1.0. The javascript is patched to allow
for linking to other pages in the tab bar - a feature which should be built in in version 1.1.

The site follows a fairly typical Jekyll setup so you can refer to the Jekyll documentation.

Pointer: You can access announcements from within templates using {{ site.categories.announcements }} and talks
using {{ site.categories.talks }}.

<pre>
├── about.md - the about page (at /about.html)
├── announcements
│   ├── index.html
│   └── _posts - all announcements posted on the site, in markdown format
├── _config.yml
├── connect.html
├── css
│   ├── material-brown-orange.css
│   └── styles.css
├── feeds
│   └── latest.xml - ATOM feed
├── img
│   └── ritlug.png
├── _includes - sections of the template. These are files included in templates in the _layouts directory.
├── index.html
├── js
│   └── material.js
├── _layouts - Available layouts. These are referred to in the pages themselves.
│   ├── default.html
│   ├── page.html
│   └── post.html
├── LICENSE
├── README.md
├── schedule.md
└── talks
    ├── index.html
    └── _posts - Talks posted on the site, in markdown format
</pre>

Developing and Previewing
----------------------
[Refer to the README in the site repository](http://github.com/ritlug/ritlug.github.io)
