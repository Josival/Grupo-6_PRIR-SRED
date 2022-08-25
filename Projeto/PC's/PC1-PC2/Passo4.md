# Passo 4 - Conexão entre as VMs via cabo ethernet

####  Para fazer a comunicação entre as VMs de PCs diferentes, usando a conexão ponto a ponto, utiliza-se o cabo Ethernet. 
##### Como pode ser visto na foto:

####  Para o êxito da conexão, é necessária uma mudança nas configurações de rede das VMs, o modo rede interna será substituído para placa em modo Bridge. 
##### Como pode ser visualizado na foto a seguir: 

####  Novamente utiliza-se o ping para o estabelecimento da comunicação, que agora é entre máquinas virtuais de PCs distintos. Para isso, é utilizado o seguinte comando:

######    Da VM1-PC2  para a VM1-PC1
      ping 192.168.24.81
######    Da VM1-PC1  para a VM1-PC2
      ping 192.168.24.83
      
######    Da VM2-PC2  pra a VM2-PC1
      ping 192.168.24.82
######    Da VM2-PC1  pra a VM2-PC2
      ping 192.168.24.84

### > Conclusão
Após o término desse Passo 4, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1-PC2/Passo5.md)
