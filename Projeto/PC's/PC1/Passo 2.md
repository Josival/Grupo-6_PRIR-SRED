# Passo 2- Criação das VMs da rede

Para a criação das VMs, vamos importar a imagem .OVA, ele será necessário para a construção da rede.

* .OVA é um pacote que contém arquivos usados para descrever uma máquina virtual, que inclui um arquivo descritor .OVF, manifesto opcional (.MF) e arquivos de certificado e outros arquivos relacionados. 

### Segue os passos de importação na Figura 1 e 2:

![image](https://user-images.githubusercontent.com/86027160/183978615-8366e422-6321-4bcb-b040-48e634fb4740.png)

![image](https://user-images.githubusercontent.com/86027160/183981533-6beca288-3e86-40e2-9c9d-94928950bb6d.png)

* Um ponto a ressaltar é na `configuração de "Política de Endereço MAC"`, onde é preciso que deixe como `Gerar novos endereços MAC para todas as placas de rede` para que para cada interface de rede seja criado um novo endereço MAC.

### > Conclusão
Após o término desse Passo 2, direcione para o [Próximo Passo](https://github.com/Josival/TrabalhoRedes/blob/main/Projeto/PC's/PC1/Passo3.md)
