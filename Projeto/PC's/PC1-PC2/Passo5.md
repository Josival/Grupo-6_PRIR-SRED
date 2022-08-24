# Passo 5 - Usando o SSH nas máquinas virtuais

### Na VM1-PC1 

#####  Alterar a rede para o modo NAT, como na foto:

#####  Comentar as linhas de endereçamento ip estático e ativar o dhcp, como na foto:

####  Para atribuir o nome do usuário na vm1 se faz uso do comando:
    sudo hostnamectl set-hostname srv-vm1-pc1

####  Para atualizar a VM, foram usados os comandos a seguir:
    sudo apt update       
##### Como pode ser visto abaixo na foto:

    sudo apt upgrade -y 
##### Como pode ser visto abaixo na foto: 

####  Para a instalação do ssh, que servirá para fazer a conexão via internet, foi usado o comando:
    sudo apt-get install openssh-server

#### Para verificar o status das portas do sistema, foi usado:
    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
##### Como pode ser visto na foto:

####  Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, é usado os seguintes comandos:
    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
#### Para ativar o firewall:
    sudo ufw enable
##### Como pode ser visto na foto:

####    Alterar a rede para o  modo bridge, descomentar os endereços ips estáticos, e desativar o dhcp.

##### Como pode ser notado abaixo na foto:

-------------------------------------------------------------------------------------------------------------

### Na VM2-PC1

#####  Alterar a rede para o modo NAT, como na foto:

#####  Comentar as linhas de endereçamento ip estático e ativar o dhcp, como na foto:

####  Para atribuir o nome do usuário na vm1 se faz uso do comando:
    sudo hostnamectl set-hostname srv-vm2-pc1

####  Para atualizar a VM, foram usados os comandos a seguir:
    sudo apt update       
##### Como pode ser visto abaixo na foto:

    sudo apt upgrade -y 
##### Como pode ser visto abaixo na foto: 

####  Para a instalação do ssh, que servirá para fazer a conexão via internet, foi usado o comando:
    sudo apt-get install openssh-server

#### Para verificar o status das portas do sistema, foi usado:
    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
##### Como pode ser visto na foto:

####  Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, é usado os seguintes comandos:
    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
#### Para ativar o firewall:
    sudo ufw enable
##### Como pode ser visto na foto:

####    Alterar a rede para o  modo bridge, descomentar os endereços ips estáticos, e desativar o dhcp.

##### Como pode ser notado abaixo na foto:

--------------------------------------------------------------------------

### Na VM1-PC2

#####  Alterar a rede para o modo NAT, como na foto:

#####  Comentar as linhas de endereçamento ip estático e ativar o dhcp, como na foto:

####  Para atribuir o nome do usuário na vm1 se faz uso do comando:
    sudo hostnamectl set-hostname srv-vm1-pc2

####  Para atualizar a VM, foram usados os comandos a seguir:
    sudo apt update       
##### Como pode ser visto abaixo na foto:

    sudo apt upgrade -y 
##### Como pode ser visto abaixo na foto: 

####  Para a instalação do ssh, que servirá para fazer a conexão via internet, foi usado o comando:
    sudo apt-get install openssh-server

#### Para verificar o status das portas do sistema, foi usado:
    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
##### Como pode ser visto na foto:

####  Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, é usado os seguintes comandos:
    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
#### Para ativar o firewall:
    sudo ufw enable
##### Como pode ser visto na foto:

####    Alterar a rede para o  modo bridge, descomentar os endereços ips estáticos, e desativar o dhcp.

##### Como pode ser notado abaixo na foto:

-----------------------------------------------------------------------------

### Na VM2-PC2

#####  Alterar a rede para o modo NAT, como na foto:

#####  Comentar as linhas de endereçamento ip estático e ativar o dhcp, como na foto:

####  Para atribuir o nome do usuário na vm1 se faz uso do comando:
    sudo hostnamectl set-hostname srv-vm2-pc2

####  Para atualizar a VM, foram usados os comandos a seguir:
    sudo apt update       
##### Como pode ser visto abaixo na foto:

    sudo apt upgrade -y 
##### Como pode ser visto abaixo na foto: 

####  Para a instalação do ssh, que servirá para fazer a conexão via internet, foi usado o comando:
    sudo apt-get install openssh-server

#### Para verificar o status das portas do sistema, foi usado:
    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
##### Como pode ser visto na foto:

####  Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, é usado os seguintes comandos:
    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
#### Para ativar o firewall:
    sudo ufw enable
##### Como pode ser visto na foto:

####    Alterar a rede para o  modo bridge, descomentar os endereços ips estáticos, e desativar o dhcp.

##### Como pode ser notado abaixo na foto:

-----------------------------------------------------------------------------------------------------

####  Fazendo uso do ping entre as máquinas, para verificar se está ocorrendo a comunicação e se foi configurado corretamente:

#####    Da VM1-PC2 para a VM1-PC1:
    ping 192.168.24.81
#####    Da VM1-PC1 para a VM1-PC2:
    ping 192.168.24.83
    
###    E a comunicação via ssh é feita da seguinte forma:
##### Da VM1-PC2 para a VM1-PC1:
    ssh srv-vm1-pc2@192.168.24.81
##### Da VM1-PC1 para a VM1-PC2:
    ssh srv-vm1-pc2@192.168.24.83
    
-----------------------------------------------------------------------------------------------------

####  Fazendo uso do ping entre as máquinas, para verificar se está ocorrendo a comunicação e se foi configurado corretamente:

#####    Da VM2-PC2 para a VM2-PC1:
    ping 192.168.24.82
#####    Da VM2-PC1 para a VM2-PC2:
    ping 192.168.24.84
    
###    E a comunicação via ssh é feita da seguinte forma:
##### Da VM2-PC2 para a VM2-PC1:
    ssh srv-vm2-pc1@192.168.24.82
##### Da VM2-PC1 para a VM2-PC2:
    ssh srv-vm2-pc2@192.168.24.84
    
######    Usar o comando 'exit' para sair das VMs conectadas anteriormente!

-----------------------------------------------------------------------------------------------------

### > Conclusão
Após o término desse Passo 5, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1-PC2/Passo6.md)
