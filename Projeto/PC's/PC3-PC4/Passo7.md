# Passo 7 - Configuração Estática de Nomes

### > Objetivo:
 - Configurar um serviço de nomes
 - Configurar /etc/hosts

### > Login da VM ubuntu server

* Usuário da VM: ``administrador``
* Senha da VM: ``adminifal``

#

### > Serviço de nomes estático do Ubuntu:
>**_NOTA:_**
> Nomes de host estáticos são mapeamentos de nome de host para IP definidos localmente localizados no arquivo /etc/hosts. 
> Os nomes configurados no /etc/hosts têm precedência sobre o DNS por padrão. Assim, tentar resolver um nome de host e ele corresponder a uma entrada em /etc/hosts, ele não tentará procurar o registro no DNS. 
>O seguinte é um exemplo de um arquivo de hosts em que vários servidores locais foram identificados por nomes de host simples, aliases e seus nomes de >**_** domínio totalmente qualificados (FQDNs) equivalentes.

```
127.0.0.1 localhost
127.0.1.1 servidor ubuntu
10.0.0.11 server1 server1.example.com vpn
10.0.0.12 server2 server2.example.com mail
10.0.0.13 server3 server3.example.com www
10.0.0.14 server4 server4.example.com file
```

>**Observação**: No exemplo acima, observe que cada um dos servidores recebeu aliases além de seus nomes próprios e FQDNs. 
>* ``Server1`` foi mapeado para o nome ``vpn``
>* ``server2`` é referido como ``mail`` 
>* ``server3`` como ``www`` e 
>* ``server4`` como ``file``

#

### > Configurar o serviço de nomes estático. 

```
Tabela 1: Definições de endereços IPs da Rede e Nomes de Hosts
-----------------------------------------------------------------------------------------------------
|  DESCRIÇÃO  |       IP        |   hostname        |               FQDN               |   aliase   |
-----------------------------------------------------------------------------------------------------
| rede        | 192.168.24.80   |                   |                                  |            |
| máscara     | 255.255.255.240 |                   |                                  |            |
| Gateway     | 192.168.24.81   |                   |                                  |            |
| VM1-PC1     | 192.168.24.81   |   srv-vm1-pc1     | matheus1.grupo6-924.ifalara.net  |   matheus  |
| VM2-PC1     | 192.168.24.82   |   srv-vm2-pc1     | matheus2.grupo6-924.ifalara.net  |   ataide   |
| VM1-PC2     | 192.168.24.83   |   srv-vm1-pc2     | josival1.grupo6-924.ifalara.net  |   josival  |
| VM2-PC2     | 192.168.24.84   |   srv-vm2-pc2     | josival2.grupo6-924.ifalara.net  |   costa    |
| VM1-PC3     | 192.168.24.85   |   srv-vm1-pc3     | clara1.grupo6-924.ifalara.net    |   clara    |
| VM2-PC3     | 192.168.24.86   |   srv-vm2-pc3     | clara2.grupo6-924.ifalara.net    |   leao     |
| VM1-PC4     | 192.168.24.87   |   srv-vm1-pc4     | cara1.grupo6-924.ifalara.net     |   cara1    |
| VM2-PC4     | 192.168.24.88   |   srv-vm2-pc4     | cara2.grupo6-924.ifalara.net     |   cara2    |
-----------------------------------------------------------------------------------------------------
```

* Edite os arquivo /etc/hosts conforme as definições da Tabela de Endereços e Nomes (Tabela 1)

```shell
sudo nano /etc/hosts
```


> Obs.: Colocaremos as configurações que fizemos para nosso grupo, mas você pode colocar da maneira que você desejar configurar

* Arquivo /etc/hosts na VM1-PC1:

```
127.0.0.1 localhost
127.0.1.1 srv-vm1-pc3  
192.168.24.81     srv-vm1-pc1     matheus1.grupo6-924.ifalara.net     matheus
192.168.24.82     srv-vm2-pc1     matheus2.grupo6-924.ifalara.net     ataide
192.168.24.83     srv-vm1-pc2     josival1.grupo6-924.ifalara.net     josival
192.168.24.84     srv-vm2-pc2     josival2.grupo6-924.ifalara.net     costa
192.168.24.85     srv-vm1-pc3     clara1.grupo6-924.ifalara.net       clara
192.168.24.86     srv-vm2-pc3     clara2.grupo6-924.ifalara.net       leao
192.168.24.87     srv-vm1-pc4     cara1.grupo6-924.ifalara.net        cara1
192.168.24.88     srv-vm2-pc4     cara2.grupo6-924.ifalara.net        cara2

# The following lines are desirable for IPv6 capable hosts
::1     localhost ip6-localhost ip6-loopback
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
```
 > Para as outras VM's do PC3 e PC4, deve ser alterado a segunda linha do comando (``"127.0.1.1 srv-vm1-pc3"``), alterando somente o hostname

### > Acessando uma VM remotamente:

* Exemplo: $ ssh ``<user>``@``<ipServidorRemoto>``
* Fazendo o login 
   * de: terminal-pc
   * para: 192.168.24.88

```shell
ssh administrador@192.168.24.88
```

- Acesse o diretório com os [Testes dos SSH's das VM's do PC 3 e PC 4](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/TestesDaRede/Testes:PC3-PC4/SSH.md) para ver exemplos

### > Conclusão
Após o término desse Passo 7, você pode retornar para a [tela de escolha do PC](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/Projeto/README.md) se desejar configurar algum PC. Caso não, seu projeto está finalizado!
