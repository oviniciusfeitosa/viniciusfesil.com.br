---
layout: post
status: publish
published: true
title: Docker + PHPStorm + XDebug
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 428
wordpress_url: http://viniciusfesil.com.br/?p=428
date: '2017-07-20 08:00:57 -0300'
date_gmt: '2017-07-20 08:00:57 -0300'
categories:
- PHP
- Docker
- PHPStorm
tags:
- github
- XDebug
- PHPStorm
- Docker
- Container
- DBGp Proxy
comments: []
---
<p>Ol&aacute;, tudo bom com voc&ecirc;?</p>
<p>Se voc&ecirc; que sempre achou complicado configurar e usar XDebug, ainda por cima utilizando Docker + PHPStorm, esse post foi feito exclusivamente para desmistificar esse processo para voc&ecirc;.</p>
<p><strong>O que &eacute; XDebug?</strong></p>
<p>XDebug &eacute; um m&oacute;dulo do PHP que tem como finalidade monitorar nossa aplica&ccedil;&atilde;o &nbsp;visualizando cada passo que &eacute; executado e valor que &eacute; atribu&iacute;do sem a necessidade de ficar adicionando c&oacute;digo na nossa aplica&ccedil;&atilde;o .</p>
<p><strong>O que &eacute; o PHPStorm?</strong></p>
<p>PHPStorm &eacute; uma IDE de desenvolvimento de software utilizada profissionalmente que possui um grande arsenal de ferramentas que possibilitam a cria&ccedil;&atilde;o, organiza&ccedil;&atilde;o e monitoramento de c&oacute;digo com mais facilidade.</p>
<p><strong>Iniciando</strong></p>
<p>Primeiramente precisamos configurar a IDE PHPStorm para que seja poss&iacute;vel monitorar nossa aplica&ccedil;&atilde;o &agrave; partir dele.</p>
<ul>
<li>Selecione o menu Tools > DBGp Proxy > Configuration...</li>
</ul>
<p>[caption id="attachment_429" align="aligncenter" width="1020"]<img class="size-large wp-image-429" src="http://viniciusfesil.com.br/wp-content/uploads/2017/07/Captura-de-tela-de-2017-07-19-21-42-14-1020x792.png" alt="" width="1020" height="792" /> PHPStorm DBGP Proxy Configuration[/caption]</p>
<ul>
<li>Preencha sua IDE Key, host e porta que trabalhar&aacute; com seu container PHP que est&aacute; rodando dentro do Docker.</li>
</ul>
<p>[caption id="attachment_431" align="aligncenter" width="330"]<img class="size-full wp-image-431" src="http://viniciusfesil.com.br/wp-content/uploads/2017/07/Captura-de-tela-de-2017-07-19-21-40-52.png" alt="DBGp Proxy Configuration" width="330" height="206" /> DBGp Proxy Configuration[/caption]</p>
<p>&nbsp;</p>
<ul>
<li>Para Iniciar o modo Debug do XDebug, clique no &iacute;cone que mais parece um pequeno telefone!</li>
</ul>
<p>[caption id="attachment_430" align="aligncenter" width="273"]<img class="size-full wp-image-430" src="http://viniciusfesil.com.br/wp-content/uploads/2017/07/Captura-de-tela-de-2017-07-19-21-41-03.png" alt="Start Listening for PHP Debug Connections" width="273" height="41" /> Start Listening for PHP Debug Connections[/caption]</p>
<ul>
<li>Ap&oacute;s clicar no &iacute;cone ele dever&aacute; ficar dessa maneira:</li>
</ul>
<p>[caption id="attachment_434" align="aligncenter" width="249"]<img class="size-full wp-image-434" src="http://viniciusfesil.com.br/wp-content/uploads/2017/07/Captura-de-tela-de-2017-07-19-22-52-21.png" alt="START LISTENING FOR PHP DEBUG CONNECTIONS AFTER CLICK" width="249" height="23" /> START LISTENING FOR PHP DEBUG CONNECTIONS AFTER CLICK[/caption]</p>
<p>Pronto agora vamos para a configura&ccedil;&atilde;o do server.</p>
<ul>
<li>Nas configura&ccedil;&otilde;es do seu PHPStorm, acesse Languages &amp; Frameworks > PHP > Servers</li>
<li>Clique no "+" e Adicionar um novo server com o nome que desejar. No meu caso chamei de <strong>xDebug</strong>.</li>
<li>Adicionar o host <strong>localhost</strong> e a porta <strong>9000</strong></li>
</ul>
<p>Pronto! Se voc&ecirc; seguiu esse passo a passo provavelmente suas configura&ccedil;&otilde;es devem estar como abaixo:</p>
<p>[caption id="attachment_500" align="aligncenter" width="1020"]<img class="wp-image-500 size-large" src="http://viniciusfesil.com.br/wp-content/uploads/2017/07/Captura-de-tela-de-2017-09-05-22-10-40-1020x653.png" alt="PHPStorm Server Config" width="1020" height="653" /> PHPStorm Server Config[/caption]</p>
<p>[caption id="attachment_502" align="aligncenter" width="1020"]<img class="size-large wp-image-502" src="http://viniciusfesil.com.br/wp-content/uploads/2017/07/Captura-de-tela-de-2017-09-05-22-10-58-1020x651.png" alt="PHPStorm DBGp Proxy configs" width="1020" height="651" /> PHPStorm DBGp Proxy config[/caption]</p>
<p>&nbsp;</p>
<p><strong>Configurando o container de aplica&ccedil;&atilde;o&nbsp;</strong></p>
<p>Feitos os passos acima, agora &eacute; necess&aacute;rio configurar nosso container da aplica&ccedil;&atilde;o para trabalhar habilitar a extens&atilde;o do XDebug e configurar par&acirc;metros desejados.</p>
<p>Para facilitar para voc&ecirc;, criei um reposit&oacute;rio no github ensinando a criar uma imagem e gerar um container atrav&eacute;s de uma estrutura inicial que eu j&aacute; montei para facilitar.</p>
<p>Ent&atilde;o vamos l&aacute;, caso voc&ecirc; ainda n&atilde;o tenha nenhuma imagem ou container, clone o reposit&oacute;rio abaixo e siga os passos descritos no reposit&oacute;rio.</p>
<hr />
<p>https://github.com/vinnyfs89/docker-php-xdebug</p>
<hr />
<p>Se voc&ecirc; executou os passos acima corretamente, quando voc&ecirc; executar o comando "<strong>docker ps"&nbsp;</strong>em seu terminal, deve aparecer algo como isso:</p>
<p>[caption id="attachment_435" align="aligncenter" width="1020"]<img class="size-large wp-image-435" src="http://viniciusfesil.com.br/wp-content/uploads/2017/07/Captura-de-tela-de-2017-07-19-23-05-50-1020x25.png" alt="docker container status" width="1020" height="25" /> docker container status[/caption]</p>
<p><strong>Conclus&atilde;o</strong></p>
<p>Ap&oacute;s executar os passos descritos no reposit&oacute;rio acima, voc&ecirc; j&aacute; estar&aacute; pronto pra trabalhar com o XDebug no seu projeto utilizando o Docker!</p>
<p>Agora sempre que voc&ecirc; adicionar um breakpoint &agrave; sua aplica&ccedil;&atilde;o, estiver com o xDebug ativado e acessar o caminho desejado, voc&ecirc; poder&aacute; monitorar e manipular os valores desejados em tempo de execu&ccedil;&atilde;o.</p>
<p>Lembrando que esse tutorial foi desenvolvido com o foco para PHPStorm, mas o mesmo &eacute; v&aacute;lido para quem trabalha com outros clients com suporte ao XDebug.</p>
<p>Espero que tenha gostado! Qualquer d&uacute;vida ou sugest&atilde;o de melhoria, entre em contato ou mande um pull request que ser&aacute; muito bem vindo!</p>
<p>Abra&ccedil;o!</p>
