---
layout: post
status: publish
published: true
title: "[JQuery] MultiBind"
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 33
wordpress_url: http://viniciusfesil.wordpress.com/?p=21
date: '2012-05-31 22:32:05 -0300'
date_gmt: '2012-05-31 22:32:05 -0300'
categories:
- jQuery
tags: []
comments: []
---
<p>Boa noite galera,</p>
<p>Respondendo ao que tinham me perguntado, existe uma maneira simples de dar m&uacute;ltiplas a&ccedil;&otilde;es a um ou mais seletores.</p>
<p>Esse c&oacute;digo abaixo deve ser familiar para voc&ecirc;s:</p>
<pre>$(seletor1).click(function() { 
    function1();
});

$(seletor1).ready(function() { 
    function1();
});

$(seletor1).blur(function() { 
    function1();
});

$(seletor2).click(function() { 
    function1();
});

$(seletor2).ready(function() { 
    function1();
});

$(seletor2).blur(function() { 
    function1();
});</pre>
<p>&Eacute; poss&iacute;vel eliminar v&aacute;rias linhas de c&oacute;digo repetitivo atrav&eacute;s do multibind, que &eacute; a atribui&ccedil;&atilde;o de m&uacute;ltiplas a&ccedil;&otilde;es para mais de um seletor, onde cada a&ccedil;&atilde;o pode ser separada com espa&ccedil;os dentro de uma string, ou divididas como um objeto:</p>
<p>Exemplo 1:</p>
<pre>$(seletor1, seletor2, ...).bind("click blur ready", function () { 
    function1();
 });</pre>
<p>Exemplo 2:</p>
<pre>$(seletor1, seletor2, ...).bind({
    click : function() { function1(); },
    blur : function() { function1(); },
    ready : function() { function1(); }
});</pre>
<p>Espero ter ajudado.</p>
<p>:D</p>
