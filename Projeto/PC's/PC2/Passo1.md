# Passo 1 - Criação de Pastas no Computador
- Para acessar comandos básicos do terminal do Computador, entre neste [diretório](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/Projeto/ComandosB%C3%A1sicos.md)


### > Abrir terminal do Computador


### > Entrar com o usuário ``redes``
```bash
su redes
```
#### - Digite a senha do Usuário

> Ao digitar a senha, ela não estará visivel para o usuário, contudo estará sendo escrita!


### > Instalar Net-tools
Essa instalação proporcionará o acesso a um pacote com várias ferramentas úteis para uso na sua rede local.
```bash
sudo apt install net-tools
```


### > Criar pasta ``labredes`` na raiz ``/``
```bash
 sudo mkdir /labredes
```


### > Para verificar a criação da pasta:
```bash
 ls -la / #verifica a existencia do diretório /labredes
 cd /labredes #Coloca a pasta /labredes como diretório corrente
```


### > Agora vamos criar subpastas:

Para a criação de subpastas, o diretório que você deseja inserir essas subpastas deve está como diretório corrente/atual. Utilizando o comando ``cd/<nome do diretório completo que você deseja inserir um subdiretório>``. Se você deseja adicionar uma outra subpasta em um subdiretório, você deverá colocar no cd/ todos os diretórios antecedentes.

#### - Criar os diretórios para a criação de usuário
 ```bash
 cd /labredes 
 sudo mkdir images
 cd ./images #Colocando o ./ você irá acessar o diretório anterior e o subdiretório que você quer acessar atualmente. Seria o mesmo que: cd /labredes/images
 sudo mkdir original 
 cd ./original
 ls -la #Para verificar a organização dos subdiretórios.
 ```
#### - Criar os diretórios para a criação da Máquina Virtual
```bash
 cd /labredes
 sudo mkdir VM
 cd ./VM
 sudo mkdir 924
 cd ./924
 sudo mkdir <student> # substitua <student> pelo seu nome
 cd ./<student>
```


### > Adicionar o usuário ``aluno`` ao grupo ``redes``
Para ter uma maior liberdade na manipulação das pastas/subpastas, iremos dar mais permissões ao usuário com essa etapa. 

* Modificando as permissões de arquivos e pastas
   * ``chown`` modifica o dono da pasta labredes para o usuario nobody e grupo nogroup
   * ``chgrp`` altera o proprietário de grupo do diretório ``/labredes`` para o grupo ``redes``
   * ``chmod`` altera as permissões do diretório para escrita pelos membros do grupo (Para mais informações como utilizar o chmod, entre neste site: https://www.pluralsight.com/blog/it-ops/linux-file-permissions; Para saber qual número utilizar, abra este site: https://chmodcommand.com/chmod-777/)
```bash
 sudo chown -R nobody:nogroup /labredes
 ls -la
 sudo chgrp -R redes /labredes
 sudo chmod -R 771 /labredes #define permissões para que (U)ser/proprietário possa ler, escrever e executar. (G)roup pode ler, escrever e executar. (O)outros não podem ler, não podem escrever e podem executar
 ls -la
 getent group  #lista os grupos criados: observe no fim da lista que os usuários também possuem grupos.                                                          
```


### > Instalação da imagem do Linux(Ubuntu) para utilizarmos nas Máquina Virtuais

Se você está fazendo esse projeto com o Professor Alaelson do IFAL - Campus Arapiraca, ele irá disponibilizar comandos de instalação da seguinte imagem:
```
ubuntu-server-mini.ova
```

#### - Instalação pelo Terminal 

```shell
cd /labredes/images/original
ls -la #verifique no resultado a existência dos arquivos .iso
# Se não houver os arquivos iso na pasta /labredes/images/original deve-se copiá-los com os comandos:
scp aluno@192.168.101.10:~/Public/iso-images/ubuntu-server-mini.ova /labredes/images/original
```


### > Conclusão
Após o término desse Passo 1, direcione para o [Próximo Passo](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/Projeto/PC's/PC2/Passo2.md)
