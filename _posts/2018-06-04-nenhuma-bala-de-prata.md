---
layout: post
title: "Nenhuma bala de prata: essência e acidentes de engenharia de software"
date: "2018-06-04 10:52:37 -0300"
---

## por Frederick P. Brooks, Jr. 
De todos os monstros que preenchem os pesadelos do nosso folclore, nenhum aterroriza mais do que os lobisomens, porque eles se transformam inesperadamente do familiar em horrores. Para estes, busca-se balas de prata que magicamente podem pô-las em repouso.
O projeto de software familiar, pelo menos como visto pelo gerente não técnico, tem algo desse caráter; é geralmente inocente e direto, mas é capaz de se tornar um monstro de horários perdidos, orçamentos inflados e produtos defeituosos. Então, ouvimos gritos desesperados por uma bala de prata - algo para fazer os custos de software caírem tão rapidamente quanto os custos de hardware de computador.

Mas, ao olharmos para o horizonte de uma década, não vemos nenhuma bala de prata. Não existe um desenvolvimento único, seja na tecnologia ou na técnica de gerenciamento, que, por si só, promete uma melhoria na produtividade, na confiabilidade, na simplicidade. Neste artigo, tentarei mostrar por que, examinando tanto a natureza do problema de software quanto as propriedades das balas propostas.

O ceticismo não é pessimismo, no entanto. Embora não vejamos avanços surpreendentes - e, de fato, acredito que isso seja inconsistente com a natureza do software - muitas inovações encorajadoras estão em andamento. Um esforço disciplinado e consistente para desenvolver, propagar e explorar essas inovações deve, de fato, produzir uma melhoria de ordem de grandeza. Não há estrada real, mas há uma estrada.

O primeiro passo para o manejo da doença foi a substituição das teorias demoníacas e teorias do humor pela teoria dos germes. Esse mesmo passo, o começo da esperança, por si só frustrou todas as esperanças de soluções mágicas. Dizia aos trabalhadores que o progresso seria feito passo a passo, com grande esforço, e que um cuidado persistente e incessante teria de ser pago a uma disciplina de limpeza. Assim é com engenharia de software hoje.

## Tem que ser difícil? - Dificuldades Essenciais
Não só não há balas de prata agora em vista, a própria natureza do software torna improvável que existam invenções que farão para a produtividade, confiabilidade e simplicidade do software o que a eletrônica, os transistores e a integração em grande escala fizeram. para hardware de computador. Não podemos esperar que vejamos ganhos duplos a cada dois anos.
Primeiro, deve-se observar que a anomalia não é que o progresso do software é tão lento, mas que o progresso do hardware do computador é tão rápido. Nenhuma outra tecnologia desde o início da civilização alcançou seis ordens de magnitude no ganho de preço de desempenho em 30 anos. Em nenhuma outra tecnologia pode um optar por tomar o ganho em qualquer um melhor desempenho ou em custos reduzidos. Esses ganhos fluem da transformação da fabricação de computadores de uma indústria de montagem para uma indústria de processo.

Segundo, para ver que taxa de progresso pode-se esperar na tecnologia de software, vamos examinar as dificuldades dessa tecnologia. Seguindo Aristóteles, eu os divido em essência , as dificuldades inerentes à natureza do software e os acidentes , as dificuldades que hoje assistem à sua produção, mas não são inerentes.

A essência de uma entidade de software é uma construção de conceitos interligados: conjuntos de dados, relacionamentos entre itens de dados, algoritmos e invocações de funções. Essa essência é abstrata na medida em que tal construção conceitual é a mesma sob muitas representações diferentes. No entanto, é altamente preciso e ricamente detalhado.

Acredito que a parte difícil de construir software seja a especificação, o design e o teste desse constructo conceitual, não o trabalho de representá-lo e testar a fidelidade da representação . Ainda fazemos erros de sintaxe, com certeza; mas eles são confusos em comparação com os erros conceituais na maioria dos sistemas.

Se isso for verdade, construir software sempre será difícil. Não há inerentemente nenhuma bala de prata.

Vamos considerar as propriedades inerentes a essa essência irredutível dos sistemas de software modernos: complexidade, conformidade, mutabilidade e invisibilidade.

### Complexidade. 
As entidades de software são mais complexas para seu tamanho do que, talvez, qualquer outra construção humana, porque não há duas partes iguais (pelo menos acima do nível de instrução). Se eles são, nós fazemos as duas partes similares em uma sub-rotina - aberta ou fechada. Nesse aspecto, os sistemas de software diferem profundamente de computadores, edifícios ou automóveis, onde elementos repetidos são abundantes.

Os computadores digitais são, eles próprios, mais complexos do que a maioria das coisas que as pessoas constroem: eles têm um grande número de estados. Isso faz com que conceber, descrever e testá-los com força. Os sistemas de software têm mais estados de ordem de grandeza do que os computadores.

Da mesma forma, uma ampliação de uma entidade de software não é apenas uma repetição dos mesmos elementos em tamanhos maiores, é necessariamente um aumento no número de elementos diferentes. Na maioria dos casos, os elementos interagem uns com os outros de alguma forma não linear, e a complexidade do todo aumenta muito mais do que linearmente.

A complexidade do software é uma propriedade essencial, não acidental. Assim, as descrições de uma entidade de software que abstraem sua complexidade geralmente abstraem sua essência. Por três séculos, a matemática e as ciências físicas deram grandes passos construindo modelos simplificados de fenômenos complexos, derivando propriedades dos modelos e verificando essas propriedades por meio de experimentos. Este paradigma funcionou porque as complexidades ignoradas nos modelos não eram as propriedades essenciais dos fenômenos. Não funciona quando as complexidades são a essência.

Muitos dos problemas clássicos do desenvolvimento de produtos de software derivam dessa complexidade essencial e seu aumento não-linear aumenta com o tamanho. Da complexidade vem a dificuldade de comunicação entre os membros da equipe, o que leva a falhas de produto, custos excessivos, atrasos no cronograma. Da complexidade, vem a dificuldade de enumerar, muito menos compreender, todos os estados possíveis do programa, e daí vem a falta de confiabilidade. Da complexidade da função vem a dificuldade de invocar a função, o que torna os programas difíceis de usar. Da complexidade da estrutura vem a dificuldade de estender programas a novas funções sem criar efeitos colaterais. Da complexidade da estrutura, vêm os estados não visualizados que constituem alçapões de segurança.

