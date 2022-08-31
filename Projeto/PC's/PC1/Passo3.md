# Passo 3 - Configurações iniciais das Máquinas Virtuais

- Após o passo anterior inicie as Máquinas Virtuais para fazer as seguintes configurações:

### - Na VM1-PC1

#### > Usar o usuário da VM:
     administrador

#### > Instalação do net-tools:
     sudo apt install net-tools -y  
 
#### > Para poder editar as configurações de ips e dhcp usa-se:
     sudo nano /etc/netplan/01-netcfg.yaml

#### > Mudança no sudo nano:

> Figura mostrando o sudo nano, após as alterações:

<p align = "center">
<img src="/Projeto/Figuras/PC1/Passo3/vm1-pc1-sudonano.png" title="VM1-PC1-Configurações Iniciais das Máquinas Virtuais" width="950" />
</p>
     
#### > Para aplicar as mudanças feitas no comando anterior;
     sudo netplan apply

#

### - Na VM2-PC1

#### > Usar o usuário da VM:
     administrador

#### > Instalação do net-tools:
     sudo apt install net-tools -y  
 
#### > Para poder editar as configurações de ips, máscara de hosts, dhcp, usa-se:
     sudo nano /etc/netplan/01-netcfg.yaml

#### > Mudança no sudo nano:

> Figura mostrando o sudo nano, após as alterações:

<p align = "center">
<img src="/Projeto/Figuras/PC1/Passo3/vm2-pc1-sudonano.png" title="VM2-PC1-Configurações Iniciais das Máquinas Virtuais" width="950" />
</p>
     
#### > Para aplicar as mudanças feitas no comando anterior;
     sudo netplan apply

#

#### > Para ver todas as interfaces configuradas usa-se:
     ifconfig ou ifconfig -a

#

#### > Nas configurações de rede das máquinas virtuais, alterar do modo NAT para a rede interna, como mostrado nas figuras:

#### - VM1-PC1:
<p align = "center">
<img src="/Projeto/Figuras/PC1/Passo3/vm1-pc1-redeinterna.png" title="VM1-PC1-Configurações Iniciais das Máquinas Virtuais" width="950" />
</p>

#### - VM2-PC1:
<p align = "center">
<img src="/Projeto/Figuras/PC1/Passo3/vm2-pc1-redeinterna.png" title="VM1-PC1-Configurações Iniciais das Máquinas Virtuais" width="950" />
</p>

#### > Para verificar se as máquinas estão se conectando usa-se o ping, como pode ser visto a seguir:

##### - Da VM1-PC1 para a VM2-PC1:
     ping 192.168.24.82
##### - Da VM2-PC1 para a VM1-PC1:
     ping 192.168.24.81

#

### > Conclusão
Antes de ir para o passo 4, [configure ás maquinas virtuais do PC2](). Se o PC2 já estiver configurado, continue no [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1-PC2/Passo4.md)
