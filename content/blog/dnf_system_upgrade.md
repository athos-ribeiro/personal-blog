+++
Categories = ["Fedora"]
Description = ""
Tags = ["Fedora", "dnf", "upgrade"]
date = "2016-06-22T12:17:30-03:00"
menu = "main"
title = "Atualizando Fedora sem dor"

+++

##### Problemas com novas versões

Sou usuário do fedora desde o *Spherical Cow* (Fedora 18), e desde então sempre que uma versão nova saía vinha aquele receio de atualizar o sistema para a nova versão: conflitos para gerencias, problemas com drivers ou qualquer coisa do tipo. Obviamente isto nunca me impediu de utilizar o Fedora, e o que eu costumava fazer para atualizar o sistema operacional a cada 6 meses, período em que o projeto Fedora lança novas versões, era:

* Extrair uma lista com todos os pacotes instalados
* Salvar arquivos de configuração  importantes
* Formatar a partição de `/`
* Instalar a nova versão do Fedora em `/`

Note que `/home` sempre está em ourta partição.

Sabendo que a cada 6 meses eu teria que seguir o procedimento acima e que após 12 meses de seu lançamento, uma versão do Fedora deixa de ser mantida, ou seja, para de receber atualizações, eu nunca gostei de utilizar Fedora ao trabalhar com servidores, optando por distribuições que mantém versões por períodos mais longos.

##### dnf e o system-upgrade plugin

Nas últimas duas releases, desde a adoção do [dnf](https://fedoraproject.org/wiki/Dnf) como gerenciador de pacotes para substituir o `yum`, o processo de atualização da distribuição foi melhorado e ficou muito mais confiável. O `dnf` possui um plugin, `system-upgrade`, que torna a vida dos usuários muito mais confortável.

##### Atualizando Fedora

Para atualizar a distro, basta seguir os passos apresentados [aqui](https://fedoramagazine.org/upgrading-fedora-23-workstation-to-fedora-24/), que resumimos a seguir:

1. Atualize todos os pacotes
2. Instale o *plugin* `system-upgrade` para o `dnf`
3. Utilize o plugin instalado para baixar os pacotes necessários para a atualização: o parâmetro `--releasever` deve receber a versão do Fedora para a qual se deseja atualizar
4. Reinicie o sistema para dar início ao processo de atualização

Os passos acima são realizados com os seguintes comandos:

```
$ sudo dnf upgrade --refresh
$ sudo dnf install dnf-plugin-system-upgrade
$ sudo dnf system-upgrade download --releasever=24
$ sudo dnf system-upgrade reboot
```

##### Servidores Fedora?

O Projeto Fedora disponibiliza imagens com conjuntos de pacotes ideais para diferentes contextos. Dado que o processo de atualização tem ficado mais simples, passamos a ter mais confiança em rodar Fedora em nossos servidores, sem medo dos períodos de atualização. Você pode baixar imagens para seu servidor [aqui](https://getfedora.org/en/server/)

**Antes de escrever este post, eu segui os passos acima para atualizar este servidor para Fedora 24 :)**