Não apenas problemas técnicos, mas problemas de gerenciamento também vêm da complexidade. Isso torna a visão geral difícil, impedindo assim a integridade conceitual. Isso torna difícil encontrar e controlar todas as pontas soltas. Cria o tremendo fardo de aprendizado e compreensão que torna a rotatividade de pessoal um desastre.

### Conformidade. 
As pessoas de software não estão sozinhas em enfrentar a complexidade. A física lida com objetos terrivelmente complexos, mesmo no nível de partículas "fundamentais". O físico trabalha, no entanto, com a firme fé de que existem princípios unificadores a serem encontrados, seja em quarks ou em teorias de campo unificado. Einstein argumentou que deve haver explicações simplificadas da natureza, porque Deus não é caprichoso ou arbitrário.

Nenhuma dessas crenças conforta o engenheiro de software. Grande parte da complexidade que ele deve dominar é uma complexidade arbitrária, forçada sem rima ou razão pelas muitas instituições e sistemas humanos aos quais suas interfaces devem obedecer. Elas diferem de interface para interface e, de tempos em tempos, não por necessidade, mas apenas porque foram projetadas por pessoas diferentes, e não por Deus.

Em muitos casos, o software deve estar em conformidade porque é a chegada mais recente à cena. Em outros, deve se conformar porque é percebido como o mais adequado. Mas em todos os casos, muita complexidade vem da conformação para outras interfaces; essa complexidade não pode ser simplificada por qualquer redesenho do software sozinho.

### Mutabilidade. 
A entidade de software está constantemente sujeita a pressões por mudança. Claro, também são prédios, carros, computadores. Mas as coisas fabricadas raramente são alteradas após a fabricação; elas são substituídas por modelos posteriores, ou mudanças essenciais são incorporadas em cópias posteriores de números de série do mesmo design básico. As chamadas de retorno dos automóveis são realmente muito raras; alterações de campo de computadores um pouco menos. Ambos são muito menos frequentes do que modificações no software em campo.

Em parte, isso ocorre porque o software de um sistema incorpora sua função, e a função é a parte que mais sente as pressões da mudança. Em parte, é porque o software pode ser mudado mais facilmente - é puro material de pensamento, infinitamente maleável. Os edifícios, de fato, mudam, mas os altos custos da mudança, entendidos por todos, servem para amortecer os caprichos dos cambistas.

Todo o software bem sucedido é alterado. Dois processos estão no trabalho. Primeiro, como um produto de software é útil, as pessoas o experimentam em novos casos na borda ou além do domínio original. As pressões para a função estendida vêm principalmente de usuários que gostam da função básica e inventam novos usos para ela.

Em segundo lugar, o software bem-sucedido sobrevive além da vida normal do veículo da máquina para o qual foi escrito pela primeira vez. Se não forem novos computadores, pelo menos novos discos, novos monitores, novas impressoras aparecerão; e o software deve estar em conformidade com seus novos veículos de oportunidade.

Em suma, o produto de software está embutido em uma matriz cultural de aplicativos, usuários, leis e veículos de máquinas. Tudo isso muda continuamente, e suas mudanças inexoravelmente forçam a mudança no produto de software.

### Invisibilidade. 
O software é invisível e não visualizável. Abstrações geométricas são ferramentas poderosas. A planta de um prédio ajuda o arquiteto e o cliente a avaliar espaços, fluxos de tráfego, visualizações. Contradições e omissões se tornam óbvias. Desenhos de escala de peças mecânicas e modelos de moléculas de bonecos, embora abstrações, servem ao mesmo propósito. Uma realidade geométrica é capturada em uma abstração geométrica.

A realidade do software não é inerentemente incorporada no espaço. Portanto, ele não tem representação geométrica pronta na maneira que a terra tem mapas, chips de silício têm diagramas, computadores têm esquemas de conectividade. Assim que tentamos diagramar a estrutura do software, achamos que ela constitui não um, mas vários, gráficos gerais dirigidos sobrepostos uns sobre os outros. Os vários gráficos podem representar o fluxo de controle, o fluxo de dados, padrões de dependência, seqüência de tempo, relações de nome-espaço. Esses gráficos geralmente não são nem planares, muito menos hierárquicos. De fato, uma das maneiras de estabelecer o controle conceitual sobre essa estrutura é impor o corte de links até que um ou mais dos gráficos se tornem hierárquicos. [1]

Apesar do progresso em restringir e simplificar as estruturas de software, elas permanecem inerentemente não visualizáveis ​​e, portanto, não permitem que a mente use algumas de suas ferramentas conceituais mais poderosas. Essa falta não apenas impede o processo de design dentro de uma mente, mas também dificulta a comunicação entre as mentes.

## Avanços Passados ​​Resolvidos Dificuldades Acidentais
Se examinarmos os três passos no desenvolvimento da tecnologia de software que foram mais frutíferos no passado, descobrimos que cada um atacou uma grande dificuldade diferente na construção de software, mas que essas dificuldades foram acidentais, não essenciais, dificuldades. Também podemos ver os limites naturais para a extrapolação de cada um desses ataques.
Idiomas de alto nível. Certamente, o golpe mais poderoso para produtividade, confiabilidade e simplicidade de software tem sido o uso progressivo de linguagens de alto nível para programação. A maioria dos observadores credita esse desenvolvimento com pelo menos um fator de cinco em produtividade e com ganhos concomitantes em confiabilidade, simplicidade e compreensibilidade.

O que uma linguagem de alto nível realiza? Liberta um programa de grande parte da sua complexidade acidental. Um programa abstrato consiste em construções conceituais: operações, tipos de dados, seqüências e comunicação. O programa da máquina de concreto está preocupado com bits, registros, condições, ramificações, canais, discos e outros. Na medida em que a linguagem de alto nível incorpora os construtos que se deseja no programa abstrato e evita todos os menores, elimina todo um nível de complexidade que nunca foi inerente ao programa.

