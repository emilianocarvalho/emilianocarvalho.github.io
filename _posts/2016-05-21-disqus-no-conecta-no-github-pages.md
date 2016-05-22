---
layout: post
title: "Disqus não conecta no GitHub Pages"
date: "2016-05-21 20:22:37 -0300"
---

## Estou recebendo a mensagem "Não foi possível carregar Disqus."

Já havia um tempo que tinha criado minha GitHub Pages para montar com Jekyll, mas não tinha organizado ainda a estrutura. Estava pensando em usar o Semantic.UI ao invés do já explorado Bootstrap, essas coisas mas como estava no final de curso deixei de lado.

Bem, de passagem pelo Facebook encontrei um compartilhamento de um curso do [Willian Justen][1], excelente vale a pena fazer, é gratuito, e como já estava na hora, por que não aproveitar o curso?

Depois de tudo configurado, versionado no github, finalmente estava lá. Github Pages perfeito.

Sólo un detalle. No curso do [Willian Justen][1] ele mostra como adicionar o Disqus, até aí tudo bem, sem definir as variáveis url de nossa página e o identificador de página, como no exemplo abaixo: (disponibilizada pelo Disqus para que você coloque no seu site, que vem comentadas)

{% highlight javascript %}
var disqus_config = function () {
  this.page.url = PAGE_URL; // Replace PAGE_URL with your page's canonical URL variable
  this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
{% endhighlight %}

Mas ao definir com as variáveis do Jekyll configuradas para minha Github Pages

{% highlight javascript %}
var disqus_config = function () {
  this.page.url = '{{ site.url }}{{ site.baseurl }}{{ page.url }}';
  this.page.identifier = '{{ page.url }}';
};
{% endhighlight %}

não passou a reconhecer, apresentando a mensagem acima "We were unable to load Disqus."

## Como resolví

Ao deixar as variáveis comentadas o Disqus carrega, mas ao você deixar seu comentário ele não referencia corretamente o post que você comentou, ou seja, perdemos o link para este post.

A solução foi adicionar o protocolo `http:` ao meu endereço do GitHub Page, no arquivo de configurações `_config.yml`.

url: "http://emilianocarvalho.github.io"

Pronto, Github Page criada com Jekyll e Disqus ativo, vinculado a minha conta.

[1]: http://willianjusten.teachable.com/courses/criando-sites-estaticos-com-jekyll "Willian Justen"
