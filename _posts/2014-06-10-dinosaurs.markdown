---
layout:     post
title:      "Tearing Down and Building New"

date:       2015-06-05 12:00:00
author:     "Josh Kingston"
header-img: 
---
As a financial analyst, we spend our entire time taking things apart and breaking them down into pieces. Building this blog and KC's parent website was an exercise in the exact opposite and a refreshing, creative change at creating something new. 

This blog will become home to the interesting insights that spawn from day-to-day work managing the investment fund at Kingston Carnegie. The fund is a long-equity, value investment fund. As a value investor, the time spent buying/selling is dwarfed many times by the hours invested into research and analysis. Along the way however, by-products of all the research are (admittedly rarely) insights and views that might appeal to the general public and not just financial analyst. 

Historically, when I came across something that I thought might be interesting to others, I made a personal facebook post about it. Whether out of pity for my tragic love of finance, or honest interest, these posts were well received. Shifting this media off facebook and onto a personal blog attached to the fund will give it a wider audience and allow me to be a bit more flexibility in the post content. 

Something off-top from finance, but immediately on my mind as I write this post is all the work that made this blog and KC's new website possible. I think value investors have to enjoy understanding how things work, so when the time came in early 2015 to update KC's website (originally built in 2011), I thought it might be enjoyable to learn to do it myself during the evenings and weekends. 

I originally looked at using some pre-existing packages like Squarespace or Wordpress, but they were not nearly flexible enough to do want I wanted for KC's investor portal and way overcooked for what I wanted for this blog. It started to be come clear to me that both websites would be written from scratch. Prior to all this, my background in coding was slim and none. Being a financial analyst, some capability with Microsoft Excel and its VBA language is unavoidable, but beyond that, I had zero training or knowledge in any programming language.

KC's original website was based on Ruby and written by a talented developer and great friend of mine, Jaryd Carolin. I figured that because the old website was written in Ruby, it would probably be best to make this the code of choice for the new re-build should I get stuck and need to cross check. 

It chewed up most of my spare time for months. I'd estimate it took about 300 hours to go from ground zero, no knowledge to having a simple, functional blog and a robust website for KC and its investors. I learned to use languages like Ruby, HTML5, CSS3, SASS, and Javascript. Coming out the other side, I think Ruby is a beautiful language and with its gem system, I don't think anyone who can watch a tutorial or use google should have fear of building a new web application.

All the development was done on Windows 8.1 and whilst there were occasional sticking points, it seemed a lot less painless than all the warnings you receive for avoiding developing on windows. I'd estimate that developing on Windows added maybe 5 extra hours of bugs to figure out.

For the tech-heads, this blog is a simple Jekyll blog built on Jekyll 2.4 with a Disqus javascript plugin for comments. It’s wearing a “Clean Blog” skin from StartBootstrap that I modified to KCs colours. Otherwise, it's dead, flat, static site. I think it's clean and simple compared to Wordpress's CDMS. Best of all, it's hosted for free at github pages. 

To the public, KC's website would look pretty static too, but to investors, there's a bit more going on behind the login portal. It's written in Ruby 2 on Rails 4 and snippets of Javascript to spice up the otherwise CSS3 presentation of the HTML5. Out the back, there's a single Postgres database holding tables like "users" and "prices", which together, let investors login and view their account details. Charts are handled by chartkick, a gem for google charts. Authentication and encryption is done with devise. Activeadmin lets me breeze in as a superuser and edit data tables directly, adding price updates and new investors. There's a paperclip gem handling PDF uploads pointing to a dropbox. A Sendgrid mailer handles automatic emails like password resets and Zerigo does all the DNS pointing. The entire thing is hosted at Heroku. 

Looking back, building these two sites was a very frivolous use of my time. I wanted to bring KC's public presentation up to a professional level and give investors some more functionality, but I was acutely aware that no amount amount of web coding would increase investor returns. I never let the development invade day-to-day financial work and relegated it to downtime in the evenings and weekends. The whole process was really satisfying and a great creative outlet. It was great to build something and a stark contrast to the work I do breaking things apart everyday as an analyst. 

<!---<h2 class="section-heading">The Final Frontier</h2>-->

<!---<a href="#">
    <img src="{{ site.baseurl }}/img/post-sample-image.jpg" alt="Post Sample Image">
</a>
<span class="caption text-muted">To go places and do things that have never been done before – that’s what living is all about.</span> -->

<!---subtitle:   "It's nice to create something for a change."-->