O máximo que uma linguagem de alto nível pode fazer é fornecer todas as construções que o programador imagina no programa abstrato. Para ter certeza, o nível de nosso pensamento sobre estruturas de dados, tipos de dados e operações está aumentando constantemente, mas a uma taxa cada vez menor. E o desenvolvimento da linguagem aproxima-se cada vez mais da sofisticação dos usuários.

Além disso, em algum momento, a elaboração de uma linguagem de alto nível cria um fardo de domínio de ferramentas que aumenta, não reduz, a tarefa intelectual do usuário que raramente usa as construções esotéricas.

### Compartilhamento de tempo. 
O compartilhamento de tempo trouxe uma grande melhoria na produtividade dos programadores e na qualidade de seu produto, embora não tão grande quanto a trazida pelas linguagens de alto nível.

O compartilhamento de tempo ataca uma dificuldade bem diferente. A partilha de tempo preserva o imediatismo e, portanto, permite manter uma visão geral da complexidade. A lenta reviravolta da programação em lote significa que inevitavelmente esquecemos as minúcias, se não o próprio impulso, do que se estava pensando quando ele parou de programar e pediu compilação e execução. Essa interrupção é dispendiosa no tempo, pois é preciso refrescar a memória. O efeito mais sério pode muito bem ser a decadência de tudo o que está acontecendo em um sistema complexo.

O retorno lento, assim como as complexidades da linguagem de máquina, é uma dificuldade acidental, e não essencial, do processo de software. Os limites da contribuição potencial do tempo compartilhado derivam diretamente. O principal efeito do tempo compartilhado é encurtar o tempo de resposta do sistema. À medida que esse tempo de resposta chega a zero, em algum momento ele ultrapassa o limiar humano de noticiabilidade, cerca de 100 milissegundos. Além desse limiar, não há benefícios esperados.

### Ambientes de programação unificada. 
O Unix e o Interlisp, os primeiros ambientes de programação integrados a serem amplamente utilizados, parecem ter melhorado a produtividade por fatores integrais. Por quê?

Eles atacam as dificuldades acidentais que resultam do uso de programas individuais juntos, fornecendo bibliotecas integradas, formatos de arquivos unificados e canais e filtros. Como resultado, estruturas conceituais que, em princípio, poderiam sempre chamar, alimentar e usar uma a outra podem, de fato, facilmente fazê-lo na prática.

Essa inovação, por sua vez, estimulou o desenvolvimento de bancadas inteiras, já que cada nova ferramenta poderia ser aplicada a qualquer programa que usasse os formatos padrão.

Devido a esses sucessos, os ambientes são objeto de grande parte das pesquisas de engenharia de software atuais. Nós olhamos para suas promessas e limitações na próxima seção.

## Esperanças para a Prata

Agora vamos considerar os desenvolvimentos técnicos que são mais frequentemente avançados como potenciais balas de prata. Quais problemas eles abordam - os problemas da essência ou as dificuldades acidentais remanescentes? Eles oferecem avanços revolucionários ou incrementais?

### Ada e outros avanços de linguagem de alto nível.
Um dos desenvolvimentos recentes mais elogiados é Ada, uma linguagem de alto nível de propósito geral dos anos 80. A Ada não apenas reflete melhorias evolucionárias em conceitos de linguagem, mas na verdade incorpora recursos para incentivar o design moderno e a modularização. Talvez a filosofia Ada seja mais um avanço do que a linguagem Ada, pois é a filosofia de modularização, de tipos de dados abstratos, de estruturação hierárquica. Ada é super-rica, um resultado natural do processo pelo qual os requisitos foram colocados em seu design. Isso não é fatal, pois vocabulários de trabalho subconjuntos podem resolver o problema de aprendizado, e os avanços de hardware nos darão o MIPS barato para pagar os custos de compilação. O avanço da estruturação de sistemas de software é realmente um bom uso para o aumento de MIPS que nossos dólares comprarão. Sistemas operacionais,

No entanto, Ada não irá provar ser a bala de prata que mata o monstro de produtividade de software. Afinal de contas, é apenas mais uma linguagem de alto nível, e a maior recompensa dessas linguagens veio da primeira transição - a transição das complexidades acidentais da máquina para a declaração mais abstrata de soluções passo-a-passo. Uma vez que esses acidentes tenham sido removidos, os restantes serão menores, e a recompensa de sua remoção será certamente menor.

Eu prevejo que, daqui a uma década, quando a eficácia da Ada for avaliada, será visto que ela fez uma diferença substancial, mas não por causa de qualquer característica particular da linguagem, nem por causa de todas elas combinadas. Os novos ambientes Ada também não serão a causa das melhorias. A maior contribuição de Ada será que a mudança para ele ocasionou programadores de treinamento em técnicas modernas de design de software.

### Programação orientada a objetos. 
Muitos estudantes da arte esperam mais por programação orientada a objetos do que por qualquer outra modalidade técnica do dia. [2] Eu estou entre eles. Mark Sherman, da Dartmouth, observa na CSnet News que é preciso ter cuidado para distinguir duas ideias separadas que têm esse nome: tipos de dados abstratos e tipos hierárquicos . O conceito do tipo de dado abstrato é que o tipo de um objeto deve ser definido por um nome, um conjunto de valores apropriados e um conjunto de operações apropriadas, e não por sua estrutura de armazenamento, que deve estar oculta. Exemplos são os pacotes Ada (com tipos privados) e os módulos do Modula.

Tipos hierárquicos, como as classes de Simula-67, permitem definir interfaces gerais que podem ser refinadas, fornecendo tipos subordinados. Os dois conceitos são orthogonal_one podem ter hierarquias sem se esconder e se esconder sem hierarquias. Ambos os conceitos representam avanços reais na arte de construir software.

Cada um remove mais uma dificuldade acidental do processo, permitindo que o designer expresse a essência do design sem ter que expressar grandes quantidades de material sintático que não adicionam conteúdo de informação. Para tipos abstratos e hierárquicos, o resultado é remover um tipo de dificuldade acidental de ordem superior e permitir uma expressão de design de ordem superior.

No entanto, tais avanços não podem fazer mais do que remover todas as dificuldades acidentais da expressão do projeto. A complexidade do design em si é essencial, e tais ataques não alteram isso. Um ganho de ordem de grandeza pode ser feito por programação orientada a objetos somente se o underbrush desnecessário de especificação de tipo ainda presente em nossa linguagem de programação for ele mesmo nove décimos do trabalho envolvido no projeto de um produto de programa. Eu duvido.

