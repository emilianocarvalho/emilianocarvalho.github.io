---
layout: post
title: "Github sincronizando fork com o original"
date: "2016-10-11 23:33:37 -0300"
---

## Como sincronizar um fork com o projeto original

Antes de tudo, pra quem não esta familiarizado com o mundo open-source, [fork][1] é uma bifurcação de um projeto de software, quando disponibilizado pelo criador ou equipe de desenvolvimento que normalmente compartilham seu código fonte original. Você tem que fazer isso se quiser contribuir com o projeto.

A idéia aqui é definir não apenas como sincronizar com o projeto original, mas principalmento um roteiro de atualização diária, de forma que, tanto o seu projeto local quando o original fiquem atualizados.

### As etapas para que se mantenha atualizado o projeto "copiado"

1. Entrar no github e no projeto que você deseja contribuir clicar no botão `Fork a Project` ![Fork a project](images/fork-github.png)
2. Clonar o repositório na sua máquina `git clone <repositório>`
3. Verificar os remotes adicionados `git remote -v`
4. Adicionar o repositório "forkado" do projeto disponibilizado pelo criador ou equipe de desenvolvimento.
  - `git remote add <nome-para-o-repositório-original> <repositório-original>`
5. Verifique novamente os remotes adicionados e veja se ele foi adicionado `git remote -v`
6. Busque se há alguma atualização no repositório original `git fetch <repositório-original>`.
7. Cheque o seu fork local `git checkout master`
8. Agora você faz um "merge" entre o repositório original e o seu local
  - `git merge <nome-para-o-repositório-original>/master`
9. Seguir sua rotina de versionamento usando `git status, add, commit e push`
10. Submeter para o repositório original as alterações feitas no seu repositório local que você acabou de subir para o Github realizando um [Pull Request][2]

> Mesclar (merge) as alterações do **repositório-original / master** em seu branch master local faz com que seu **branch master fork** local em sincronismo com o **repositório original**, sem perder as suas alterações locais

A seguir vejam os passos que devem ser seguidos para mantê-lo atualizado na sua rotina diária.

## Rotina de trabalho

Depois de ter seguido o roteiro para realizar sua atualização inicial vamos para o roteiro que deve ser usado no dia a dia para sempre manter seu código atualizado.


### Início das atividades
Após você ter executado seu `git push origin master` e ter submetido suas alterações ao repositório original com o `New Pull Request`, **no dia anterior**,  você deve checar se houveram alterações no repositório original de forma a não deixar o seu branch master local desatualizado. Então deve seguir os seguintes passos:

1. Busque se há alguma alteração no repositório original com
  + `git fetch <nome-para-o-repositório-original>`
2. Faça um "merge" do repositório original com o seu local para ficarem atualizados
  + `git merge <nome-para-o-repositório-original>/master`

### Final do dia
...

[1]: https://pt.wikipedia.org/wiki/Bifurca%C3%A7%C3%A3o "Fork"
[2]: https://help.github.com/articles/creating-a-pull-request/ "Pull Request"
