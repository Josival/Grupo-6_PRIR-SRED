# Passo 6 - Acesso à VM com o Host-Only

### Para ativar ou conectar uma interface no computador para a comunicação do host(pc) e as VMs, aperta em 'arquivo' e depois em 'Host Network Manager'.
##### como mostrado nas fotos:

####  Duas fotos!

###  Clique em 'servidor dhcp' e 'habilite o servidor'.
##### como na foto:

### Para adicionar um novo adaptador de rede(Host-Only), para dar acesso a uma VM pelo Terminal do PC.
##### como mostrado na foto:

## Na VM

###  Fazer login no usuário:
    administrador
###  senha: 
    adminifal

#### Para verificar as interfaces de rede, usa-se:
    ifconfig -a

#### Para ativar o dhcp nessa nova interface, usamos o seguinte comando:
    sudo nano /etc/netplan/01-netcfg.yaml
    sudo netplan apply

##### O resultado pode ser visto na seguinte foto: 

#### Com o 'ifconfig -a' podemos verificar essa nova interface, enp0s8.
##### Veja na foto abaixo:

### A conexão com a VM usando o terminal do pc, é feita pelo seguinte comando:
    ssh srv-vm1-pc1@192.168.56.100
    
##### Faça isso para todas as VMs!