### Inteligência artificial. 
Muitas pessoas esperam que os avanços na inteligência artificial forneçam o avanço revolucionário que proporcionará ganhos de ordem de grandeza na produtividade e na qualidade do software. [3] eu não sei. Para entender por quê, devemos dissecar o que significa "inteligência artificial".

DL Parnas esclareceu o caos terminológico: [4]

> Duas definições bastante diferentes de IA são comuns hoje em dia. AI-1: O uso de computadores para resolver problemas que  antes só podiam ser resolvidos com a aplicação da inteligência humana. Al-2: O uso de um conjunto específico de técnicas de programação conhecidas como programação heurística ou baseada em regras. Nessa abordagem, especialistas humanos são estudados para determinar quais heurísticas ou regras práticas usam na solução de problemas ... O programa é projetado para resolver um problema da maneira como os humanos parecem resolvê-lo.

> A primeira definição tem um significado deslizante ... Algo pode se encaixar na definição de Al-1 hoje, mas, uma vez que vemos como o programa funciona e entendemos o problema, não vamos mais pensar nele como Al .... Infelizmente Não consigo identificar um corpo de tecnologia que seja exclusivo deste campo ... A maioria do trabalho é específico do problema, e alguma abstração ou criatividade é necessária para ver como transferi-lo.

Eu concordo completamente com essa crítica. As técnicas utilizadas para reconhecimento de fala parecem ter pouco em comum com aquelas utilizadas para reconhecimento de imagens, e ambas são diferentes daquelas utilizadas em sistemas especialistas. Eu tenho dificuldade em ver como o reconhecimento de imagens, por exemplo, fará qualquer diferença significativa na prática de programação. O mesmo problema é verdadeiro no reconhecimento de fala. O difícil de construir software é decidir o que se quer dizer, não dizer. Nenhuma facilitação da expressão pode dar mais do que ganhos marginais.

A tecnologia de sistemas especialistas, AI-2, merece uma seção própria.

### Sistemas especializados. 
A parte mais avançada da arte da inteligência artificial, e a mais amplamente aplicada, é a tecnologia para a construção de sistemas especialistas. Muitos cientistas de software trabalham duro para aplicar essa tecnologia ao ambiente de criação de software. [3, 5] Qual é o conceito e quais são as perspectivas?

Um *sistema especialista* é um programa que contém um mecanismo de inferência generalizada e uma base de regras, pega dados de entrada e suposições, explora as inferências deriváveis ​​da base de regras, produz conclusões e conselhos e oferece explicações para seus resultados, refazendo seu raciocínio para o usuário . Os mecanismos de inferência normalmente podem lidar com dados e regras difusos ou probabilísticos, além de lógica puramente determinística.

Esses sistemas oferecem algumas vantagens claras sobre os algoritmos programados projetados para chegar às mesmas soluções para os mesmos problemas:

* A tecnologia do mecanismo de inferência é desenvolvida de maneira independente do aplicativo e aplicada a muitos usos. Pode-se justificar muito esforço nos mecanismos de inferência. De fato, essa tecnologia está bem avançada.
* As partes mutáveis ​​dos materiais peculiares da aplicação são codificadas na base de regras de maneira uniforme e as ferramentas são fornecidas para desenvolver, alterar, testar e documentar a base de regras. Isso regulariza grande parte da complexidade do próprio aplicativo.

O poder de tais sistemas não vem de mecanismos de inferência cada vez mais elaborados, mas de bases de conhecimento cada vez mais ricas que refletem o mundo real com mais precisão. Acredito que o avanço mais importante oferecido pela tecnologia é a separação da complexidade da aplicação do próprio programa.

Como essa tecnologia pode ser aplicada à tarefa de engenharia de software? De muitas maneiras: Esses sistemas podem sugerir regras de interface, aconselhar sobre estratégias de teste, lembrar frequências de tipo de erro e oferecer dicas de otimização.

Considere um consultor de testes imaginário, por exemplo. Em sua forma mais rudimentar, o sistema especialista em diagnóstico é muito parecido com uma lista de verificação de um piloto, apenas enumerando sugestões quanto a possíveis causas de dificuldade. À medida que mais e mais estrutura do sistema é incorporada na base de regras, e à medida que a base de regras leva em conta mais sofisticadamente os sintomas de problemas relatados, o conselheiro de testes torna-se cada vez mais particular nas hipóteses que gera e nos testes que recomenda. Esse sistema especialista pode se afastar radicalmente dos sistemas convencionais, pois sua base de regras provavelmente deve ser modularizada hierarquicamente da mesma forma que o produto de software correspondente, de modo que, como o produto é modularmente modificado, a base de regras de diagnóstico pode ser modificada modularmente. bem.

O trabalho necessário para gerar as regras de diagnóstico é um trabalho que teria que ser feito de qualquer maneira na geração do conjunto de casos de teste para os módulos e para o sistema. Se isso for feito de uma maneira geral adequada, com uma estrutura uniforme para regras e um bom mecanismo de inferência disponível, pode realmente reduzir a mão-de-obra total gerando casos de testes e ajudar também com testes de manutenção e modificação por toda a vida. Do mesmo modo, pode-se postular outros conselheiros, provavelmente muitos e provavelmente simples, para as outras partes da tarefa de construção de software.

Muitas dificuldades impedem a realização antecipada de consultores úteis do sistema especialista para o desenvolvedor do programa. Uma parte crucial do nosso cenário imaginário é o desenvolvimento de maneiras fáceis de ir da especificação da estrutura do programa à geração automática ou semi-automática de regras de diagnóstico. Ainda mais difícil e importante é a dupla tarefa de aquisição de conhecimento: encontrar especialistas articulados e autoanalíticos que saibam por que eles fazem as coisas e desenvolver técnicas eficientes para extrair o que sabem e destilá-lo em bases de regras. O pré-requisito essencial para a construção de um sistema especialista é ter um especialista.

