---
layout: post
status: publish
published: true
title: "[SQL Server] - Procurar coluna em tabelas"
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 32
wordpress_url: http://viniciusfesil.wordpress.com/?p=32
date: '2013-01-29 17:36:13 -0200'
date_gmt: '2013-01-29 17:36:13 -0200'
categories:
- SQL Server
tags: []
comments: []
---
<p>Segue o script para procurar coluna em tabelas do SQL Server.</p>
<p>SELECT TABLE_NAME as tabela,<br />
COLUMN_NAME as coluna<br />
FROM INFORMATION_SCHEMA.COLUMNS<br />
where column_name LIKE '%limite%'</p>
<p>&nbsp;</p>
<p>Espero os que ajude.</p>
