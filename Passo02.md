##  Em ambas máquinas Virtuais: 

###  Usar o usuário da VM:
      administrador
#### Senha:
      adminifal

###   Instalação do net-tools:
      sudo apt install net-tools -y

###    Para poder editar as configurações de ips, máscara de hosts, dhcp, usa-se:
      sudo nano /etc/netplan/01-netcfg.yaml
 // Foto mostrando o sudo nano, como está no momento(sem nenhuma alteração):

###    Mudanças no sudo nano:
addresses: [192.168.24.87/28]     => IP estático da VM1-PC4
addresses: [192.168.24.88/28]     => IP estático da VM2-PC4

##    Para aplicar as mudanças feitas no comando anterior;
  sudo netplan apply
Foto mostrando o sudo nano, após as alterações:

Para ver todas as interfaces configuradas usa-se:
  ifconfig ou ifconfig -a

##  Nas configurações de rede das máquinas virtuais, alterar do modo NAT para a rede interna, como mostrado na foto:

    Para verificar se as máquinas estão se conectando usa-se o ping, como pode ser visto a |seguir:
Da VM1-PC4 para a VM2-PC4:
  ping 192.168.24.88
Da VM2-PC4 para a VM1-PC4:
  ping 192.168.24.87

