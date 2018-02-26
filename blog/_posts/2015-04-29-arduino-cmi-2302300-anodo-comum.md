---
layout: post
status: publish
published: true
title: "[ Arduino ] CMI 2302300 &Acirc;nodo Comum"
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 44
wordpress_url: https://viniciusfesil.wordpress.com/?p=44
date: '2015-04-29 13:55:28 -0300'
date_gmt: '2015-04-29 13:55:28 -0300'
categories:
- Arduino
tags:
- Arduino
- "&Acirc;nodo Comum"
- CMI 2302300
- Display 7 segmentos
comments: []
---
<p>E a&iacute; amigos, tudo bom?</p>
<p>Recentemente tive muita dificuldade para encontrar algum material sobre o display de 7 segmentos&nbsp;CMI 2302300. Diferentemente de muitos tutoriais ERRADOS, que encontrei, esse modelo de display &eacute; do tipo &Acirc;NODO COMUM.</p>
<p>Tomei a liberdade de desejar um datasheet bem simples mostrando a ordem dos pontos e qual segmento(LETRA) que ele representa, conforme imagem abaixo.</p>
<p>[caption id="attachment_45" align="alignnone" width="169"]<a href="http://viniciusfesil.com.br/wp-content/uploads/2015/04/img_20150429_103904.jpg"><img class="size-medium wp-image-45" src="http://viniciusfesil.com.br/wp-content/uploads/2015/04/img_20150429_103904.jpg?w=169" alt="Datasheet CMI 2302300" width="169" height="300" /></a> Datasheet CMI 2302300[/caption]</p>
<p>Antes que quebrem a cabe&ccedil;a assim como eu para verificar se ele funciona corretamente, quero lembra-los que ele trabalha em 12V e funciona bem a 10 MiliAmperes. Conforme o datasheet que desenhei acima, os pinos 1 e 5 s&atilde;o pinos &Acirc;NODO COMUM, ou seja, tanto o pino 1 ou 5, podem receber 12V e os demais s&atilde;o pinos do tipo CATODO COMUM. Uma forma de testar seus segmentos &eacute; ligar o pino 1 ou 5 a uma tens&atilde;o de 12V e adicionar um resistor de 680 ohns ao segmento que quer testar e ligar ao ground.</p>
<p>Outra dica que dou para voc&ecirc;s que estejam tentando utilizar o componente MAX7219, &eacute; que ele &eacute; espec&iacute;fico para trabalhar com CATODO COMUM e n&atilde;o &eacute; recomendado para este tipo de display. O mais indicado &eacute; o 74HC595. Existem v&aacute;rios exemplos, mostrando como utilizado com displays do tipo ANODO COMUM. Voc&ecirc; pode ver alguns exemplos <a title="74hc595 anodo comum" href="http://automatobr.blogspot.com.br/2013/08/mais-sobre-displays-de-led-com-74hc595.html" target="_blank">aqui</a> e <a title="74hc595 anodo comum exemplo 2" href="http://www.dobitaobyte.com.br/arduino/eletronica-digital-display-7-segmentos-com-74hc595" target="_blank">aqui</a>.</p>
<p>Espero ter ajudado, abra&ccedil;o.</p>