A contribuição mais poderosa dos sistemas especialistas certamente será colocar a serviço do programador inexperiente a experiência e a sabedoria acumulada dos melhores programadores. Esta não é uma pequena contribuição. A lacuna entre a melhor prática de engenharia de software e a prática média é muito ampla - talvez mais ampla do que em qualquer outra disciplina de engenharia. Uma ferramenta que divulgue boas práticas seria importante.

### Programação "automática". 
Por quase 40 anos, as pessoas têm antecipado e escrito sobre "programação automática", ou a geração de um programa para resolver um problema a partir de uma declaração das especificações do problema. Alguns hoje escrevem como se esperassem que essa tecnologia fornecesse o próximo avanço. [5]

Parnas [4] implica que o termo é usado para glamour, não para conteúdo semântico, afirmando,

Em suma, a programação automática sempre foi um eufemismo para programação com uma linguagem de nível mais alto do que a que estava disponível atualmente para o programador.

Ele argumenta, em essência, que na maioria dos casos é o método da solução, não o problema, cuja especificação deve ser dada.

Pode-se encontrar exceções. A técnica de construir geradores é muito poderosa, e é rotineiramente usada para uma boa vantagem em programas de classificação. Alguns sistemas de integração de equações diferenciais também permitiram a especificação direta do problema, e os sistemas avaliaram os parâmetros, escolhidos de uma biblioteca de métodos de solução, e geraram os programas.

Estas aplicações têm propriedades muito favoráveis:

Os problemas são prontamente caracterizados por relativamente poucos parâmetros.
Existem muitos métodos conhecidos de solução para fornecer uma biblioteca de alternativas.
Análises extensivas levaram a regras explícitas para a seleção de técnicas de solução, dados os parâmetros do problema.
É difícil ver como tais técnicas se generalizam para o mundo mais amplo do sistema de software comum, onde casos com propriedades tão claras são a exceção. É difícil até imaginar como esse avanço na generalização poderia ocorrer.

### Programação gráfica. 
Um assunto favorito para dissertações de doutorado em engenharia de software é a programação gráfica ou visual - a aplicação da computação gráfica ao design de software. [6, 7] Às vezes a promessa mantida por tal abordagem é postulada por analogia com o design de chip VLSI, no qual a computação gráfica desempenha um papel tão produtivo. Às vezes, o teórico justifica a abordagem considerando os fluxogramas como o meio ideal de design de programas e fornecendo recursos poderosos para construí-los.

Nada ainda convincente, muito menos emocionante, ainda emergiu de tais esforços. Estou convencido de que nada será.

Em primeiro lugar, como argumentei em outro lugar [8], o fluxograma é uma abstração muito pobre da estrutura do software. De fato, é melhor visualizá-lo como a tentativa de Burks, von Neumann e Goldstine de fornecer uma linguagem de controle de alto nível, desesperadamente necessária, para o computador proposto. Na forma lamentável, de várias páginas e em caixas de conexões, para a qual o fluxograma foi elaborado hoje, ele se mostrou inútil como uma ferramenta de design - os programadores desenham fluxogramas depois, não antes, de escrever os programas que descrevem.

Em segundo lugar, as telas de hoje são muito pequenas, em pixels, para mostrar tanto o escopo quanto a resolução de qualquer diagrama de software detalhado. A chamada "metáfora da área de trabalho" da estação de trabalho atual é, ao contrário, uma metáfora de "assento de avião". Qualquer pessoa que tenha arrastado um colo cheio de papéis enquanto estiver sentado entre dois passageiros corpulentos reconhecerá a diferença - pode-se ver apenas algumas poucas coisas ao mesmo tempo. O verdadeiro desktop fornece visão geral e acesso aleatório a uma pontuação de páginas. Além disso, quando os ajustes de criatividade são fortes, sabe-se que mais de um programador ou escritor abandonou o desktop para o andar mais espaçoso. A tecnologia de hardware terá que avançar substancialmente antes que o escopo de nossos escopos seja suficiente para a tarefa de design de software.

Mais fundamentalmente, como argumentei acima, o software é muito difícil de visualizar. Seja um fluxo de controle de diagramas, aninhamento de escopo variável, referências cruzadas variáveis, fluxo de dados, estruturas de dados hierárquicas ou qualquer outra coisa, a pessoa sente apenas uma dimensão do elefante de software intrinsecamente intertravado. Se alguém sobrepor todos os diagramas gerados pelas muitas visualizações relevantes, será difícil extrair qualquer visão global. A analogia do VLSI é fundamentalmente enganosa - um design de chip é uma descrição bidimensional em camadas cuja geometria reflete sua realização em 3-espaços. Um sistema de software não é.

### Verificação do programa 
Grande parte do esforço na programação moderna entra em testes e no reparo de bugs. Há talvez uma bala de prata a ser encontrada, eliminando os erros na fonte, na fase de projeto do sistema? A produtividade e a confiabilidade do produto podem ser radicalmente aprimoradas seguindo a estratégia profundamente diferente de provar os projetos corretos antes que o imenso esforço seja aplicado na implementação e no teste dos mesmos?

Eu não acredito que vamos encontrar mágica de produtividade aqui. A verificação do programa é um conceito muito poderoso, e será muito importante para coisas como kernels seguros de sistemas operacionais. A tecnologia não promete, no entanto, economizar mão de obra. As verificações são muito trabalhosas que apenas alguns programas substanciais já foram verificados.

A verificação do programa não significa programas à prova de erros. Não há mágica aqui também. Provas matemáticas também podem estar com defeito. Assim, enquanto a verificação pode reduzir a carga de teste do programa, ela não pode eliminá-lo.

Mais seriamente, até mesmo a verificação perfeita do programa pode apenas estabelecer que um programa atende às suas especificações. A parte mais difícil da tarefa de software é chegar a uma especificação completa e consistente, e muito da essência da criação de um programa é, na verdade, a depuração da especificação.

### Ambientes e ferramentas. 
Quanto mais ganho pode ser esperado das pesquisas explosivas em melhores ambientes de programação? A reação instintiva é que os grandes problemas - sistemas de arquivos hierárquicos, formatos uniformes de arquivos para possibilitar interfaces de programa uniformes e ferramentas generalizadas - foram os primeiros atacados e foram resolvidos. Os editores inteligentes específicos da linguagem são desenvolvimentos ainda não amplamente utilizados na prática, mas o máximo que eles prometem é a ausência de erros sintáticos e erros semânticos simples.

