---
layout: post
title: "Titulo da noticia"
date: "2018-02-14 20:22:37 -0300"
---

### Manchete

Já havia um tempo que tinha criado minha GitHub Pages para montar com Jekyll, mas não tinha organizado ainda a estrutura. Estava pensando em usar o Semantic.UI ao invés do já explorado Bootstrap, essas coisas, mas como estava no final de curso deixei de lado.

Bem, de passagem pelo Facebook encontrei um compartilhamento de um curso do [Willian Justen][1], excelente, vale a pena fazer, é gratuito, e como já estava na hora, por que não aproveitar o curso?

Depois de tudo configurado, versionado no github, finalmente estava lá. Github Pages perfeito.

Sólo un detalle. No curso do [Procon PB][1] ele mostra como adicionar o Disqus, até aí tudo bem, sem definir as variáveis url de nossa página e o identificador de página, como no exemplo abaixo: (disponibilizada pelo Disqus para que você coloque no seu site, que vem comentadas)


Mas ao definir com as variáveis do Jekyll configuradas para minha Github Pages


não passou a reconhecer, apresentando a mensagem acima "We were unable to load Disqus."

### Como resolver

Ao deixar as variáveis comentadas o Disqus carrega, mas ao você deixar seu comentário ele não referencia corretamente o post que você comentou, ou seja, perdemos o link para este post.

A solução foi adicionar o protocolo `http:` ao meu endereço do GitHub Page, no arquivo de configurações `_config.yml`.

url: "http://emilianocarvalho.github.io"

Pronto, Github Page criada com Jekyll e Disqus ativo, vinculado a minha conta.

[1]: http://procon.pb.gov.br "Procon PB"
