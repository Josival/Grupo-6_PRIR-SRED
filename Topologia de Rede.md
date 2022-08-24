### Topologia da Rede

* A topologia utilizada na rede é do tipo estrela, nessa topologia os computadores são todos conectados a um hub (switch) central que atua conectando todas as máquinas. 

* A rede vai possuir 4 PCs conectados entre si a partir dos cabos ethernet e um switch físico, com suas respectivas configurações de rede. Dentro de cada PC será criado 2 VMs, onde todas as VMs criadas poderão se conectar através dos switches virtuais das VMs e do switch físico com seus cabos de rede (ethernet). Sendo assim será possível conectar-se entre elas. No nosso exemplo, fizemos login em usuários criados nestas VMs para evidenciar essa conexão. 

* Segue a imagem da topologia da rede:

<p><center> Figura 1: Topologia de Rede estrela, com oito VMs com suas NICs em modo BRIDGE</center></p>   
<img src="figures/star-network.svg" title="Figura 1: Topologia de Rede Estrela" width="1000" />
