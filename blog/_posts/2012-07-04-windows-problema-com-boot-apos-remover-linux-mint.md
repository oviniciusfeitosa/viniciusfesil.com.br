---
layout: post
status: publish
published: true
title: "[Windows] Problema com boot ap&oacute;s remover Linux Mint"
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 27
wordpress_url: http://viniciusfesil.wordpress.com/?p=27
date: '2012-07-04 02:42:03 -0300'
date_gmt: '2012-07-04 02:42:03 -0300'
categories:
- Windows
tags:
- Windows
comments: []
---
<p>Se estiverem com problemas para dar boot no windows, ap&oacute;s remover o Linux Mint que voc&ecirc; fazia dual boot com Windows 7, a solu&ccedil;&atilde;o est&aacute; no coment&aacute;rio abaixo:</p>
<p>&nbsp;</p>
<p>O seu problema foi causado pelo Linux, mas tem que resolver no Windows 7 mesmo.<br />
Tente reparar o sistema. Fa&ccedil;a assim...<br />
D&ecirc; boot com o DVD do Windows 7 e opte em "reparar". Depois de concluir a busca de instala&ccedil;&otilde;es existentes e tal clique em "avan&ccedil;ar". Escolha agora "prompt de comando" e digite:&nbsp;<em><strong><br />
bootsect /nT60 ALL /force /mbr<br />
</strong></em></p>
