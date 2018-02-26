---
layout: post
status: publish
published: true
title: Tutorial Gulp - Guia para iniciantes
author:
  display_name: admin
  login: admin
  email: viniciusfesil@gmail.com
  url: ''
author_login: admin
author_email: viniciusfesil@gmail.com
wordpress_id: 393
wordpress_url: http://viniciusfesil.com.br/?p=393
date: '2016-08-03 08:00:17 -0300'
date_gmt: '2016-08-03 08:00:17 -0300'
categories:
- NodeJS
tags:
- O que &eacute; o Gulp
- Grunt
- Gulp
- Gulp x Grunt
- Grunt x Gulp
- SASS
- CSS
- NodeJS
- npm
- gulpfile.js
- package.json
- gulp globalmente
- gulp4beginner
- github
comments: []
---
<p>J&aacute; faz algum tempo que fiquei interessado por ferramentas que facilitam pap&eacute;is que fazemos manualmente, automatizando rotinas e simplificando a nossa forma de trabalhar.</p>
<p>Antes de mais nada, quero deixar bem claro que eu <strong>n&atilde;o tenho nada contra</strong> quem utiliza o <strong>Grunt</strong>. Eu mesmo vinha o utilizando at&eacute; pouco tempo atr&aacute;s. Vou procurar ensinar para voc&ecirc; de uma maneira que fique mais claro, beleza?</p>
<h2>O que &eacute; o Gulp?</h2>
<p>&Eacute; uma ferramenta de automa&ccedil;&atilde;o que pode ser utilizada em seus projetos de forma simples e r&aacute;pida. Com ele &eacute; poss&iacute;vel criar tarefas e delegar responsabilidades que s&atilde;o executadas em tempo real.</p>
<h2>Porque usar o Gulp?</h2>
<p>O <strong>Gulp</strong>, assim como o <strong>Grunt</strong>, possui ferramentas que possibilitam a minifica&ccedil;&atilde;o e valida&ccedil;&atilde;o de c&oacute;digo-fonte em tempo real, convers&atilde;o de c&oacute;digo <strong>SASS</strong> para <strong>CSS</strong>, unifica&ccedil;&atilde;o de arquivos, cria&ccedil;&atilde;o de tarefas, watchers e muito mais.</p>
<p>Talvez seria mais simples para mim perguntar para voc&ecirc;, porque n&atilde;o utilizar o <strong>Gulp</strong>?</p>
<h2>Gulp x Grunt , qual o mais r&aacute;pido?</h2>
<p>Pelo o que pude observar em meus testes com as vers&otilde;es mais atuais do <strong>Gulp</strong> e <strong>Grunt</strong>, a velocidade e "fluidez" com o qual foi poss&iacute;vel criar e testar um c&oacute;digo-fonte, o <strong>Gulp</strong> acabou saindo na frente.</p>
<h2>O que preciso para come&ccedil;ar?</h2>
<p>Basicamente voc&ecirc; precisar ter instalado o <strong>NodeJS&nbsp;</strong>em seu ambiente. Com ele instalado voc&ecirc; j&aacute; poder&aacute; utilizar&nbsp;o Gerenciador de Pacotes do Node, chamado de <strong>npm</strong>.</p>
<p>Com o <strong>npm</strong> &eacute; poss&iacute;vel executar diversas opera&ccedil;&otilde;es&nbsp;e trabalhar com&nbsp;pacotes que podem ficar versionados em um reposit&oacute;rio online, globalmente para que possa ser utilizado em qualquer lugar da sua m&aacute;quina ou mesmo localmente em uma pasta espec&iacute;fica de sua m&aacute;quina</p>
<p>Mais informa&ccedil;&otilde;es sobre <strong>npm</strong>, clique <a href="http://nodebr.com/o-que-e-a-npm-do-nodejs/" target="_blank">aqui</a>.</p>
<p>Crie um diret&oacute;rio com o nome de sua prefer&ecirc;ncia e entre nele.</p>
<pre>$ sudo mkdir gulp4beginner &amp;&amp; cd gulp4beginner;</pre>
<p>Inicie um projeto node dentro da pasta criada utilizando.</p>
<pre>$ git init</pre>
<p>Ao executar esse comando automaticamente ser&aacute; criado um arquivo chamado "<strong>package.json</strong>". Nele contem as informa&ccedil;&otilde;es sobre seu projeto tais como nome, vers&atilde;o, depend&ecirc;ncias e outros.</p>
<p><img class="aligncenter size-full wp-image-399" src="http://viniciusfesil.com.br/wp-content/uploads/2016/08/gulp.png" alt="gulp" width="960" height="593" /></p>
<h2>Instalando o Gulp</h2>
<p>O Gulp, apesar de ser baixado como um pacote do NodeJS, precisa ser executado como uma aplica&ccedil;&atilde;o. Para que possamos utilizar ele desta maneira, precisamos instalar o Gulp globalmente.</p>
<p>Digite o c&oacute;digo abaixo para instala-lo globalmente:</p>
<pre><span class="pln">$ npm install --global gulp</span></pre>
<p>Para saber se ele foi instalado corretamente digite o c&oacute;digo abaixo e dever&aacute; ser exibida a vers&atilde;o atual do Gulp.</p>
<pre>$ gulp -v</pre>
<p>No meu caso foi exibida a vers&atilde;o abaixo. Caso queira buscar e analisar melhor o pacote, voc&ecirc; pode acessar diretamente por esse <a href="https://www.npmjs.com/package/gulp" target="_blank">link</a> e conferir as novidades.</p>
<h2>Instalando e Utilizando Plugins para o Gulp</h2>
<p>Na raiz de nosso projeto adicione&nbsp;um arquivo chamado "<strong>gulpfile.js</strong>". Nele ficar&atilde;o as informa&ccedil;&otilde;es que ser&atilde;o executadas quando o comando "<strong>gulp</strong>" for executado.</p>
<p>Para que nossa automa&ccedil;&atilde;o tenha&nbsp;mais op&ccedil;&otilde;es de funcionamento precisamos instalar alguns plugins:</p>
<pre><span class="pln">npm install gulp gulp</span><span class="pun">-</span><span class="pln">jshint gulp<span class="pun">-</span><span class="pln">concat </span>gulp</span><span class="pun">-</span><span class="pln">uglify gulp-watch </span><span class="pun">--</span><span class="pln">save</span><span class="pun">-</span><span class="pln">dev</span></pre>
<p>Note que foram instalados 4 pacotes dentro da pasta do projeto Node. Eles ficar&atilde;o localizados dentro de "node_modules".</p>
<p>O comando "--save-dev" ao final do c&oacute;digo, indica que al&eacute;m de baixar e instalar os pacotes, atualizar&aacute; o arquivo "package.json" com as depend&ecirc;ncias e vers&otilde;es que est&atilde;o sendo utilizadas.</p>
<p>Abra o arquivo&nbsp;"<strong>gulpfile.js</strong>" e adicione o conte&uacute;do&nbsp;a seguir:</p>
<pre>var gulp = require("gulp");
var uglify = require("gulp-uglify");
var watch = require("gulp-watch");
var jshint = require("gulp-jshint");
var concat = require("gulp-concat");</pre>
<h2>Executando o Gulp</h2>
<p>Na pasta onde est&aacute; localizado seu arquivo "<strong>gulpfile.js</strong>" execute:</p>
<pre>$ gulp</pre>
<p>Por padr&atilde;o, o segundo par&acirc;metro ap&oacute;s o "gulp" &eacute; o nome da tarefa que voc&ecirc; criou, se voc&ecirc; n&atilde;o informar nada logo ap&oacute;s o comando acima, o Gulp buscar&aacute; uma tarefa chamada "<strong>default</strong>" dentro do seu "<strong>gulpfile.js</strong>".</p>
<p>Ent&atilde;o vamos cria-la:</p>
<pre>var gulp = require("gulp");
var uglify = require("gulp-uglify");
var watch = require("gulp-watch");
var jshint = require("gulp-jshint");
var concat = require("gulp-concat");

