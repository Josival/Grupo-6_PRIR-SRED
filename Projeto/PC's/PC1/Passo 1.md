# Passo 1 - Criação de Pastas no Computador
- Para acessar comandos básicos do terminal do Computador, entre neste [diretório](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/Comandos%20B%C3%A1sicos.md)
- Antes de começar, utilize o comando ``sudo apt install net-tools`` para ter acesso a um pacote com várias ferramentas úteis para uso na sua rede local

### - Abrir terminal do Computador


### - Entrar com o usuário ``redes``
```bash
su redes
```
#### Senha para entrar no usuário ``redes``
```bash
adminifal
```


### - Criar pasta ``labredes`` na raiz ``/``
```bash
 cd ~ #Vai deixar a raiz inicial do computador como diretório corrente
 sudo mkdir /labredes
```


### - Para verificar se foi criada esta pasta
```bash
 ls -la / #verifica a existencia do diretório /labredes
 cd /labredes #Coloca a pasta /labredes como diretório corrente
```


### - Agora vamos criar subpastas

Para a criação de subpastas, o diretório que você deseja colocar essas subpastas deve está como diretório corrente/atual. Utilizando o comando ``cd/<nome do diretório completo que você deseja colocar um subdiretório>``. Se você deseja adicionar em um subdiretório, você deverá colocar no cd/ todos os diretórios antecedentes.

#### Criar os diretórios para a criação de usuário
 ```bash
 cd /labredes 
 sudo mkdir images
 cd ./images #Colocando o ./ você irá acessar o diretório anterior e o subdiretório que você quer acessar atualmente. Seria o mesmo que: cd /labredes/images
 sudo mkdir original 
 cd ./original
 ls -la #Para ver como está ficando com os subdiretórios
 ```
#### Criar os diretórios para a criação da Máquina Virtual
```bash
 cd ~
 sudo mkdir labredes/VM
 sudo mkdir labredes/VM/924
 sudo mkdir labredes/VM/924/<student> # substitua <student> pelo seu nome
```


### - Adicionar o usuário ``aluno`` ao grupo ``redes``
Para ter uma maior liberdade na manipulação das pastas/subpastas, iremos dar mais permissões a elas com essa etapa. Comece utilizando esse comando: 
```bash
 sudo usermod -aG redes aluno
```
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
 getent group  #lista grupos: observe no fim da lista que os usuários também possuem grupos
```


### - Instalação da imagem do Linux(Ubuntu) para utilizarmos nas Máquina Virtuais

Se você estará fazendo esse projeto com o Professor Alaelson do IFAL - Campus Arapiraca, ele irá disponibilizar comandos de instalação das imagens. Temos 3 imagens:
```
mini.iso
ubuntu-20.04.4-desktop-amd64.iso
ubuntu-22.04-live-server-amd64.iso
```
Sugerimos que utilize a mais básica: ``mini.iso``. Mas claro que iremos mostrar a instalação das 3 imagens. Também colocaremos 3 formas de fazer a instalação, pelo: Nautilus, Terminal e Windows Explorer (Sugerimos e fizemos pelo terminal)

#### Pelo Nautilus, acessar:

	smb://192.168.101.10/iso-images
	- user: aluno, senha: aluno
  - Copie os arquivos da pasta public para a pasta  ``/labredes/images/original``

#### Pelo Terminal 

```shell
cd /labredes/images/original
ls -la #verifique no resultado a existência dos arquivos .iso
# Se não houver os arquivos iso na pasta /labredes/images/original deve-se copiá-los com os comandos:
scp aluno@192.168.101.10:~/Public/iso-images/mini.iso /labredes/images/original
scp aluno@192.168.101.10:~/Public/iso-images/ubuntu-20.04.4-desktop-amd64.iso /labredes/images/original
scp aluno@192.168.101.10:~/Public/iso-images/ubuntu-22.04-live-server-amd64.iso /labredes/images/original
```

#### No Windows Explorer
```
Abra o Windows Explorer digite o comando na barra de endereços: \\192.168.101.10\iso-images
```


### - Conclusão
Após o término desse Passo 1, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1/Passo%202.md)
