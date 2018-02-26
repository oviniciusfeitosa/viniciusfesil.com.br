---
layout: post
status: publish
published: true
title: '[JQuery] m&eacute;todo "on()" ou "live()"'
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 23
wordpress_url: http://viniciusfesil.wordpress.com/?p=4
date: '2012-03-28 01:50:16 -0300'
date_gmt: '2012-03-28 01:50:16 -0300'
categories:
- jQuery
tags:
- jQuery
- live()
- on()
comments: []
---
<p>Boa noite galera, sejam bem vindos. Este &eacute; meu post inicial, ent&atilde;o espero que gostem.</p>
<p><strong>Problema:</strong></p>
<pre style='background-color:lightyellow;border:1px solid black;font:12px;'>$(".campo").click(eventHandler);</pre>
<p>Dessa maneira, o evento de click para a class ".campo", ficar&aacute; vis&iacute;vel somente em determinados momentos dentro da p&aacute;gina.</p>
<p><strong>M&eacute;todo 'on()' (ou 'live()')</strong></p>
<p>Para quem n&atilde;o conhece, o m&eacute;todo 'on()' &eacute; utilizado caso voc&ecirc; precise que uma a&ccedil;&atilde;o seja vis&iacute;vel dentro de todo o escopo da camada de apresenta&ccedil;&atilde;o. Esse m&eacute;todo est&aacute; dispon&iacute;vel das vers&otilde;es 1.7 adiante da jquery.</p>
<p>O m&eacute;todo 'live()', ficou defasado desde a vers&atilde;o 1.4.3+ adiante, dando a possibilidade de utilizar, tamb&eacute;m, o m&eacute;todo <em>delegate.</em></p>
<p><strong>Como tornar uma a&ccedil;&atilde;o sempre vis&iacute;vel dentro da p&aacute;gina?</strong></p>
<pre style='background-color:lightyellow;border:1px solid black;font:12px;'>$(document).on("click", ".campo", function () {
    alert('Alo Mundo!');
});</pre>
<p>Seguem algumas informa&ccedil;&otilde;es retiradas do site da <a title="Live" href="http://api.jquery.com/live/">jQuery</a>:</p>
<pre style='background-color:lightyellow;border:1px solid black;font:12px;'>
$(<em>selector</em>).live(<em>events</em>, <em>data</em>, <em>handler</em>);                // jQuery 1.3+
$(document).delegate(<em>selector</em>, <em>events</em>, <em>data</em>, <em>handler</em>);  // jQuery 1.4.3+
$(document).on(<em>events</em>, <em>selector</em>, <em>data</em>, <em>handler</em>);        // jQuery 1.7+
</pre>
<p>Exemplos:</p>
<pre style='background-color:lightyellow;border:1px solid black;font:12px;'>
$("a.offsite").live("click", function(){ 
    alert("Goodbye!"); // jQuery 1.3+
});                
$(document).delegate("a.offsite", "click", function(){ 
    alert("Goodbye!"); // jQuery 1.4.3+
});  
$(document).on("click", "a.offsite", function(){ 
    alert("Goodbye!"); // jQuery 1.7+
});
</pre>