Talvez o maior ganho ainda a ser percebido em ambientes de programação seja o uso de sistemas integrados de banco de dados para acompanhar os inúmeros detalhes que devem ser lembrados com precisão pelo programador individual e mantidos atualizados para um grupo de colaboradores em um único sistema.

Certamente este trabalho vale a pena, e certamente trará alguns frutos em produtividade e confiabilidade. Mas, por sua própria natureza, o retorno de agora em diante deve ser marginal.

### Estações de trabalho. 
Quais ganhos são esperados para a arte do software a partir do aumento rápido e certo da capacidade de memória e energia da estação de trabalho individual? Bem, quantos MIPS podem ser usados ​​proveitosamente? A composição e edição de programas e documentos é totalmente suportada pelas velocidades de hoje. A compilação poderia ser um impulso, mas um fator de 10 na velocidade da máquina certamente deixaria a atividade dominante no dia do programador. De fato, parece ser assim agora.

Estações de trabalho mais poderosas que certamente recebemos. Realces mágicos deles não podemos esperar.

## Ataques Promissores à Essência Conceitual

Mesmo que nenhum avanço tecnológico prometa dar ao tipo de resultados mágicos com os quais estamos tão familiarizados na área de hardware, há tanto uma abundância de bom trabalho acontecendo agora quanto a promessa de progresso constante, embora não espetacular.

Todos os ataques tecnológicos aos acidentes do processo de software são fundamentalmente limitados pela equação de produtividade:

Se, como acredito, os componentes conceituais da tarefa estão agora ocupando a maior parte do tempo, então nenhuma quantidade de atividade nos componentes da tarefa que sejam apenas a expressão dos conceitos pode gerar grandes ganhos de produtividade.

Portanto, devemos considerar os ataques que abordam a essência do problema de software, a formulação dessas estruturas conceituais complexas. Felizmente, alguns desses ataques são muito promissores.

### Compre versus construir. 
A solução mais radical possível para a construção de software é não construí-lo.

Todos os dias isso se torna mais fácil, à medida que mais e mais fornecedores oferecem mais e melhores produtos de software para uma variedade estonteante de aplicativos. Embora nós, engenheiros de software, tenhamos trabalhado na metodologia de produção, a revolução do computador pessoal criou não um, mas muitos, mercados de massa para software. Cada banca traz revistas mensais, que classificam por tipo de máquina, anunciam e analisam dezenas de produtos a preços que variam de alguns dólares a algumas centenas de dólares. Fontes mais especializadas oferecem produtos muito poderosos para a estação de trabalho e outros mercados Unix. Mesmo ferramentas de software e ambientes podem ser comprados no mercado. Eu propus em outro lugar um mercado para módulos individuais. [9]

Qualquer produto desse tipo é mais barato comprar do que construir de novo. Mesmo com um custo de cem mil dólares, um software comprado está custando apenas cerca de um ano de programação. E a entrega é imediata! Imediato, pelo menos, para produtos que realmente existam, produtos cujo desenvolvedor pode encaminhar produtos para um usuário feliz. Além disso, esses produtos tendem a ser muito melhor documentados e um pouco melhor mantidos do que os softwares desenvolvidos internamente.

O desenvolvimento do mercado de massa é, acredito, a mais profunda tendência de longo prazo da engenharia de software. O custo do software sempre foi custo de desenvolvimento, não custo de replicação. Compartilhar esse custo entre alguns usuários reduz radicalmente o custo por usuário. Outra maneira de ver isso é que o uso de n cópias de um sistema de software efetivamente multiplica a produtividade de seus desenvolvedores por n . Isso é um aprimoramento da produtividade da disciplina e da nação.

A questão chave, claro, é a aplicabilidade. Posso usar um pacote disponível no mercado para executar minha tarefa? Uma coisa surpreendente aconteceu aqui. Durante as décadas de 1950 e 1960, estudo após estudo mostrou que os usuários não usariam pacotes prontos para uso para folha de pagamento, controle de estoque, contas a receber e assim por diante. Os requisitos eram muito especializados, a variação caso a caso era muito alta. Durante a década de 1980, encontramos esses pacotes em alta demanda e uso generalizado. O que mudou?

Não os pacotes, realmente. Eles podem ser um pouco mais generalizados e um pouco mais personalizáveis ​​do que antes, mas não muito. Não os aplicativos também. Se alguma coisa, as necessidades comerciais e científicas de hoje são mais diversificadas e complicadas do que as de 20 anos atrás.

A grande mudança foi na relação custo / hardware do software. Em 1960, o comprador de uma máquina de dois milhões de dólares achou que poderia pagar mais US $ 250 mil por um programa de folha de pagamento personalizado, que escorregou fácil e sem interrupções para o ambiente social hostil ao computador. Hoje, o comprador de uma máquina de escritório de US $ 50.000 não pode pagar por um programa de folha de pagamento personalizado, então ele adapta o procedimento da folha de pagamento aos pacotes disponíveis. Agora, os computadores são tão comuns, se não tão amados, que as adaptações são aceitas como uma coisa natural.

Há exceções dramáticas ao meu argumento de que a generalização de pacotes de software mudou pouco ao longo dos anos: planilhas eletrônicas e sistemas de banco de dados simples. Essas poderosas ferramentas, tão óbvias em retrospecto e, no entanto, tão tardias em aparecer, se prestam a uma miríade de usos, alguns pouco ortodoxos. Artigos e até livros agora são abundantes sobre como lidar com tarefas inesperadas com a planilha. Um grande número de aplicativos que anteriormente seriam gravados como programas personalizados no Cobol ou no Report Program Generator agora são rotineiramente feitos com essas ferramentas.

Muitos usuários agora operam seus próprios computadores todos os dias em vários aplicativos sem precisar escrever um programa. De fato, muitos desses usuários não podem escrever novos programas para suas máquinas, mas são adeptos da resolução de novos problemas.

Acredito que a estratégia de produtividade de software mais poderosa para muitas organizações hoje é equipar os trabalhadores intelectuais ingênuos que estão na linha de fogo com computadores pessoais e bons programas generalizados de redação, desenho, arquivos e planilhas e depois soltá-los. . A mesma estratégia, realizada com pacotes matemáticos e estatísticos generalizados e algumas capacidades simples de programação, também funcionará para centenas de cientistas de laboratório.

