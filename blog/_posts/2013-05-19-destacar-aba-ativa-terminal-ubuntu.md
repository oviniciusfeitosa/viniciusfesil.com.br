---
layout: post
status: publish
published: true
title: Destacar aba ativa - Terminal Ubuntu
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 35
wordpress_url: http://viniciusfesil.wordpress.com/?p=35
date: '2013-05-19 21:45:03 -0300'
date_gmt: '2013-05-19 21:45:03 -0300'
categories:
- Linux
tags:
- Ubuntu
comments: []
---
<p>Se voc&ecirc; j&aacute; ficou confuso, sem saber em qual aba est&aacute;, ao usar o terminal, seus problemas acabaram.<br />
Siga os passos abaixo:</p>
<p># cd /usr/share/themes/Ambiance/gtk-3.0/apps/<br />
# sudo cp gnome-terminal.css gnome-terminal.css _backup</p>
<p># sudo gedit /usr/share/themes/Ambiance/gtk-3.0/apps/gnome-terminal.css</p>
<p>Substitua do conte&uacute;do do arquivo pelo script abaixo, salve e pronto!</p>
<p>TerminalScreen {<br />
-TerminalScreen-background-darkness: 0.95;</p>
<p>background-color: #300a24;<br />
color: #fff;<br />
}</p>
<p>TerminalWindow .notebook tab {<br />
background-image: none;<br />
background-color: shade (@dark_bg_color, 1.02);<br />
border-radius: 3;</p>
<p>-unico-border-gradient: -gtk-gradient (linear, left top, right top,<br />
from (shade (@dark_bg_color, 0.93)),<br />
to (shade (@dark_bg_color, 0.93)));<br />
background-color: #D6C0B3;<br />
-unico-inner-stroke-width: 0;<br />
-unico-outer-stroke-width: 0;<br />
}</p>
