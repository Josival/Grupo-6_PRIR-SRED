# Passo 4 - Conexão entre as VMs via cabo ethernet

####  Para fazer a comunicação entre as VMs de PCs diferentes, usando a conexão ponto a ponto, utiliza-se o cabo Ethernet. 
> Como pode ser visto na foto:
<img src="/Projeto/Figuras/PC1/Passo4/cabo-pc.jpeg" title="Topologia de Física" width="400" />

####  Para o êxito da conexão, é necessária uma mudança nas configurações de rede das VMs, o modo rede interna será substituído para placa em modo Bridge. 
> Como pode ser visualizado na foto a seguir:
- **VM1-PC1:**
<img src="/Projeto/Figuras/PC1/Passo4/vm1-pc1-bridge.png" title="VM1-PC1-Conexão entre as VMs Via Cabo Ethernet" width="1000" />

- **VM2-PC1:**
<img src="/Projeto/Figuras/PC1/Passo4/vm2-pc1-bridge.png" title="VM2-C1-Conexão entre as VMs Via Cabo Ethernet" width="1000" />

####  Novamente utiliza-se o ping para o estabelecimento da comunicação, que agora é entre máquinas virtuais de PCs distintos. Para isso, é utilizado o seguinte comando:

- Da VM1-PC2  para a VM1-PC1
      ping 192.168.24.81
- Da VM1-PC1  para a VM1-PC2
      ping 192.168.24.83
      
- Da VM2-PC2  para a VM2-PC1
      ping 192.168.24.82
- Da VM2-PC1  para a VM2-PC2
      ping 192.168.24.84

### > Conclusão
Após o término desse Passo 4, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1-PC2/Passo5.md)
