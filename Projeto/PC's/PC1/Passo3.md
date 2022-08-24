# Passo 3 - Configurações iniciais das Máquinas Virtuais

### > Na VM1-PC1

#### - Usar o usuário da VM:
     administrador
##### Senha:
     adminifal

#### - Instalação do net-tools:
     sudo apt install net-tools -y  
 
#### - Para poder editar as configurações de ips, máscara de hosts, dhcp, usa-se:
     sudo nano /etc/netplan/01-netcfg.yaml
          
Foto mostrando o sudo nano, como está no momento(sem nenhuma alteração):

#### - Mudança no sudo nano:
     addresses: [192.168.24.81/28]     => IP estático da VM1-PC1

#### - Para aplicar as mudanças feitas no comando anterior;
     sudo netplan apply
Foto mostrando o sudo nano, após as alterações:



### > Na VM2-PC1

#### - Usar o usuário da VM:
     administrador
##### Senha:
     adminifal

#### - Instalação do net-tools:
     sudo apt install net-tools -y  
 
#### - Para poder editar as configurações de ips, máscara de hosts, dhcp, usa-se:
     sudo nano /etc/netplan/01-netcfg.yaml
Foto mostrando o sudo nano, como está no momento(sem nenhuma alteração):

#### - Mudança no sudo nano:
     addresses: [192.168.24.82/28]     => IP estático da VM1-PC1

#### - Para aplicar as mudanças feitas no comando anterior;
     sudo netplan apply
Foto mostrando o sudo nano, após as alterações:

#### - Para ver todas as interfaces configuradas usa-se:
     ifconfig ou ifconfig -a

* Nas configurações de rede das máquinas virtuais, alterar do modo NAT para a rede interna, como mostrado na foto:

#### - Para verificar se as máquinas estão se conectando usa-se o ping, como pode ser visto a |seguir:

##### Da VM1-PC1 para a VM2-PC1:
     ping 192.168.24.82
##### Da VM2-PC1 para a VM1-PC1:
     ping 192.168.24.81

### > Conclusão
Antes de ir para o passo 4, [configure ás maquinas virtuais do PC2](). Se o PC2 já estiver configurado, continue no [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1-PC2/Passo4.md):
