# Passo 5 - Usando o SSH nas máquinas virtuais

### - Na VM1-PC3 

#### > Alterar a rede para o modo NAT, como na figura:

<p align = "center">
<img src="/Projeto/Figuras/PC3/Passo5/vm1-pc3-redenat.png" title="VM1-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, no terminal da Máquina Virtual. Como é apresentado na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/vm1-pc3-sudonat.png" title="VM1-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do hostname na VM1-PC3 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm1-pc3

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/status das portas.png" title="Status da Porta" width="900" />

#### > Para a configuração do firewall, necessário para garantir que as portas estejam funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh    # ativa o ssh no firewall UFW do ubuntu
    
#### > Para ativar o firewall:

    sudo ufw enable
    
#### > Para verificar o status do firewall    
     
     sudo ufw status  

> Como pode ser visto na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/configuração do firewall.png" title="Status da Porta" width="900" />


#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo nas figuras:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/vm1-pc3-bridge.png" title="vm1-pc3-Bridge" width="900" />

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo3/vm1-pc3-sudonano.png" title="vm1-pc3-sudonano-bridge" width="900" />

-------------------------------------------------------------------------------------------------------------

### - Na VM2-PC3

#### > Alterar a rede para o modo NAT, como na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/vm2-pc3-redenat.png" title="VM2-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="1000" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, no terminal da Máquina Virtual. Como é apresentado na figura::
     
<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/vm2-pc3-sudonat.png" title="VM2-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do hostname na VM2-PC3 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm2-pc3

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/status das portas.png" title="Status da Porta" width="900" />

#### > Para a configuração do firewall, necessário para garantir que as portas estejam funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh    # ativa o ssh no firewall UFW do ubuntu
    
#### > Para ativar o firewall:

    sudo ufw enable
    
#### > Para verificar o status do firewall    
     
     sudo ufw status  

> Como pode ser visto na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/configuração do firewall.png" title="Status da Porta" width="900" />

#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo nas figuras:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/vm2-pc3-bridge.png" title="vm2-pc3-Bridge" width="900" />

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo3/vm2-pc3-sudonano.png" title="vm1-pc3-sudonano-bridge" width="900" />

--------------------------------------------------------------------------

### - Na VM1-PC4

#### > Alterar a rede para o modo NAT, como na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm1-pc4-redenat.png" title="VM1-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="1000" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, no terminal da Máquina Virtual. Como é apresentado na figura::
     
<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm1-pc4-sudonat.png" title="VM1-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do hostname na VM1-PC4 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm1-pc4

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/status das portas.png" title="Status da Porta" width="900" />

#### > Para a configuração do firewall, necessário para garantir que as portas estejam funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh    # ativa o ssh no firewall UFW do ubuntu
    
#### > Para ativar o firewall:

    sudo ufw enable
    
#### > Para verificar o status do firewall    
     
     sudo ufw status  

> Como pode ser visto na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/configuração do firewall.png" title="Status da Porta" width="900" />

#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo nas figuras:

<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm1-pc4-bridge.png" title="vm1-pc4-Bridge" width="900" />

<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm1-pc4-sudobridge.png" title="vm1-pc3-sudonano-bridge" width="900" />

-----------------------------------------------------------------------------

### - Na VM2-PC4

#### > Alterar a rede para o modo NAT, como na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm2-pc4-redenat.png" title="VM2-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="1000" />
     
#### > Comentar as linhas de endereçamento IP estático e ativar o DHCP, no terminal da Máquina Virtual. Como é apresentado na figura:
     
<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm2-pc4-sudonat.png" title="VM2-PC3-NAT-Usando o SSH nas Máquinas Virtuais" width="900" />

#### > Para atribuir o nome do hostname na VM2-PC4 é utilizado o comando:

    sudo hostnamectl set-hostname srv-vm2-pc4

#### > Para atualizar a VM, foram usados os comandos a seguir:

    sudo apt update  
    sudo apt upgrade -y 
> Atenção, isso pode demorar um pouco!

#### > Para a instalação do SSH, que proporciona a conexão via internet, foi utilizado o comando:

    sudo apt-get install openssh-server

#### > Para verificar o status das portas do sistema, foi utilizado:

    netstat -an | grep LISTEN.  #verifique as conexões TCP na porta 22 se está como LISTENING
    
> Como pode ser visto na figura:

<p align = "center">     
<img src="/Projeto/Figuras/PC3/Passo5/status das portas.png" title="Status da Porta" width="900" />

#### > Para a configuração do firewall, necessário para garantir que as portas estejam funcionando corretamente, são utilizados os seguintes comandos:

    sudo ufw allow ssh    # ativa o ssh no firewall UFW do ubuntu
    
#### > Para ativar o firewall:

    sudo ufw enable
    
#### > Para verificar o status do firewall    
     
     sudo ufw status  

> Como pode ser visto na figura:

<img src="/Projeto/Figuras/PC3/Passo5/configuração do firewall.png" title="Status da Porta" width="900" />

#### > Alterar a rede para o modo bridge, descomentar os endereços IPs estáticos e desativar o DHCP.

> Como pode ser notado abaixo nas figuras:

<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm2-pc4-bridge.png" title="vm2-pc4-Bridge" width="900" />

<p align = "center">     
<img src="/Projeto/Figuras/PC4/Passo5/vm2-pc4-sudobridge.png" title="vm1-pc3-sudonano-bridge" width="900" />
    
-----------------------------------------------------------------------------------------------------

####  > Fazer o uso do ping entre as máquinas para verificar se está ocorrendo a comunicação e se tudo foi configurado corretamente:

- Acesse o diretório com os [Testes dos Ping's das VM's do PC 3 e PC 4](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/TestesDaRede/Testes:PC3-PC4/Pings.md)

#

##### > Criação de novos usuários para as VMs, para a comunicação via ssh, pode ser feita com o comando:
    sudo adduser matheus   ->   Na VM1-PC3
    sudo adduser ataide    ->   Na VM2-PC3
     
    sudo adduser josival   ->   Na VM1-PC4
    sudo adduser costa     ->   Na VM2-PC4
     
#
     
### > A comunicação via SSH é feita da seguinte forma:

- Acesse o diretório com os [Testes dos SSH's das VM's do PC 3 e PC 4](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/TestesDaRede/Testes:PC3-PC4/SSH.md)

-----------------------------------------------------------------------------------------------------

### > Conclusão
Após o término desse Passo 5, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC3-PC4/Passo6.md)
