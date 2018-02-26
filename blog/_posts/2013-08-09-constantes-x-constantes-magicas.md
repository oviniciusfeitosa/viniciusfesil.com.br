---
layout: post
status: publish
published: true
title: Constantes x Constantes M&aacute;gicas
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 41
wordpress_url: http://viniciusfesil.wordpress.com/?p=41
date: '2013-08-09 13:21:12 -0300'
date_gmt: '2013-08-09 13:21:12 -0300'
categories:
- PHP
tags:
- php
comments: []
---
<p>* Constantes x Constantes M&aacute;gicas</p>
<p>Para fins informativos ou de quem pretende estudar para a prova de certifica&ccedil;&atilde;o, existe uma simples diferen&ccedil;a entre as Constants e Magic Constants.</p>
<p>[ Constants ]<br />
- Ap&oacute;s a associa&ccedil;&atilde;o de valor a uma constante, ela n&atilde;o pode ser alterada.<br />
- Constantes podem ser declaradas em interfaces e classes.<br />
- Se uma constante for definida dentro de uma interface, essa interface n&atilde;o pode ser implementada.<br />
- Aceita o uso de heredoc.<br />
- Podem estar num escopo global ou n&atilde;o;<br />
- Por padr&atilde;o, geralmente s&atilde;o declaradas em mai&uacute;sculo. Mas se necess&aacute;rio, na defini&ccedil;&atilde;o da constante &eacute; poss&iacute;vel informar se deve ser considerado ou n&atilde;o case sensitive.<br />
[Exemplo]:<br />
define("MINHA_CONSTANTE", "valor");<br />
[Exemplo2]:<br />
class teste {<br />
public const MINHA_CONSTANTE =<br />
}<br />
[Exemplo3]:<br />
class teste {<br />
const TESTANDO = <<<EOT<br />
Testando<br />
EOT;<br />
}<br />
define("TESTE2", <<<EOT<br />
Testando2<br />
EOT<br />
);</p>
<p>echo teste::TESTANDO;<br />
echo TESTANDO2;<br />
[Exemplo 3]<br />
E_ALL, TRUE;</p>
<p>[ Magic Constants ]<br />
- S&atilde;o constantes, que apesar de ter o nome definido no mesmo padr&atilde;o das anteriores, o seu valor pode mudar de acordo com a situa&ccedil;&atilde;o em que se encontra.<br />
[Exemplo]<br />
__DIR__, __FILE__, __METHOD__, __NAMESPACE__, ...</p>
