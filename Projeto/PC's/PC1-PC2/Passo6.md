# Passo 6 - Acesso a VM com o Host-Only

### Para ativar ou conectar uma interface no computador para a comunicação do host(PC) e as VMs, seleciona-se 'arquivo' e depois em 'Host Network Manager'.

###  Clique em 'servidor DHCP' e 'habilite o servidor'.
##### como na foto:

### Para adicionar um novo adaptador de rede (Host-Only), com o objetivo de possibilitar acesso a uma VM pelo Terminal do PC.
##### como mostrado na foto:

## Na VM

####  Fazer login no usuário:
    administrador
####  senha: 
    adminifal

#### Para verificar as interfaces de rede, usa-se:
    ifconfig -a

#### Para ativar o DHCP nessa nova interface, utilizamos o seguinte comando:
    sudo nano /etc/netplan/01-netcfg.yaml
    sudo netplan apply

##### O resultado pode ser visto na seguinte foto: 

#### Podemos verificar essa nova interface criada, enp0s8, usando:
    ifconfig -a 
##### Veja na foto abaixo:

### A conexão é estabelecida com a VM através do terminal do PC pelo seguinte comando:
    ssh srv-vm1-pc1@192.168.56.100


### Conclusão
Após o término desse Passo 6, direcione para o [Próximo Passo](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/Projeto/PC's/PC1-PC2/Passo7.md)
