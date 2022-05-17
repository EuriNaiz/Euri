---
title: "GTK, HIGs & The XFCE's Future"
layout: post
date: 2022-05-16 00:20
tag:
- XFCE
- Adwaita
- Granite
- GTK
- "GTK 5"
- Future
- Design
- Desktop
- Platform
- Ecosystem
- "GNU + Linux"
- Theming
- "Dark Mode"
- HIG
- Mate
- "GTK Library"
- Iconography
articulos: true
image: /assets/images/media/XFCE_Future.png
headerImage: true
description: "XFCE, GTK and some problematics found in the GNU + Linux desktop, some solutions for the XFCE's future as DE and/or platform."
category: blog
author: Euri
externalLink: false
permalink: "/blog/GTK-HIGs-And-The-XFCE-Future/"
comments:
  host: floss.social
  username: EuriNaiz
  id: 
---

# GTK, HIGs & The XFCE's Future
## Introduction
We all can be d'accord with me when I say that a modern DE/OS should be beauty, accessible, stable, easy to use and recognisable.
Recently GNOME, in their process to become into a platform, [neutralised GTK](https://blog.elementary.io/linux-experiment-interview-cassidy-james-blaede-gnome-themes-libadwaita/) a little (is expected to be fully neutral in their version 5), removing all widgets that follow the GNOME's HIG, and moving 'em to the new library [Libadwaita](https://blogs.gnome.org/alexm/2021/12/31/libadwaita-1-0/), so, now Adwaita isn't part of GTK anymore... That's so useful for another DEs and Platforms (like Elementary)...

You can keep using GTK 4 without problems, but for GTK 5 it will be harder, because you'll need use a library, like [LibAdwaita](https://gnome.pages.gitlab.gnome.org/libadwaita/) or [Granite](https://github.com/elementary/granite).

But, why does GTK libraries care here? Easy, In the future all apps will use a library to be built, and now in GTK 4 you can force apps to ignore library and use GTK themes with the ```GTK_THEME``` variable, but it is expected to be dropped for GTK 5... And taking in count that GNOME apps are SO popular and included by a lot of distros (like Linux Mint or Manjaro), the XFCE desktop will (and actually) look SO inconsistent.
But, Inconsistency isn't the only problem, other problems are:

1. The multiple HIGs for the end user, ¡That's confusing!
2. Accesibility
3. Branding problems (for XFCE and Distros)
4. User's personalisation
5. Broken apps caused by "Themes"
6. Etc...

## The "theming" problems.

I know, theming is a controversial topic, right, but just think about it... 

Imagine: You're running KDE Plasma, and you arbitrarily modify the style sheets of the apps (a.k.a you apply a "theme") to look like MacOS... The HIGs are the same, the theme won't change it, and the app won't look like MacOS because the KDE apps don't follow the HIG's. The HIG are the same and you cannot change 'em without rewriting the app.
The same happens with GNOME apps, even overriding the appearance, the app won't look like an XFCE app. 

> Epiphany is a special case, because Elementary and GNOME co-worked together, and it is possible because both HIG are so close.

> Maybe KDE apps could be adapted to Windows, because the HIG are similar.

As ecosystem, Elementary officially support GTK, Epiphany, and other external projects, and even, are part of the ecosystem. In the future, when all apps were using a GTK library, adopting apps will be hard for XFCE, but there are some possible solutions and I'll mention em in this article.

## They lied, GNOME theming is not dead.

Doesn't Adwaita killed theming? Answering that question isn't too easy like a "yes" or "no", because... Yes, the old and dirty way to "theme" apps is over, but it's fine, because [there are no broken apps anymore](https://stopthemingmy.app/)
But the good new is: [¡Now you'll be able to theme your apps right!](https://blogs.gnome.org/alatiera/2021/09/18/the-truth-they-are-not-telling-you-about-themes/) without broken apps or weird issues.

But what do I mean with broken apps? This:

![secrets white text in white background](https://stopthemingmy.app/assets/stylesheets.png)

So, Now we can theme apps based on libadwaita? Yes, because now themes are colour palettes, and, even you can see some themes for libadwaita right now, themes applied for all system, or themes for individual apps.
The next theme is applied for all system:

[Flat Remix Theme](https://www.gnome-look.org/s/Gnome/p/1214931) For Adwaita Apps:

![flat remix theme for adwaita](https://i.redd.it/t6eoh20jclq81.png)

And this theme is for an app specifically:

[Pink theme for G-T-E](https://gitlab.com/-/snippets/2277556) (GNOME Text Editor) by Xerz:
![Pink G-T-E Theme by Xerz](https://gitlab.com/uploads/-/system/personal_snippet/2277556/4b911d449b39b350a346ecb0b7559e61/image.png)

But, that isn't all, ¡Now we haven't got third themes just for adwaita apps!, Now devs provide us themes officially, like the themes provided by default for G-T-E

![GTE settings screenshot](https://dl.flathub.org/repo/screenshots/org.gnome.TextEditor-stable/752x423/org.gnome.TextEditor-ea17dfb8e8cf60b64fece1a97f0d3173.png)

> Here is an [interesting article](https://blog.elementary.io/linux-experiment-interview-cassidy-james-blaede-gnome-themes-libadwaita/), I really recommend it.



But, Why I am talking about GNOME? This is XFCE... Right, now I can explain some solutions for these problematics. The antecedents are important to understand the following points.

## Adopting (and co-develop) a GTK library (and their HIGs)

Adopting Adwaita **IN MY OPINION** is the best option, and what I want to see in the XFCE's future. And the reasons are:

1. [Like granite](https://blog.elementary.io/user-interface-study-findings/), the [GNOME HIGs are designed with accessibility and beauty in mind (and studies behind).](https://developer.gnome.org/hig/principles.html)
2. ¡The major part of the GTK GNU+Linux apps are wrote using GNOME HIG!. That means that almost all apps will look native, and consistent with the system/DE.
3. Theming. You'll be able to set custom themes (colour palettes) and accent colours.
4. Is maintained by a large user/dev base, you can have some warranties, like the support in the future or the new features addition.
5. A more unified experience. Before you've based the XFCE icons in Adwaita icons, or setting CSD by default... Now this could be the next step to offer a better experience.
6. The possibility to offer a best and standardised dark mode.
7. The opportunity to collaborate and work with the GNOME developers. Where a single person do a good work, a whole team can do miracles.

> D'accord with an [interview](https://www.dedoimedo.com/computers/interview-xfce.html) between Dedoimedo and Sean (XFCE Core Developer), you'd like to hire development, design and bug triage... I have good news: That's work done in adwaita, if adwaita is adopted as GTK4 library for XFCE apps, the only thing to worry is doing the bug triage.

## What about Granite?

I know that Adwaita's appearance could be a little different compared with GreyBird... But [the new] Adwaita is nice, so eyecandy, easy, and has good accessibility.
But, there is other library too good build like Adwaita, and that's Granite, the official theme (and HIG/Library) for Elementary Platform.

Here you can see a comparison between Granite and Eyecandy, you can look the similarities... Actually GreyBird and Granite are SO close, even in colours (but more modern)...

Personally I think Granite is closer than Adwaita, with GreyBird.

| GreyBird's appearance                                                           | Granite's appereance                                                                                     |
|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------:|
| ![XFCE Display dialog](https://cdn.xfce.org/about/tour/4.16/display-dialog.png) | ![Elementary Desktop settings](https://cdn-images-1.medium.com/max/1600/1*EyErGVV6till1aap3FMPYA@2x.png) |

Here is the comparison but in dark mode:

| GreyBird's appearance                                                             | Granite's appereance                                                                                                     |
|:---------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------:|
| ![XFCE Panel settings](https://cdn.xfce.org/about/tour/4.16/panel-statustray.png) | ![Granite Demo](https://blog.elementary.io/images/look-and-feel-changes-coming-elementary-os-6/granite-welcome-dark.png) |

But what are the reasons to adopt Granite?

1. Is built with some [UI studies](https://blog.elementary.io/user-interface-study-findings/), that gives you some idea about the experience that the end user gets.
2. Is supported by a corporation, it can warrant the long time development and support.
3. https://blog.elementary.io/user-interface-study-findings/
4. Is designed thinking to be inclusive with all people, [accessibility features are just features.](https://blog.elementary.io/accessibility-features-are-just-features/)
5. The design is so close with GreyBird (but modern), the change won't be as radical as Adwaita could be.
6. There is a dev base developing apps for Elementary platform... That means, the experience is less or more coherent and consistent (but not at all like could be with Adwaita)
7. You can monetise your apps in the Elementary's store... That means, more money entries for XFCE project.

## Co-building a new GTK library, HIG, iconography, and platform with Mate or other project.

Ok, This is weird, but, keep reading because it makes sense...
Mate and XFCE are small projects (compared with KDE or GNOME, but not the smallest like LXQT), and building a whole and attractive platform could be hard, so, working together could derivate a new collaborative platform, at least, a shared GTK library, HIGs, and maybe some apps/ports...

I do not know a lot about Mate, but in **my** experience, XFCE and Mate have some similarities, and redundant apps... About the philosophy or direction I have no idea, but I think you can converge in this and work together.

For example Pluma and Mousepad, they're so, so, so similar... With a shared library, HIGs, etc... The maintainers could work in a single app, adding features faster, or improving the app fixing bugs faster; And the same with terminal, Image Viewer...

Even, with some fear about being cancelled, I can say... Even you could co-develop a single DE/Platform... (Something like Razor-qt and LXDE) and just offer two layouts, a layout like XFCE and other like Mate... That could specially beneficial for all (specially for end users), because they will be able to get a best, modern and rich experience, without personalisation or choosing options...

The situation also could be applied with Cinnamon, but, being realistic, I think it wouldn't happen... Is more probably with Mate.

## Co-create a new GTK library to reimplement AGAIN the old bad practices...

Yes, one more time talking about collaboration with other proyects, but... If KDE collaborate in GNOME and vice-versa, Why XFCE and Mate not? 
This option is less ambitious and, in reality, won't fix the actual problems, but... Anyway, a new library could be co-created to reimplement the old ~~hacks~~ "themes", and allow users theme their desktop, and cross-desktop apps without a persistent appearance like now's happening with GNOME LibAdwaita or Elementary apps...
Probably Cinnamon could be interested in this... I don't know.

1. It won't solve the problems, ¡It will prolong 'em only! And moving the problems from GTK to the new library
2. The desktop will never be consistent, or attractive to new developers (Right now, some developers have been approaching to GNOME as platform... Now GNU/Linux is a little more attractive for developers than before)
3. Is time lost that could be used to improve other parts of XFCE like accessibility or Wayland support.
4. You could lost the time to adapt you to the modern times, and this could cost the attractive to be used as DE for new operating systems, or even, the existence of the XFCE project...

## Create your OWN GTK Library, HIG, and platform.

Ok, this is the last option (in addition to keep the things like they're), and I think it isn't feasible for many reasons... And that's create your own HIG, Library, etc...

1. Now it's so late to start with it, in retrospective with the past releases times, it would be ready for 2045... /s ¡Debian released their last version with the last XFCE version!
2. The second obstacle is being attractive to make XFCE apps... If there are just 3 or 4 XFCE apps... Good luck being consistent and having a HIG coherent...
3. With this, maybe new distros focused in XFCE will born and will make XFCE more attractive and used...
4. Maybe this could stop the residual use of XFCE (mainly for lightweight distros) and, making it a first raze DE/platform and return "to the game".

## Conclusions

I know that XFCE project have few people, and add some of this to the to-do list requires efforts, time and maybe money too, but now is the time to start working in the times to come, because though the time XFCE have been losing relevance and that could cost the project's existence...

And in this time, you have the opportunity to fix some deficiencies and old bad practices, and if you postpone it, after it could require more effort, time and maybe starting again some code (just see GNOME 2 and GNOME 3).

I also know that XFCE needs other improvements that could be more important than this, like the Wayland port to stay current, the deprecation of X.org is coming and everything seems to indicate that [fedora will be the first OS doing it.](https://www.phoronix.com/scan.php?page=news_item&px=Fedora-37-Drop-Old-X11-Drivers)

But this also requires time, and I prefer to put the topic on the table now that there is time to discuss and work in it, GTK 4 have been released some time ago, and the GTK 5 release is far in future, but should be warned, without surprises.

Euri Montero 🍊️
Kontaktua [at] EuriNaiz [dot] com