### Requinte de requisitos e prototipagem rápida. 
A parte mais difícil da construção de um sistema de software é decidir precisamente o que construir. Nenhuma outra parte do trabalho conceitual é tão difícil quanto estabelecer os requisitos técnicos detalhados, incluindo todas as interfaces para pessoas, máquinas e outros sistemas de software. Nenhuma outra parte do trabalho enfraquece o sistema resultante, se for feito errado. Nenhuma outra parte é mais difícil de corrigir depois.

Portanto, a função mais importante que o desenvolvedor de software executa para o cliente é a extração e refinamento iterativo dos requisitos do produto. Pois a verdade é que o cliente não sabe o que ele quer. O cliente geralmente não sabe quais perguntas devem ser respondidas e quase nunca pensou no problema no detalhe necessário para a especificação. Até mesmo a resposta simples - "Faça o novo sistema de software funcionar como nosso antigo sistema manual de processamento de informações" - de fato é simples demais. Nunca se quer exatamente isso. Sistemas complexos de software são, além disso, coisas que agem, que se movem, que funcionam. A dinâmica dessa ação é difícil de imaginar. Portanto, ao planejar qualquer atividade de design de software, é necessário permitir uma iteração extensa entre o cliente e o designer como parte da definição do sistema.

Eu daria um passo adiante e afirmaria que é realmente impossível para um cliente, mesmo trabalhando com um engenheiro de software, especificar completamente, precisamente e corretamente os requisitos exatos de um produto de software moderno antes de tentar algumas versões do produto.

Portanto, um dos mais promissores esforços tecnológicos atuais, e que ataca a essência, e não os acidentes, do problema de software, é o desenvolvimento de abordagens e ferramentas para prototipagem rápida de sistemas, uma vez que a prototipagem é parte da especificação iterativa dos sistemas. requisitos.

Um *protótipo de sistema de software* é aquele que simula as interfaces importantes e executa as principais funções do sistema pretendido, embora não esteja necessariamente limitado pelas mesmas restrições de velocidade, tamanho ou custo do hardware. Os protótipos normalmente executam as tarefas principais do aplicativo, mas não tentam manipular as tarefas excepcionais, respondem corretamente a entradas inválidas ou abortam de forma limpa. O objetivo do protótipo é tornar real a estrutura conceitual especificada, para que o cliente possa testá-la quanto à consistência e usabilidade.

Grande parte do procedimento de aquisição de software atual baseia-se na suposição de que é possível especificar um sistema satisfatório com antecedência, obter propostas para sua construção, construí-lo e instalá-lo. Acho que essa suposição é fundamentalmente errada e que muitos problemas de aquisição de software surgem dessa falácia. Portanto, eles não podem ser corrigidos sem uma revisão fundamental - revisão que forneça desenvolvimento iterativo e especificação de protótipos e produtos.

Desenvolvimento incremental - cresça, não construa software. Ainda me lembro do choque que senti em 1958 quando ouvi pela primeira vez um amigo falar sobre a *construção de* um programa, em vez de *escrever* um. Num piscar de olhos, ele ampliou minha visão geral do processo de software. A mudança da metáfora foi poderosa e precisa. Hoje entendemos como, como outros processos de construção, a construção de software é, e usamos livremente outros elementos da metáfora, como *especificações, montagem de componentes* e *andaimes*.

A metáfora do edifício sobreviveu à sua utilidade. É hora de mudar novamente. Se, como acredito, as estruturas conceituais que construímos hoje são muito complicadas para serem especificadas com precisão e complexas demais para serem construídas sem falhas, então devemos adotar uma abordagem radicalmente diferente.

Vamos transformar a natureza e estudar a complexidade nas coisas vivas, em vez de apenas as obras mortas do homem. Aqui encontramos construções cujas complexidades nos emocionam com admiração. O cérebro, por si só, é intricado além do mapeamento, poderoso além da imitação, rico em diversidade, autoprotegido e autorregenerador. O segredo é que é cultivado, não construído.

Então deve ser com nossos sistemas de software. Alguns anos atrás, a Harlan Mills propôs que qualquer sistema de software deveria ser desenvolvido por desenvolvimento incremental. [10] Ou seja, o sistema deve primeiro ser executado, mesmo que não faça nada útil, exceto chamar o conjunto apropriado de subprogramas fictícios. Então, pouco a pouco, ele deve ser desenvolvido, com os subprogramas, por sua vez, sendo desenvolvidos - em ações ou chamadas para stubs vazios no nível abaixo.

Eu tenho visto resultados mais dramáticos desde que comecei a insistir com essa técnica sobre os construtores do projeto na minha aula de Laboratório de Engenharia de Software. Nada na última década mudou tão radicalmente minha própria prática ou sua eficácia. A abordagem exige um projeto de cima para baixo, pois é um crescimento de cima para baixo do software. Permite fácil retrocesso. Presta-se aos primeiros protótipos. Cada função adicional e nova provisão para dados mais complexos ou circunstâncias crescem organicamente fora do que já está lá.

Os efeitos da moral são surpreendentes. Entusiasmo pula quando há um sistema em execução, mesmo um simples. Esforços redobram quando a primeira imagem de um novo sistema de software gráfico aparece na tela, mesmo que seja apenas um retângulo. Um sempre tem, em todas as fases do processo, um sistema de trabalho. Eu acho que as equipes podem desenvolver entidades muito mais complexas em quatro meses do que podem construir .

Os mesmos benefícios podem ser obtidos em grandes projetos, como nos meus pequenos. [11]

### Grandes designers. 
A questão central em como melhorar os centros de arte de software, como sempre, nas pessoas.

Podemos obter bons desenhos seguindo boas práticas, em vez de boas práticas. Boas práticas de design podem ser ensinadas. Os programadores estão entre as partes mais inteligentes da população, para que possam aprender boas práticas. Assim, um grande impulso nos Estados Unidos é promulgar boas práticas modernas. Novos currículos, novas literaturas, novas organizações como o Instituto de Engenharia de Software, todos surgiram para elevar o nível de nossa prática de ruim para bom. Isso é inteiramente apropriado.

