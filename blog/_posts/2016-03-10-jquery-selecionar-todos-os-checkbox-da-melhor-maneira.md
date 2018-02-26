---
layout: post
status: publish
published: true
title: "[ jQuery ] Marcar ou Desmarcar todos os checkbox da melhor maneira!"
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 191
wordpress_url: http://viniciusfesil.com.br/?p=191
date: '2016-03-10 15:16:17 -0300'
date_gmt: '2016-03-10 15:16:17 -0300'
categories:
- jQuery
tags:
- jQuery
- "$.each"
- checkbox
- prop
comments: []
---
<p>Se voc&ecirc; est&aacute; precisando de algo r&aacute;pido e eficaz para selecionar todos os seus checkboxes em uma lista, por exemplo, n&atilde;o se preocupe vou mostrar uma solu&ccedil;&atilde;o bacana para voc&ecirc;.</p>
<h2>O c&oacute;digo</h2>
<p><code><br />
marcarTodosCheckBoxes: function (seletorCheckBoxes) {<br />
$(this).prop('checked', !$(this).prop('checked'));<br />
$(seletorCheckBoxes).prop("checked", $(this).prop("checked"));<br />
}<br />
</code></p>
<h2>Como utilizar?</h2>
<p>Bem simles, basta associar essa a&ccedil;&atilde;o a seu elemento ou a um seletor.</p>
<p>Vou mostrar duas formas que podem estar mais pr&oacute;ximas do que voc&ecirc;s est&aacute; acostumado a trabalhar.</p>
<h3>A primeira</h3>
<p>Definindo uma a&ccedil;&atilde;o para o seletor "#botaoMarcarDesmarcar" ao carregar a p&aacute;gina, dentro de $(document).ready( /* fn */ ).</p>
<pre lang="php">
<!-- include da lib jquery antes -->
<script type="text/javascript">// <![CDATA[
jQuery(function($){ funcoesLegais = { marcarTodosCheckBoxes: function (seletorCheckBoxes) { $(this).prop('checked', !$(this).prop('checked')); $(seletorCheckBoxes).prop("checked", $(this).prop("checked")); } } $(document).ready(function() { $("#botaoMarcarDesmarcar").click(function() { funcoesLegais.marcarTodosCheckBoxes(".checkbox_legal"); }); }); })
// ]]></script>

&nbsp;

<button id="botaoMarcarDesmarcar" type="button"> MARCAR / DESMARCAR </button>
<table style="border-color: #B0B0B0; width: 434px; border-collapse: collapse;">
<tbody>
<tr>
<th style="width: 25px;"></th>
<th scope="col">Valor</th>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="1" /></td>
<td>00001</td>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="2" /></td>
<td>00002</td>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="3" /></td>
<td>00003</td>
</tr>
</tbody>
</table>
</pre>
<p>&nbsp;</p>
<h3>A segunda</h3>
<p>Chamando diretamente no a&ccedil;&atilde;o "onclick" do bot&atilde;o "botaoMarcarDesmarcar".</p>
<pre lang="php">
<!-- include da lib jquery antes -->
<script type="text/javascript">// <![CDATA[
jQuery(function($){ marcarTodosCheckBoxes: function (seletorCheckBoxes) { $(this).prop('checked', !$(this).prop('checked')); $(seletorCheckBoxes).prop("checked", $(this).prop("checked")); } })
// ]]></script>

&nbsp;

<button id="botaoMarcarDesmarcar" type="button"> MARCAR / DESMARCAR </button>
<table style="border-color: #B0B0B0; width: 434px; border-collapse: collapse;">
<tbody>
<tr>
<th style="width: 25px;"></th>
<th scope="col">Valor</th>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="1" /></td>
<td>00001</td>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="2" /></td>
<td>00002</td>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="3" /></td>
<td>00003</td>
</tr>
</tbody>
</table>
</pre>
<h2> Exemplo pr&aacute;tico </h2>
<p><script type="text/javascript"><br />
	jQuery(function($){<br />
		funcoesLegais = {<br />
			marcarTodosCheckBoxes: function (seletorCheckBoxes) {<br />
		        $(this).prop('checked', !$(this).prop('checked'));<br />
		        $(seletorCheckBoxes).prop("checked", $(this).prop("checked"));<br />
		    }<br />
		}<br />
		$(document).ready(function() {<br />
			$("#botaoMarcarDesmarcar").click(function() {<br />
				funcoesLegais.marcarTodosCheckBoxes(".checkbox_legal");<br />
			});<br />
		});<br />
	})<br />
</script></p>
<p>&nbsp;</p>
<p><button id="botaoMarcarDesmarcar" type="button"> MARCAR / DESMARCAR </button></p>
<table style="border-color: #B0B0B0; width: 434px; border-collapse: collapse;">
<tbody>
<tr>
<th style="width: 25px;"></th>
<th scope="col">Valor</th>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="1" /></td>
<td>00001</td>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="2" /></td>
<td>00002</td>
</tr>
<tr>
<td><input class="checkbox_legal" name="meu_check" type="checkbox" value="3" /></td>
<td>00003</td>
</tr>
</tbody>
</table>
<h2>Conclus&atilde;o</h2>
<p>Tanto a primeira quanto a segunda forma funcionam, veja qual a melhor se adapta a sua forma de programar. Existem outras maneiras de fazer a seli&ccedil;&atilde;o, utilizando por exemplo o "$.each(function (indice, seletor) { /* fn */})", por&eacute;m &eacute; menos perform&aacute;tica.</p>
<p>Caso tenha algo a acrescentar, uma dica, corre&ccedil;&atilde;o ou d&uacute;vida, deixe seu coment&aacute;rio!&nbsp;Espero que tenha lhe ajudado!</p>
<p>Caso tenha gostado,&nbsp;compartilhe e ajude outras pessoas!</p>
<p>Abra&ccedil;o!</p>
<p>&nbsp;</p>
