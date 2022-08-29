## Configuração dos endereços IPs

```
Tabela 1: Definições de endereços IPs da Rede

|  Descrição  |        IP       |
|-------------|-----------------|
|    rede     |  192.168.24.80  |
|   máscara   | 255.255.255.240 |
|   Gateway   |  192.168.24.81  | 
|   VM1-PC1   |  192.168.24.81  |
|   VM2-PC1   |  192.168.24.82  |
|   VM1-PC2   |  192.168.24.83  |
|   VM2-PC2   |  192.168.24.84  |
|   VM1-PC3   |  192.168.24.85  |
|   VM2-PC3   |  192.168.24.86  |
|   VM1-PC4   |  192.168.24.87  |
|   VM2-PC4   |  192.168.24.88  |
```

## Configuração do serviço de nomes estáticos
```
Tabela 2: Definições de endereços IPs da Rede e Nomes de Hosts
-----------------------------------------------------------------------------------------------------------------------------------------------------------
|                   Responsável                       |  DESCRIÇÃO  |       IP        |   hostname        |               FQDN               |   aliase   |
-----------------------------------------------------------------------------------------------------------------------------------------------------------
| [Matheus Ataide](https://github.com/Matheus-Ataide) |   VM1-PC1   | 192.168.24.81   |   srv-vm1-pc1     | matheus1.grupo6-924.ifalara.net  |   matheus  |
                                                      |   VM2-PC1   | 192.168.24.82   |   srv-vm2-pc1     | matheus2.grupo6-924.ifalara.net  |   ataide   |
| [Josival Costa](https://github.com/Josival)         |   VM1-PC2   | 192.168.24.83   |   srv-vm1-pc2     | josival1.grupo6-924.ifalara.net  |   josival  |
                                                      |   VM2-PC2   | 192.168.24.84   |   srv-vm2-pc2     | josival2.grupo6-924.ifalara.net  |   costa    |
| [Clara Leão](https://github.com/mariaclaraleao)     |   VM1-PC3   | 192.168.24.85   |   srv-vm1-pc3     | clara1.grupo6-924.ifalara.net    |   clara    |
                                                      |   VM2-PC3   | 192.168.24.86   |   srv-vm2-pc3     | clara2.grupo6-924.ifalara.net    |   leao     |
| Outro cara                                          |   VM1-PC4   | 192.168.24.87   |   srv-vm1-pc4     | cara1.grupo6-924.ifalara.net     |   cara1    |
                                                      |   VM2-PC4   | 192.168.24.88   |   srv-vm2-pc4     | cara2.grupo6-924.ifalara.net     |   cara2    |
-----------------------------------------------------------------------------------------------------------------------------------------------------------
```
* IP: nosso número de identificação única para cada máquina utilizada.
* hostname: nome da nossa máquina onde está vinculada ao IP.
* FQDN: endereço estático associado ao IP.
* aliases: nome atribuído ao IP.

## Configuração de hardware
```
Tabela 3: Configuração dos hardware das VMs
---------------------------------------------------------------------------------------------------------------------------------
|  DESCRICAO  |       IP        |   PROCESSADORES   |    ESPAÇO EM DISCO    |   QUANTIDADE DE MEMÓRIA  |   SISTEMA OPERACIONAL  |
---------------------------------------------------------------------------------------------------------------------------------
| VM1-PC1     | 192.168.24.81   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
| VM2-PC1     | 192.168.24.82   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
| VM1-PC2     | 192.168.24.83   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
| VM2-PC2     | 192.168.24.84   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
| VM1-PC3     | 192.168.24.85   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
| VM2-PC3     | 192.168.24.86   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
| VM1-PC4     | 192.168.24.87   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
| VM2-PC4     | 192.168.24.88   |         1         |         10 GB         |          4.60 GB         |      Ubuntu (64-bit)   |
---------------------------------------------------------------------------------------------------------------------------------
``` 

## Configuração dos usuários
```
Tabela 4: Definições dos nomes de usuários e senha 
------------------------------------------------
|  DESCRIÇÃO  |     USUÁRIOS    |     SENHA    |
------------------------------------------------
| VM1-PC1     |      matheus    |   adminifal  |
| VM2-PC1     |      ataide     |   adminifal  |
| VM1-PC2     |      josival    |   adminifal  |
| VM2-PC2     |      costa      |   adminifal  |
| VM1-PC3     |      clara      |   adminifal  | 
| VM2-PC3     |      leao       |   adminifal  |
| VM1-PC4     |      cara1      |   adminifal  |
| VM2-PC4     |      cara2      |   adminifal  |
------------------------------------------------
```

## Alocação dos PC' utilizados

#### Tabela 5: PC's físicos reservados para cada máquina

|                   RESPONSÁVEL                       |  DESCRIÇÃO  |   PC FÍSICO   |
|-----------------------------------------------------|-------------|---------------|
| [Matheus Ataide](https://github.com/Matheus-Ataide) |     PC1     | LAB 1 - PC 09 |
| [Josival Costa](https://github.com/Josival)         |     PC2     | LAB 1 - PC 10 | 
| [Clara Leão](https://github.com/mariaclaraleao)     |     PC3     | LAB 1 - PC 11 |
| Outro cara                                          |     PC4     | LAB 1 - PC 12 |
