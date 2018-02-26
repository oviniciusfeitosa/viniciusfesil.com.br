---
layout: post
status: publish
published: true
title: Como repetir o cabe&ccedil;alho para cada linha da tabela ?
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 173
wordpress_url: http://viniciusfesil.com.br/?p=173
date: '2016-01-29 19:28:37 -0200'
date_gmt: '2016-01-29 19:28:37 -0200'
categories:
- jQuery
tags:
- jQuery
- asp.net
- gridview
- eventhandler
- repetir cabe&ccedil;alho
- "$.each"
- javascript
comments: []
---
<p>Oi, tudo bom?</p>
<p>Recentemente tive problemas para repetir o cabe&ccedil;alho de uma tabela (thead) ao tentar fazer utilizando o componente GridView&nbsp;do asp.net, que utiliza WebForms. A solu&ccedil;&atilde;o mais r&aacute;pida e pr&aacute;tica que encontrei foi utilizar jquery. Vou mostrar para voc&ecirc; como fazer isso rapidamente com jQuery, independentemente da linguagem server-side, funcionar&aacute;.</p>
<h2>C&oacute;digo JavaScript</h2>
<pre><script language="javascript" type="text/javascript">

              jQuery(function ($) {
                        var funcoes = {
                             repetirCabecalhoPorLinhaDaTabela: function (seletorTabela, seletorLinha) {
		                if ($(seletorTabela).is(":visible")) {
		                    if (!seletorLinha) {
		                        seletorLinha = "tbody tr";
		                    }
		                    $(seletorTabela).find(seletorLinha).each(function (indice, elemento) {
		                        if (indice > 0) {
		                            var seletorCabecalho = $(seletorTabela).find("tbody tr").first().clone();
		                            $(seletorCabecalho).insertBefore(elemento);
		                        }
		                    });
		                }
		            }
		        };

		        $(document).ready(function () {
		            funcoes.repetirCabecalhoPorLinhaDaTabela("#grdProtocolo", ".linha_grid")
		        });
                
            });
</pre>
<h2>Explicando</h2>
<p>Come&ccedil;amos o c&oacute;digo com a chamada do jquery injetando fun&ccedil;&otilde;es dentro do seu bloco. Qualquer d&uacute;vida sobre porque utilizei o "jQuery" antes, acesse esse link que explico porque &eacute; interessante utiliza-lo.Em seguida &eacute; criada uma vari&aacute;vel do tipo objeto chamada "funcoes" com a propriedade "repetirCabecalhoPorLinhaDaTabela" que recebe como primeiro par&acirc;metro o seletor da tabela e como segunda par&acirc;metro qual o seletor das linhas da sua tabela. Por default, se o par&acirc;metro "seletorLinha" n&atilde;o for informado, ele assume que o seletor ser&aacute; "tbody tr" que buscar&aacute; todas as linhas do corpo da tabela. Ap&oacute;s isso, &eacute; feita uma busca na tabela por todos os elementos que tem como seletor, o item informado na vari&aacute;vel "seletorLinha". Esse loop &eacute; feito atrav&eacute;s do m&eacute;todo "$.each( /* fn(i, e) */)" nativo da biblioteca jQuery e em seu "eventHandler" recebe por padr&atilde;o o &iacute;ndice do loop e o elemento que est&aacute; sendo iterado. Ent&atilde;o, somente se o &iacute;ndice da itera&ccedil;&atilde;o for maior que "0", pois o primeiro item j&aacute; tem cabe&ccedil;alho, &eacute; que &eacute; feita a duplica&ccedil;&atilde;o do cabe&ccedil;alho para as demais linhas, clonando o cabe&ccedil;alho e adicionando-o antes do elemento em quest&atilde;o</p>
<p>Logo ap&oacute;s "$(document).ready( /* fn */ )" fa&ccedil;o uma chamada para a fun&ccedil;&atilde;o "repetirCabecalhoPorLinhaDaTabela" que criei dentro do objeto "funcoes".</p>
<h2>Conclus&atilde;o</h2>
<p>Repetir o cabe&ccedil;alho nunca foi t&atilde;o f&aacute;cil se voc&ecirc; puder utilizar jQuery. Basta chamar o m&eacute;todo que criamos, informando os parametros desejados e pronto! Parece m&aacute;gica, hehehe.<br />
Para quem j&aacute; conhece e trabalha com jQuery, basta olhar o c&oacute;digo-fonte e ajustar da maneira como bem entender.</p>
<p>Espero que lhe ajude. Abra&ccedil;o.</p>
