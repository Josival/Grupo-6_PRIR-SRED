# Passo 5 - Usando o SSH nas máquinas virtuais

### Na VM1-PC1 

#### > Alterar a rede para o modo NAT, como na figura:

<img src="/Projeto/Figuras/PC1/Passo5/vm1-pc1-redenat.png" title="VM1-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="1000" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, como na figura:
     
<img src="/Projeto/Figuras/PC1/Passo5/vm1-pc1-sudonat.png" title="VM1-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do usuário na VM1-PC1 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm1-pc1

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na foto:

#### > Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
    
#### > Para ativar o firewall:

    sudo ufw enable
    
> Como pode ser visto na figura:

#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo na figura:

-------------------------------------------------------------------------------------------------------------

### Na VM2-PC1

#### > Alterar a rede para o modo NAT, como na figura:

<img src="/Projeto/Figuras/PC1/Passo5/vm2-pc1-redenat.png" title="VM2-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="1000" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, como na figura:
     
<img src="/Projeto/Figuras/PC1/Passo5/vm2-pc1-sudonat.png" title="VM2-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do usuário na VM2-PC1 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm2-pc1

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na foto:

#### > Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
    
#### > Para ativar o firewall:

    sudo ufw enable
    
> Como pode ser visto na figura:

#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo na figura:

--------------------------------------------------------------------------

### Na VM1-PC2

#### > Alterar a rede para o modo NAT, como na figura:

<img src="/Projeto/Figuras/PC2/Passo5/vm1-pc2-redenat.png" title="VM1-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="1000" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, como na figura:
     
<img src="/Projeto/Figuras/PC2/Passo5/vm1-pc2-sudonat.png" title="VM1-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do usuário na VM1-PC2 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm1-pc2

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na foto:

#### > Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
    
#### > Para ativar o firewall:

    sudo ufw enable
    
> Como pode ser visto na figura:

#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo na figura:

-----------------------------------------------------------------------------

### Na VM2-PC2

#### > Alterar a rede para o modo NAT, como na figura:

<img src="/Projeto/Figuras/PC2/Passo5/vm2-pc2-redenat.png" title="VM2-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="1000" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, como na figura:
     
<img src="/Projeto/Figuras/PC2/Passo5/vm2-pc2-sudonat.png" title="VM2-PC1-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do usuário na VM2-PC2 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm2-pc2

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na foto:

#### > Para a configuração do firewall, necessário para garantir que as portas etão funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh.    # ativa o ssh no firewall UFW do ubuntu.
    sudo ufw status
    
#### > Para ativar o firewall:

    sudo ufw enable
    
> Como pode ser visto na figura:

#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo na figura:
    
-----------------------------------------------------------------------------------------------------

####  > Fazendo uso do ping entre as máquinas para verificar se está ocorrendo a comunicação e se tudo foi configurado corretamente:

##### - Da VM1-PC1 para a VM1-PC2

    ping 192.168.24.83
    
<img src="/Projeto/Figuras/PC1/Passo5/vm1-pc1-ping.png" title="VM2-PC1-ping-Usando o SSH nas Máquinas Virtuais" width="800" />

##### - Da VM2-PC1 para a VM2-PC2:

    ping 192.168.24.84
    
<img src="/Projeto/Figuras/PC1/Passo5/vm2-pc1-ping.png" title="VM2-PC1-ping-Usando o SSH nas Máquinas Virtuais" width="800" />

##### - Da VM1-PC2 para a VM1-PC1

    ping 192.168.24.81
    
<img src="/Projeto/Figuras/PC2/Passo5/vm1-pc2-ping.png" title="VM2-PC1-ping-Usando o SSH nas Máquinas Virtuais" width="800" />

##### - Da VM2-PC2 para a VM2-PC1:

    ping 192.168.24.82
    
<img src="/Projeto/Figuras/PC2/Passo5/vm2-pc2-ping.png" title="VM2-PC1-ping-Usando o SSH nas Máquinas Virtuais" width="800" />

> Para cancelar o ping é só clicar nas teclas: ``ctrl + C``

#

##### > Criação de novos usuários para as VMs, para a comunicação via ssh, pode ser feita com o comando:
    sudo adduser matheus   - > Na VM1-PC1
    sudo adduser taide     -> Na VM2-PC1
     
    sudo adduser josival   - > Na VM1-PC2
    sudo adduser costa     -> Na VM2-PC2
     
     
#
     
     
### > A comunicação via SSH é feita da seguinte forma:

##### - Da VM1-PC1 para a VM1-PC2
    ssh josival@192.168.24.83
    
<img src="/Projeto/Figuras/PC1/Passo5/vm1-pc1-ssh.png" title="VM1-PC1-SSH-Usando o SSH nas Máquinas Virtuais" width="800" />
    
##### - Da VM2-PC1 para a VM2-PC2:

    ssh costa@192.168.24.84
    
<img src="/Projeto/Figuras/PC1/Passo5/vm2-pc1-ssh.png" title="VM2-PC1-SSH-Usando o SSH nas Máquinas Virtuais" width="800" />

##### - Da VM1-PC2 para a VM1-PC1

    ssh matheus@192.168.24.81
    
<img src="/Projeto/Figuras/PC2/Passo5/vm1-pc2-ssh.png" title="VM1-PC2-SSH-Usando o SSH nas Máquinas Virtuais" width="800" />

##### - Da VM2-PC2 para a VM2-PC1:

    ssh ataide@192.168.24.82
    
<img src="/Projeto/Figuras/PC2/Passo5/vm2-pc2-ssh.png" title="VM2-PC2-SSH-Usando o SSH nas Máquinas Virtuais" width="800" />



> Usar o comando 'exit' para sair do usuário logado
-----------------------------------------------------------------------------------------------------

### > Conclusão
Após o término desse Passo 5, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1-PC2/Passo6.md)
