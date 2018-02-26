---
layout: post
status: publish
published: true
title: Docker + PHPUnit
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 494
wordpress_url: http://viniciusfesil.com.br/?p=494
date: '2017-09-04 17:02:05 -0300'
date_gmt: '2017-09-04 17:02:05 -0300'
categories:
- PHP
- Docker
tags:
- php
- Docker
- phpunit
- docker-compose
- composer
comments: []
---
<p>Recentemente precisei de um <strong>Stack Docker</strong> que teria uma &uacute;nica responsabilidade, aplicar testes unit&aacute;rios. Pesquisei em alguns locais e achei alguns coisas pr&oacute;ximas do que eu estava precisando, mas n&atilde;o um conjunto de &nbsp;com o essencial para trabalhar com os testes.</p>
<p>Portanto criei o reposit&oacute;rio <strong>vinnyfs89/docker-phpunit</strong> pra facilitar a vida de quem gostaria de fazer o mesmo que eu.</p>
<p>Pra utilizar o reposit&oacute;rio &eacute; muito simples:</p>
<ul>
<li>Clone o reposit&oacute;rio</li>
<li>Duplique e renomei o arquivo <strong>composer.json_example</strong> para <strong>composer.json</strong></li>
<li>Duplique e renomei os arquivos <strong>docker-compose.yml_example</strong> para <strong>docker-compose.yml</strong></li>
<li>Execute o comando <strong>docker-compose up</strong> (ou execute<strong> docker-compose up -d</strong> caso deseje iniciar seus containers em background)</li>
</ul>
<p>Um diferencial bacana desse reposit&oacute;rio &eacute; que ele possui um servi&ccedil;o espec&iacute;fico para o <strong>composer</strong> para fazer a gerencia de pacotes atrav&eacute;s do projeto.</p>
<p>Clique no link abaixo para visitar o reposit&oacute;rio: <a href="https://github.com/vinnyfs89/docker-phpunit"><code>https://github.com/vinnyfs89/docker-phpunit</code></a></p>
<p>https://github.com/vinnyfs89/docker-phpunit</p>
<p>Espero que os ajude.</p>
<p>&nbsp;</p>
