---
layout: post
status: publish
published: true
title: Ubuntu Gnome - Configurando Bluetooth Linux A2DP
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 452
wordpress_url: http://viniciusfesil.com.br/?p=452
date: '2017-08-11 14:38:38 -0300'
date_gmt: '2017-08-11 14:38:38 -0300'
categories:
- Linux
tags:
- Ubuntu
- a2dp
- linux
- bluetooth
- bluez-firmware
- Gnome
comments: []
---
<p>Bom dia, tudo j&oacute;ia?</p>
<p>Recentemente enfrentei alguns problemas pra conseguir instalar os drivers corretos para usar um adaptador Bluetooth no Ubuntu Gnome para se conectar com um fone de ouvido JBL Everest 300.</p>
<p>Sempre que eu pareava o adaptador de bluetooth com o fone de ouvido eu notei que a qualidade do audio estava muito reduzida. Descobri que era porque por padr&atilde;o o perfil ativo &eacute; HSP e para ter uma qualidade em alta defini&ccedil;&atilde;o &eacute; necess&aacute;rio ativar o perfil A2DP.</p>
<p>Consegui um tutorial bacana com o <a href="https://github.com/darciro">Ricardo</a>, por&eacute;m n&atilde;o informava como instalar o bluez-firmware.</p>
<p>Ent&atilde;o adicionei o passo a passo em um Gist do meu github para voc&ecirc; conseguir habilitar isso no seu SO. Segue o abaixo:</p>
<p>https://gist.github.com/vinnyfs89/d02a39bf4cada2f09ea5569cb097dde3</p>
<p>Espero que lhe ajude!</p>
<p>Abra&ccedil;o.</p>
