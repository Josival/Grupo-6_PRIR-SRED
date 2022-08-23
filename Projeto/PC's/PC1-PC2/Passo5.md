# Passo 5 | Usando o SSH nas máquinas virtuais

####  Alterar a rede para o modo NAT, como na foto:

####  Comentar as linhas de endereçamento ip estático e ativar o dhcp, como na foto:


###  Para atribuir o nome do usuário na vm1 se faz uso do comando:
    sudo hostnamectl set-hostname srv-vm1-pc1

###  Para atualizar a   VM, foram usados so comandos a seguir:
    sudo apt update       
#### Como pode ser visto abaixo na foto:

    sudo apt upgrade -y 
#### Como pode ser visto abaixo na foto: 

###  Para a instalação do ssh, que servirá para fazer a conexão via internet, foi usado o |comando:
    sudo apt-get install openssh-server

#### Para verificar o status das portas do sistema, foi usado:
    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
#### Como pode ser visto na foto:

###  Para a configuração do firewall, necessário para garantir que as portas etão funcionando |corretamente, é usado os seguintes comandos:
    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
#####    sudo ufw status
#### para ativar o firewall:
    sudo ufw enable
#### Como pode ser visto na foto:

###    Alterar a rede para o  modo bridge, e descomentar os endereços ips estáticos, e desativar o dhcp. Como pode ser notado abaixo na foto:

###    Para verificar se está ocorrendo a comunicação entre as máquinas, faz uso do ping, como:
####   Da VM1-PC3 para a VM2-PC4:
    ping 192.168.24.88

####    Da VM2-PC3 para a VM1-PC4:
    ping 192.168.24.87

###    E a comunicação via ssh é feita da seguinte forma:
#### Da VM1-PC2 para a VM2-PC1:
    ssh srv-vm2-pc4@192.168.24.88

#### Da VM2-PC2 para a VM1-PC1:
    ssh srv-vm1-pc4@192.168.24.87

######    Usar o comando exit para sair das vms conectadas anteriormente!
