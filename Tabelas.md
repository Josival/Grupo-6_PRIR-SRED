# PROJETO E INFRAESTRUTURA DE REDES - GRUPO 6  - 924

### Tabela 1: Responsáveis por máquina e Designação dos respectivos endereços IPs 
 
|                    Responsável                      | Máquina |      IP       |
|-----------------------------------------------------|---------|---------------|
|[Matheus Ataide](https://github.com/Matheus-Ataide)  | VM1-PC1 | 192.168.24.81 |
|                                                     | VM2-PC1 | 192.168.24.82 |
|[Josival Costa](https://github.com/Josival)          | VM1-PC2 | 192.168.24.83 |
|                                                     | VM2-PC2 | 192.168.24.84 |
|[Clara Leão](https://github.com/mariaclaraleao)      | VM1-PC3 | 192.168.24.85 |
|                                                     | VM2-PC3 | 192.168.24.86 |
|Outro cara                                           | VM1-PC4 | 192.168.24.87 |
|                                                     | VM2-PC4 | 192.168.24.88 |

## Configuração do serviço de nomes estáticos

```
Tabela 2: Definições de endereços IPs da Rede e Nomes de Hosts
-----------------------------------------------------------------------------------------------------
|  DESCRIÇÃO  |       IP        |   hostname        |               FQDN               |   aliase   |
-----------------------------------------------------------------------------------------------------
| rede        | 192.168.24.80   |                   |                                  |            |
| máscara     | 255.255.255.240 |                   |                                  |            |
| Gateway     | 192.168.24.81   |                   |                                  |            |
| VM1-PC1     | 192.168.24.81   |   srv-vm1-pc1     | matheus1.grupo6-924.ifalara.net  |   matheus  |
| VM2-PC1     | 192.168.24.82   |   srv-vm2-pc1     | matheus2.grupo6-924.ifalara.net  |   ataide   |
| VM1-PC2     | 192.168.24.83   |   srv-vm1-pc2     | josival1.grupo6-924.ifalara.net  |   josival  |
| VM2-PC2     | 192.168.24.84   |   srv-vm2-pc2     | josival2.grupo6-924.ifalara.net  |   costa    |
| VM1-PC3     | 192.168.24.85   |   srv-vm1-pc3     | clara1.grupo6-924.ifalara.net    |   clara    |
| VM2-PC3     | 192.168.24.86   |   srv-vm2-pc3     | clara2.grupo6-924.ifalara.net    |   leao     |
| VM1-PC4     | 192.168.24.87   |   srv-vm1-pc4     | cara1.grupo6-924.ifalara.net     |   cara1    |
| VM2-PC4     | 192.168.24.88   |   srv-vm2-pc4     | cara2.grupo6-924.ifalara.net     |   cara2    |
-----------------------------------------------------------------------------------------------------
```

```
Tabela 3: PC's físicos reservados para cada máquina
-------------------------------
|  DESCRICAO  |   PC FÍSICO   |
-------------------------------
|     PC1     | LAB 1 - PC 09 |
|     PC2     | LAB 1 - PC 10 | 
|     PC3     | LAB 1 - PC 11 |
|     PC4     | LAB 1 - PC 12 |
-------------------------------
```
