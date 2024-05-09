---
draft: false 
date: 2017-12-23
lang: en
categories:
  - Web
authors:
  - guigur
---

![Banner](myfriends2_banner.png)

## A short summary

Myfriends2.fr is an ancient website of mine from the years 2013-2014.
It was the website of  MyAppleFr's Minecraft server.
<!-- more -->

## Features

Among other things, you could:

- Sign-up by redeeming a token sent by private message on the Minecraft server. (to avoid having your account stolen)
- Consult the server's news.
- Post in-game images on the "Portfolio" board
- React with comments to articles and Portfolio's pictures.
- Guide yourself wif the Dynmap of the server.
- Buy items in the online shop (but sadly, this feature was never finished :/)

## Security problems and pitfalls

Being coded "from scratch", the website has suffered from some security problems...

The most important problem was the use of "mysql_connect" and the forgetfulness of "msql_realescape" in the sign-in which resulted in SQL injections...

The problem was quickly patched although the code of the site is really messy.

An attempt was undertaken to recode the website. Still "from scratch" but this time using Object-oriented programming (OOP).
## Community Reception

The website worked quite well, the visits were consistent and the community greatly appreciated it.

Some advertising campaigns were carried out through Twitter and in-game to democratize the website.

![Advertising on the main page of myfriends2](myfriends2_pub.png)

## In hindsight

If I had to do a similar project again today, I think I'd be happy even if Minecraft is not really my goto game anymore.

However, if there is one thing I would do differently on a new project, it's  the use of a framework like Symfony for instance. This should lighten development and help me structure my code in an organized way. And of course to ensure the project is less susceptible to various security flaws.

## Update 02/26/2018

A backup is available here (only in French) --> [myfriends2.guigur.com](http://myfriends2.guigur.com/) <--
