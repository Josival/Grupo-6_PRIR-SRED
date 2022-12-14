# Passo 4 - Conexão entre as VMs via cabo ethernet

####  > Para fazer a comunicação entre as VMs de PCs diferentes, usando a conexão ponto a ponto, utiliza-se o cabo Ethernet 
> Como pode ser visto na figura:
<p align = "center">
<img src="/Projeto/Figuras/PC3/Passo4/cabo-pc.jpeg" title="Topologia de Física" width="400" />
</p>

#### > Para o êxito da conexão, é necessária uma mudança nas configurações de rede das VMs, o modo ``rede interna`` será substituído para ``Placa em modo Bridge`` 

> Você deve realizar essas configurações nas quatro VM's dos dois PC's. Como pode ser visualizado nas figuras a seguir:

<p align = "center">
<img src="/Projeto/Figuras/PC1/Passo4/modobridge.png" title="Conexão entre as VMs Via Cabo Ethernet" width="950" />
</p>

#### > Novamente utiliza-se o ping para o estabelecimento da comunicação, que agora é entre máquinas virtuais de PCs distintos. Para isso, é utilizado o seguinte comando:

- Acesse o diretório com os [Testes dos Ping's das VM's do PC 3 e PC 4](https://github.com/Josival/Grupo-6_PRIR-SRED/blob/main/TestesDaRede/Testes:PC3-PC4/Pings.md)

### > Conclusão
Após o término desse Passo 4, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC3-PC4/Passo5.md)
