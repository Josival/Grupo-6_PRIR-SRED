# Passo 4 | Conexão entre as VMs via cabo ethernet

#####  Para fazer a comunicação entre as VMS de pcs diferentes, usando a conexão ponto a |ponto, usa-se o cabo ethernet, como pode ser visto na foto:

#####  E mudar nas configurações de rede das VMS, o modo rede interna, para placa em modo |Bridge, como pode ser visualizado na foto a seguir: 

####  Novamente usa-se o ping para ocorrer a comunicação, que agora é entre máquinas virtuais |de pcs distintos, nisso, é usado o seguinte comando:

######    Da VM1-PC2  para a VM2-PC1
      ping 192.168.24.82
######    Da VM2-PC2  pra a VM1-PC1
      ping 192.168.24.81
