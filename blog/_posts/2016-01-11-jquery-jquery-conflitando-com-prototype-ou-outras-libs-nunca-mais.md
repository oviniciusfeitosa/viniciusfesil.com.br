---
layout: post
status: publish
published: true
title: "[ jQuery ] jQuery conflitando com Prototype ou outras Libs? Nunca mais!"
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 113
wordpress_url: http://viniciusfesil.com.br/?p=113
date: '2016-01-11 15:53:27 -0200'
date_gmt: '2016-01-11 15:53:27 -0200'
categories:
- jQuery
tags:
- jQuery
- noConflict
- protype
- conflito
comments: []
---
<p>Opa, beleza?</p>
<p>Vim aqui pra dar uma dica para voc&ecirc;s de como acabar com esse problema que tiram os cabelos de alguns Devs iniciantes.</p>
<p>Quando est&atilde;o dando manuten&ccedil;&atilde;o em sistemas que utilizam prototype ou outras libs em conjunto com jQuery, normalmente a vari&aacute;vel "$" j&aacute; &eacute; muito utilizada em escopo global da aplica&ccedil;&atilde;o client-side. Dificultando chamadas para m&eacute;todos ou defini&ccedil;&atilde;o de propriedades atrav&eacute;s do jQuery.</p>
<p>Existem v&aacute;rias maneiras de solucionar esse problema.&nbsp;Vamos ver tr&ecirc;s maneiras bem simples:</p>
<h2>1&ordf; Forma - Utilizando "jQuery.noConflict()":</h2>
<pre lang="javascript">var $j = jQuery.noConflict();
$j(document).ready(function () {
	alert('Oi, mundo!');
});
</pre>
<p>Desta maneira &eacute; poss&iacute;vel definir que a vari&aacute;vel "$j" recebe um objeto jQuery e com ele podemos ter o mesmo resultado que a vari&aacute;vel "$".</p>
<h2>2&ordf; Forma - Utilizando "jQuery(function($){ /*fn*/ })":</h2>
<pre lang="javascript">jQuery(function($){
	alert('Oi, mundo!');
})
</pre>
<p>Definindo "jQuery" manualmente e informando como par&acirc;metro um eventHandler que recebe como valor "$", assim como no primeiro cen&aacute;rio &eacute; poss&iacute;vel trabalhar normalmente com o c&oacute;digo-fonte.</p>
<h2>3&ordf; Forma - Outra op&ccedil;&atilde;o de "jQuery.noConflict()":</h2>
<pre lang="javascript"><script src="other_lib.js"></script><script src="jquery.js"></script><script>// <![CDATA[
$.noConflict();
jQuery( document ).ready(function( $ ) {
  // Code that uses jQuery's $ can follow here.
});
// Code that uses other library's $ can follow here.
// ]]></script></pre>
<p>Neste exemplo que foi extra&iacute;do de "http://api.jquery.com/jQuery.noConflict/" onde podemos observar que assim que definido "$.noConflict();" podemos trabalhar com os 2 cen&aacute;rios acima em conjunto sem problemas.</p>
<h2>Conclus&atilde;o</h2>
<p>Existem enumeras maneiras de trabalhar com bibliotecas que utilizam vari&aacute;veis semelhantes, estas s&atilde;o apenas algumas formas de contornar essa situa&ccedil;&atilde;o utilizando jQuery. Espero que ajude. Deixe seu coment&aacute;rio!</p>
<p>Abra&ccedil;o.</p>
