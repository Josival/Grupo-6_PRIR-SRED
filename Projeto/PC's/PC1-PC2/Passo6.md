# Passo 6 - Acesso à VM pelo Host-Only

###  Fazer login no usuário:
    administrador
###  senha: 
    adminifal

### Ativar ou conectar uma interface no computador para a comunicação do host(pc) e as VMs, clicando em 'arquivo' e depois em 'Host Network Manager'.
##### como mostrado nas fotos:

####  Duas fotos!

###  Clicar em servidor dhcp e habilitar o servidor.
##### como na foto:

### Adicionar um novo adaptador de rede(Host Only).
##### como mostrado na foto:

#### Para ativar o dhcp nessa nova interface, usamos o seguinte comando:
    sudo nano /etc/netplan/01-netcfg.yaml
    sudo netplan apply

##### O resultado pode ser visto na seguinte foto: 

#### Com o 'ifconfig -a' podemos verificar essa nova interface, na enp0s8.
##### Veja na foto abaixo:

### Fazer a conexão com as VMs usando o terminal do pc, usando o seguinte comando:
    ssh srv-vm1-pc1@192.168.56.100   
