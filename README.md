[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/joserochadocarmo/ufg-eventos)

# \<ufg-eventos\>

Webcomponente de eventos da UFG - Universidade Federal de Goiás

[DEMO](https://joserochadocarmo.github.io/ufg-eventos)
[PRODUCTION](https://www.ufg.br/events)

Example Usage:

<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="ufg-eventos.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->

```html
<ufg-eventos></ufg-eventos>
```

### Instalação

Pra rodar você precisa de um HTTP Server, o Chrome tem uma extensão que resolve este problema de forma bem simples.

[Web Server for Chrome](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb)

Faça uma cópia do projeto para seu computador
```
git clone https://github.com/joserochadocarmo/ufg-eventos.git && cd ufg-eventos
```

Rode o seguinte comando(não modifique) dentro da pasta, é necessario ter docker instalado:

```
docker run --rm -it -v $(pwd):/home/node/app -u node fresnizky/polymer-cli bower install --allow-root
```

Pronto! agora é só acessar pelo navegador, procurar pela extensão WebServer, selecionar a pasta do projeto e acessar o IP que está lá, geralmente http://127.0.0.1:8887. Agora é só trabalhar.

### Build

Simples como comprar um Bitcoin, basta rodar o comando abaixo dentro da pasta raiz do projeto.
Feito o build, ele cria dentro da pasta "copy_my_inner_content" um arquivo chamado ufg-eventos.html.
Esse arquivo é seu build, basta copiá-lo e colocar em qualquer lugar de qualquer projeto(nginx,apache,angular...).

```
docker run --rm -it -v $(pwd):/home/node/app -u node fresnizky/polymer-cli polymer build
```

### Implantação

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/webcomponentsjs/1.0.1/webcomponents-lite.js"></script>
<link rel="import" href="https://xxxxx/xxxx/ufg-eventos.html">
```

IMPORTANTE: No nosso caso, vc deve copiar o arquivo de build(ufg-eventos.html) para a pasta docs deste projeto! Porquê? Porque usamos o github como servidor:
```html
<link rel="import" href="https://joserochadocarmo.github.io/ufg-eventos/ufg-eventos.html">
```