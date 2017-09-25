+++
title = "Sobre o Processo de Revisão de Pacotes no Fedora Project"
date = "2017-09-25T13:38:47-03:00"
tags = ["pt_BR"]
Categories = ["Fedora"]
draft = false
+++

No [Projeto Fedora](https://fedoraproject.org), quando um um empacotador decide
incluir um novo pacote na distribuição, este pacote deve passar por um processo
de revisão, que serve para verificar se o novo pacote respeita as diretrizes
listadas no [Fedora Packaging
Guidelines](https://fedoraproject.org/wiki/Packaging:Guidelines). O revisor
deve verificar, dentre outros atributos,

* a licença do software a ser incluído na distribuição, uma vez que o Fedora não distribui software proprietário ou patenteado;
* se o pacote não distribui nenhuma biblioteca embutida, uma vez que isto pode ocasionar problemas de segurança;
* se o pacote distribui os arquivos corretos, nos lugares corretos, conforme o [File System Hieratchy Standard](https://wiki.linuxfoundation.org/lsb/fhs);
* se o pacote não gera conflitos com outros pacotes;
* se o pacote pode ser de fato construído a partir do seu código fonte e instalado, conforme as dependências listadas pelo empacotador.

Alguns meses atrás eu preparei um vídeo mostrando este processo de revisão.
Este vídeo não mostra todo o processo de revisão de pacotes, nem tem a intenção
de ser um tutorial para revisores ou empacotadores, mas pode ser visto como um
vídeo educativo para novos revisores ou empacotadores querendo incluir pacotes
no Fedora ou em repositórios EPEL.

{{< youtube zomd-y7tkV4 >}}
