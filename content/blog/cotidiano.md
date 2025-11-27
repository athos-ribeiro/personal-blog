+++
Categories = ["Desenvolvimento", "Hackathon", "Política"]
Description = ""
Tags = ["Desenvolvimento", "Política", "Tenho Dito"]
date = "2016-07-18T11:16:09-03:00"
menu = "main"
title = "Hackathon Cotidiano"

+++

![Dia de apresentação](https://ar.dev.br/images/apresentacao_cotidiano.jpg)

Entre os dias 9 e 15 de Julho a [Cotidiano](http://www.cotidiano.com.br/) realizou sua primeira *Hackathon* em Brasília. Como eu estava de férias por lá, resolvi participar.

O primeiro dia foi um dia de apresentações, levantamento de idéias para aplicativos cívicos e formação de equipes. Pata tal foi utilizado o novo espaço de *co-working* da Secretaria do Trabalho do Distrito Federal, que ficou aberto para os participantes ao longo da semana. O [Eduardo Castro](https://github.com/educastro) da Secretaria acompanhou o pessoal trabalhando por lá e resolveu alguns problemas com a rede do espaço que apareceram eventualmente (eu não conheço um ministério ou secretaria em Brasília que não tenha várias restrições na rede).

### Formato

* 12 participantes
* 4 Equipes de 3 membros cada
* 1 Semana para desenvolver um produto com aplicações para a população (*civic hacking*)
* As equipes poderiam trabalhar de forma remota ou no espaço cedido pela Secretaria
* A equipe com a melhor solução, atendendo aos critérios: **impacto social**, **abrangência**, **capacidade de implantação** e **implementação** seria declarada vencedora da *hackathon*
* A equipe vencedora ganharia 3 celulares Lenovo (um para cada membro)
* Todos os produtos desenvolvidos deveriam estar no Github sob uma licença de Software Livre

### Nossa equipe

Nossa equipe foi formada pelo [Fabrício Raphael](https://github.com/fabricioraphael), estudante de engenharia de software que conhecemos no primeiro dia, pelo [Matheus Fernandes](https://github.com/msfernandes), colega de [LAPPIS](http://lappis.unb.br), Universidade de Brasília e agora funcionário do LabHacker da Câmara dos Deputados e por mim.

![Dia de apresentação](https://ar.dev.br/images/hack_cotidiano_eq.jpg) 
Matheus, eu e Fabrício

Ao longo da semana desenvolvemos um software que
* coletava palavras-chave dos discursos e das propostas dos deputados federais
* utilizava o método de similaridade de cossenos para calcular a semelhança entre discursos e propostas de cada deputado
* normalizava os dados encontrados para cada deputado, chamando-os de nível de coerência do deputado
* apresentava um ranking dos deputados com maiores e menores índices de coerência
* apresentava duas nuvens de palavras para cada deputado, com as palavras mais frequentes em seus discursos e propostas

No último dia ainda não tinhamos nem um nome e nem uma logo, então o Dudu da Cotidiano apareceu e resolveu nosso problema:

![Tenho Dito](https://ar.dev.br/images/tenho_dito.png)
Obrigado, Dudu!

### Último dia e resultado da *hackathon*

O último dia foi super divertido: todas as equipes trabalharam juntas em uma sala bem legal, cheia de comida (nhom! nhom!) e café!

No fim, embora eu tenha gostado bastante da nossa solução, o pessoal do [Chegou-Sus](https://github.com/matrpedreira/Chegou-Sus-) levou os celulares para casa!

Depois foi todo mundo pra casa descansar mesmo porque a semana foi puxada!

[O Tenho Dito está no Github](https://github.com/tenhodito) sob a licença GPLv3. Nós pretendemos rodar as análises de similaridade de cossenos com mais dados e subir uma versão 0.1 na infraestrutura do LabHacker em breve!
