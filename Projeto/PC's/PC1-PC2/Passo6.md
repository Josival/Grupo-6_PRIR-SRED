# Passo 6 - Acesso a VM com o Host-Only


### > Para ativar ou conectar uma interface no computador para a comunicação do host(PC) e as VMs, seleciona-se 'arquivo' e depois em 'Host Network Manager'


###  > Clique em 'servidor DHCP' e 'habilite o servidor'

> Como na figura:

<img src="/Projeto/Figuras/PC1/Passo6/servidordhcp.png" title="Acesso à VM pelo Host-Only" width="900" />

### > Para adicionar um novo adaptador de rede (Host-Only), com o objetivo de possibilitar acesso a uma VM pelo Terminal do PC

> Como mostrado na figura:

<img src="/Projeto/Figuras/PC1/Passo6/adap2.png" title="Acesso à VM pelo Host-Only" width="900" />

## Na VM

####  > Fazer login no usuário:
    administrador
    
##### - Senha: 
    adminifal


#### > Para ativar o DHCP nessa nova interface, utilizamos o seguinte comando:

    sudo nano /etc/netplan/01-netcfg.yaml
    sudo netplan apply


> O resultado pode ser visto na seguinte figura: 

##### - VM1-PC1
<img src="/Projeto/Figuras/PC1/Passo6/vm1-pc1-sudonano-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

##### - VM2-PC1
<img src="/Projeto/Figuras/PC1/Passo6/vm2-pc1-sudonano-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

##### - VM1-PC2
<img src="/Projeto/Figuras/PC2/Passo6/vm1-pc2-sudonano-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

##### - VM2-PC2
<img src="/Projeto/Figuras/PC2/Passo6/vm2-pc2-sudonano-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

#### > Podemos verificar essa nova interface criada, enp0s8, usando:

    ifconfig -a 
    
> Veja na figura abaixo:

##### - VM1-PC1
<img src="/Projeto/Figuras/PC1/Passo6/vm1-pc1-ifconfig-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

##### - VM2-PC1
<img src="/Projeto/Figuras/PC1/Passo6/vm2-pc1-ifconfig-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

##### - VM1-PC2
<img src="/Projeto/Figuras/PC2/Passo6/vm1-pc2-ifconfig-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

##### - VM2-PC2
<img src="/Projeto/Figuras/PC2/Passo6/vm2-pc2-ifconfig-hostonly.png" title="Acesso à VM pelo Host-Only" width="900" />

### > A conexão é estabelecida com a VM através do terminal do PC pelo seguinte comando:

    ssh <usuario ou hostname>@192.168.56.101
    
    Exemplos: ssh srv-vm1-pc1@192.168.56.101
              ssh josival@192.168.56.101


### > Conclusão
Após o término desse Passo 6, direcione para o [Próximo Passo](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/Projeto/PC's/PC1-PC2/Passo7.md)
