---
layout: post
title:  "Paperboy"
date:   2015-02-15 13:47:20
picture: images/zeitung.jpg
---

# Goal

The goal of this project is to use the excelent news wrapper from [calibre](http://calibre-ebook.com/) on a server. This service allows to define jobs to generate ebooks from your favorite website on a regular basis, which you can define via an download scedule. If you have an Kindle like i do, you can also let calibre send you the generated ebook. The problem is that you alway have to keep calibre running to automatically receive the updates.

As i am a verry lazy person, i tend to forget to keep calibre up and running all the time. So i had the idea to use a server. But to run calibre on a server you have to install an X server and VNC to connect to it. This all makes the server verry slow and it is quite tideous to handle it.

The good news is that there is the possibility to generate the ebooks for the websites via the commandline. All you need is the "ebook-convert" command with the recipe reference and an output path.

{% highlight console %}
    ebook-convert guardian.recipe guardian.epub
{% endhighlight %}
    
This excample creates an epub version of the guardian webpage. So you can use this command plus "calibre-smtp" to send the book to your Kindle. You only have to install calibre on your server write a script with you desired recipe and have it executed in a cron job.

But as i said i am a lazy person and my interests shift from time to time. So that i dont like to always have to search the recipe names, change the script and configure the cron jobs. Therefore I want to create a webpage and a service which handles all this stuff.