gulp.task("default", function () {
 gutil.log("Gulp default task is working!");
});</pre>
<p>Nesse caso, ao executar novamente o "gulp" seria impresso no console a seguinte informa&ccedil;&atilde;o:</p>
<pre>Gulp default task is working!</pre>
<p>Viu como &eacute; f&aacute;cil? Ent&atilde;o vamos adicionar mais algumas tarefas?</p>
<pre>var gulp = require("gulp");
var uglify = require("gulp-uglify");
var watch = require("gulp-watch");
var jshint = require("gulp-jshint");
var concat = require("gulp-concat");

gulp.task("default", function () {

 gutil.log("Gulp is working!");
 gulp.start('watch');
});


gulp.task('uglify', function () {

 gutil.log('Starting uglifyJS task.');
 gulp.src(['src/js/**/*.js'])
 .pipe(uglifyJS())
 .pipe(gulp.dest('build/js'));
});

gulp.task('concat', function() {

 gutil.log('Starting concatJS task.');
 gulp.src('build/js/**/*.js')
 .pipe(concat('all_files_concated.js'))
 .pipe(gulp.dest('build'));
});

gulp.task('jshint', function () {

 gutil.log('Starting jshint task.');
 return gulp.src('src/js/**/*.js')
 .pipe(jshint())
 .pipe(jshint.reporter('jshint-stylish'));
});

gulp.task('watch', function () {

 gutil.log('Starting watch task.');
 gulp.watch('src/js/**/*.js', function (event) {
 gutil.log('File ' + event.path + ' was ' + event.type + ', running tasks...');
 gulp.start('jshint');
 gulp.start('uglify');
 gulp.start('concat');
 });

});</pre>
<h2>Conclus&atilde;o</h2>
<p>At&eacute; o momento o Gulp se mostrou muito pr&aacute;tico, veloz&nbsp;e tem aumentado a produtividade pois acredito que tem facilitado as manuten&ccedil;&otilde;es e processos de melhoria.</p>
<p>Criei um reposit&oacute;rio no github chamado "<strong>gulp4beginner</strong>" e pode ser acessado clicando <a href="https://github.com/vinnyfs89/gulp4beginner">aqui</a>. Esse reposit&oacute;rio, cont&eacute;m&nbsp;o c&oacute;digo-fonte completo que criei e mais algumas informa&ccedil;&otilde;es!</p>
<h2></h2>
