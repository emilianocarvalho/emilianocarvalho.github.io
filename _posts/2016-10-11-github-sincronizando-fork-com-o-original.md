---
layout: post
title: "Github sincronizando fork com o original"
date: "2016-10-11 23:33:37 -0300"
---

### Como sincronizar um fork com o projeto original

Antes de tudo, pra quem não esta familiarizado com o mundo open-source, [fork][1] é uma bifurcação de um projeto de software, quando disponibilizado pelo criador ou equipe de desenvolvimento que normalmente compartilham seu código fonte original. Você tem que fazer isso

As etapas para que se tenha automatizado esse processo de pelo seu projeto "copiado", podemos dizer dessa forma, seria entrar no github e no projeto que você deseja contribuir clicar no botão `Fork a Project`. 

A seguir vejam os passos que devem ser seguidos para configurar bem o seu fork.


### Configurar o remote

Primeiro faça o controle do projeto original.

Abra o terminal, o Git Bash (Windows).

Veja quais repositórios remotos você tem configurado.
{% highlight javascript %}
$ git remote -v
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
{% endhighlight javascript %}

### Como resolver



[1]: https://pt.wikipedia.org/wiki/Bifurca%C3%A7%C3%A3o "Fork"
