---
layout:     post
title:      "Tearing Down and Building New"
date:       2015-06-05 12:00:00
author:     "Josh Kingston"
comments: true

---
Financial analysts spend all their time taking things apart and breaking them down into pieces. We don’t create things, we dismantle them. Building this blog and KC's parent website was an exercise in the exact opposite and a refreshing, creative change at creating something new. 

This blog will become home to the interesting insights that spawn from day-to-day work managing the investment fund at Kingston Carnegie. The fund is a long-equity, value investment fund. As a value investor, the time spent buying/selling is dwarfed many times by the hours invested into research and analysis. Along the way however, by-products of all the research are (admittedly rarely) insights and views that might appeal to the general public and not just financial analysts. 

Historically, when I came across something that I thought might be interesting to others, I made a personal Facebook post about it. Whether out of pity for my tragic love of finance, or honest interest, these posts were well received. Shifting this media off Facebook and onto a personal blog attached to the fund will give it a wider audience and allow me a bit more flexibility in the post content. 

These blog posts will be financially focussed, but right now as I put this very first post together, all the work that went into getting this blog and KC’s parent website operational is more immediately on my mind. I think value investors have to enjoy understanding how things work, so when the time came in early 2015 to update KC's website (originally built in 2011), I thought it might be enjoyable to learn to do it myself during the evenings and weekends. 

I originally looked at using some pre-existing packages like Squarespace or Wordpress, but they weren’t nearly flexible enough to do what I had envisioned for KC's investor portal and way overcooked for what I wanted for this blog. It started to become clear to me that both websites would be written from scratch. Prior to all this, my background in coding was slim to none. Being a financial analyst, some capability with Microsoft Excel and its VBA language is unavoidable, but beyond that, I had zero training or knowledge in any programming language.

KC's original website was based on Ruby and written by a talented developer and great friend of mine, Jaryd Carolin. I figured that, because the old website was written in Ruby, it would probably be best to make this the code of choice for the new re-build should I get stuck and need to cross check. 

Learning to code and building KC’s website chewed up most of my spare time for months. I'd estimate it took about 300 hours to go from ground zero, no knowledge, to having a simple, functional blog and a robust website for KC and its investors. I learned to use languages like Ruby, HTML5, CSS3, SASS, and Javascript. Coming out the other side, I think Ruby is a beautiful language. With Ruby’s gem system, a way of plugging in code to provide powerful functionality, I don't think anyone who can watch a tutorial or use google should have fear of building a new web application. It’s a modern version of Lego, complete with the feeling of satisfaction when you step back and look at your creation.

All the development was done on Windows 8.1 and whilst there were occasional sticking points, it seemed a lot less painless than all the warnings you receive for avoiding developing on Windows. I'd estimate that developing on Windows added maybe 5 extra hours of bugs to figure out.

For the tech-heads, this blog is a simple Jekyll blog built on Jekyll 2.4 with a Disqus javascript plugin for comments. It’s wearing a “Clean Blog” skin from StartBootstrap that I modified to my tastes. I also added some simple social share buttons at the bottom of each post. Otherwise, it's a dead, flat, static site. I think it's clean and simple compared to Wordpress, which has grown into being a being a full-blown content management system. Best of all, this blog is hosted for free at github pages. 

To the public, KC's website would look pretty static too, but to investors, there's a bit more going on behind the login portal. It's written in Ruby 2 on Rails 4 with snippets of Javascript to spice up the otherwise CSS3 presentation of the HTML5. Out the back, there's a single Postgres database holding tables like "users" and "prices", which together, let investors login and view their account details. Charts are handled by chartkick, a gem for google charts. Authentication and encryption is done with devise. Activeadmin lets me breeze in as a superuser and edit data tables directly, adding price updates and new investors. There's a paperclip gem handling PDF uploads pointing to a dropbox. A Sendgrid mailer handles automatic emails like password resets and Zerigno does all the DNS pointing. The entire thing is hosted at Heroku. 

Looking back, building these two sites was a very frivolous use of my time. I wanted to bring KC's public presentation up to a professional level and give investors some more functionality, but I was acutely aware that no amount of web coding would increase investor returns. I never let the development invade day-to-day financial work and relegated it to downtime in the evenings and weekends. The whole process was really satisfying and a great creative outlet. It was fantastic to build something and a stark contrast to the work I do breaking things apart everyday as an analyst.