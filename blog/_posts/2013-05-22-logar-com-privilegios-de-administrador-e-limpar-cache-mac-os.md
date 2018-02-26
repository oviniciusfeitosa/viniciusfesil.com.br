---
layout: post
status: publish
published: true
title: Logar com privil&eacute;gios de administrador e limpar cache no MAC OS
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 39
wordpress_url: http://viniciusfesil.wordpress.com/?p=39
date: '2013-05-22 04:35:36 -0300'
date_gmt: '2013-05-22 04:35:36 -0300'
categories:
- MAC OS
tags:
- MAC
comments: []
---
<p>Ap&oacute;s apertar a tecla Power, segure as teclas Command + S para iniciar no modo usu&aacute;rio &uacute;nico.<br />
Quando iniciar o terminal de comandos digite os comandos abaixo:</p>
<p>$ mount -uw /<br />
$ chmod 777 /etc/sudoers</p>
<p>Agora v&aacute; em /Library/Cache e apague todas as pastas de dentro.</p>
<p>Aqui funcionou perfeitamente.<br />
Esse passo foi necess&aacute;rio ser feito, porque o macbook n&atilde;o inciava e nem era poss&iacute;vel reparar o disco. Ao ligar no suporte da apple, eles tentaram v&aacute;rias op&ccedil;&otilde;es que n&atilde;o funcionaram e a queriam enviar o macbook para o suporte t&eacute;cnico em uma loja f&iacute;sica para fazer o backup dos meus dados e formatar. Essa solu&ccedil;&atilde;o foi a ideal.</p>
<p>Espero ter ajudado.</p>