No entanto, não acredito que possamos dar o próximo passo para cima da mesma maneira. Enquanto a diferença entre os projetos conceituais pobres e os bons pode estar na solidez do método de design, a diferença entre bons e grandes designs certamente não. Grandes designs vêm de grandes designers. A construção de software é um processo *criativo*. Metodologia sólida pode capacitar e liberar a mente criativa; não pode inflamar ou inspirar o drudge.

As diferenças não são menores - são como as diferenças entre Salieri e Mozart. Estudo após estudo mostra que os melhores projetistas produzem estruturas mais rápidas, menores, mais simples, mais limpas e produzidas com menos esforço. [12] As diferenças entre o grande e o médio aproximam-se de uma ordem de grandeza.

Uma pequena retrospectiva mostra que, embora muitos sistemas de software úteis tenham sido projetados por comitês e construídos como parte de projetos com várias partes, esses sistemas de software que entusiasmaram os fãs apaixonados são aqueles que são produtos de uma ou poucas mentes projetadas, grandes projetistas. Considere Unix, APL, Pascal, Modula, a interface Smalltalk, até Fortran; e contraste-os com Cobol, PL / I, Algol, MVS / 370 e MS-DOS. (Veja a Tabela 1.)

Portanto, embora eu apoie fortemente os esforços de transferência de tecnologia e desenvolvimento de currículos em andamento, acredito que o esforço individual mais importante que podemos desenvolver é desenvolver maneiras de desenvolver grandes projetistas.

Nenhuma organização de software pode ignorar esse desafio. Bons gerentes, por mais escassos que sejam, não são mais escassos do que bons designers. Grandes designers e grandes gerentes são ambos muito raros. A maioria das organizações gasta esforços consideráveis ​​para encontrar e cultivar as perspectivas de gestão; Não conheço ninguém que gaste um esforço igual para encontrar e desenvolver os grandes projetistas dos quais a excelência técnica dos produtos dependerá.

Tabela 1. Vs excitantes. 

Produtos de software úteis mas não excitantes.
---------------------------------------------
Emocionante           | Produtos
----------------------|----------------------
sim                   | Não
Unix                  | Cobol
APL                   | PL/I
Pascal                | Algol
Modula                | MVS / 370
Conversa fiada        | MS-DOS
Fortran               | nenhuma



Minha primeira proposta é que cada organização de software deve determinar e proclamar que os grandes projetistas são tão importantes para o seu sucesso quanto os grandes gerentes, e que se espera que sejam igualmente nutridos e recompensados. Não apenas o salário, mas as gratificações de reconhecimento - tamanho do escritório, mobília, equipamento técnico pessoal, fundos de viagem, suporte de pessoal - devem ser totalmente equivalentes.

Como crescer grandes designers? O espaço não permite uma longa discussão, mas alguns passos são óbvios:

* Identifique sistematicamente os principais projetistas o mais cedo possível. Os melhores nem sempre são os mais experientes.
* Atribuir um mentor de carreira para ser responsável pelo desenvolvimento do cliente em potencial e cuidadosamente manter um arquivo de carreira.
* Elaborar e manter um plano de desenvolvimento de cuidados para cada cliente em potencial, incluindo estágios cuidadosamente selecionados com os melhores designers, episódios de educação formal avançada e cursos de curta duração, todos intercalados com tarefas de design individual e liderança técnica.
* Ofereça oportunidades para que designers em crescimento interajam e estimulem uns aos outros.

## Agradecimentos

Agradeço a Gordon Bell, a Bruce Buchanan, a Rick Hayes-Roth, a Robert Patrick e, principalmente, a David Parnas por seus insights e idéias estimulantes, ea Rebekah Bierly pela produção técnica deste artigo.

REFERÊNCIAS
[1] DL Parnas, "Projetando Software para Facilidade de Extensão e Contração ", IEEE Transactions on Software Engineering , vol. 5, n ° 2, março de 1979, pp. 128-38.

[2] G. Booch, "Design Orientado a Objetos", Engenharia de Software com Ada , 1983, Menlo Park, Califórnia: Benjamin / Cummings.

[3] Transações IEEE em Engenharia de Software (edição especial sobre inteligência artificial e engenharia de software), l. Mostow, guest ed., Vol. 11, n 11, novembro de 1985.

[4] DL Parnas, "Aspectos de Software de Sistemas Estratégicos de Defesa:" American Scientist , novembro de 1985.

[5] R. Balzer, "Uma perspectiva de 15 anos em programação automática", IEEE Transactions on Software Engineering (edição especial sobre inteligência artificial e engenharia de software), J. Mostow, guest ed., Vol. 11, n. 11 (novembro de 1985), pp. 1257-67.

[6] Computer (edição especial em programação visual), RB Graphton e T. Ichikawa, guest eds., Vol. 18, n ° 8, agosto de 1985.

[7] G. Raeder, "Uma pesquisa de técnicas de programação gráficas atuais", Computer (edição especial em programação visual), RB Graphton e T. Ichikawa, eds. De convidado, vol. 18, n ° 8, agosto de 1985, pp. 11-25.

[8] FP Brooks, Mês do Homem Mítico , Leitura, Missa: Addison-Wesley, 1975, Capítulo 14.

[9] Conselho de Ciência da Defesa, Relatório da Força Tarefa sobre Software Militar na imprensa.

[10] HD Mills, "Programação Top-Down em Grandes Sistemas", em Técnicas de Depuração em Grandes Sistemas , R. Ruskin, org., Englewood Cliffs, NJ: Prentice-Hall, 1971.

[11] BW Boehm, "Um modelo espiral de desenvolvimento e aprimoramento de software", 1985, Relatório Técnico TRW 21-371-85, TRW, Inc., 1 Space Park, Redondo Beach, Califórnia 90278.

[12] H. Sackman, WJ Erikson, e EE Grant, "Estudos Experimentais Exploratórios Comparando o Desempenho de Programação Online e Offline", Comunicações do ACM , vol. 11, n ° 1 (janeiro de 1968), pp. 3-11.

Brooks, Frederick P., "Nenhuma bala de prata: Essência e acidentes de engenharia de software" , Computer , vol. 20, n ° 4 (abril 1987) p. 10-19.
