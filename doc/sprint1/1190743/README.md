RCOMP 2019-2020 Project - Sprint 1 - Member 1190743 folder
===========================================

## Edifício B

Para este projeto, fiquei encarregue de cobrir o Edifício B.
Este edifício, em termos de quantidade de cabo e tomadas é reduzido em relação ao resto dos edifícios deste projeto.


## Piso 0 (Ground Floor)

![Piso_0](GroundZero.png)

### Medidas:

|         | C_real (m) | L_real (m) | Área (m²) | Outlets |
|---------|--------|--------|--------|---------|
| B0      | 60     | 20     | 1200   | 82      |
| 20.2    | 12,75  | 7,2    | 91,8   | 20      |
| 20.3    | 13,8   | 9,3    | 128,34 | 26      |
| 20.4    | 8,27   | 18,62  | 153,99 | 32      |
| Desk    | 8,27   | 1,37   | 11,33  | 4       |


### Inventário:

* 3 Half Rack Enclosure (Para IC, HC e CP):
   * HC -> 12U
   * 2 CP -> 8U (x2)
* 1 IC
* 1 HC:
    * 1 Switch Fibra Ótica 24 Portas
    * 1 Patch Panel Fibra Ótica 24 portas
    * 1 Switch Panel Cobre 48 Portas
    * 1 Patch Panel Cobre 48 Portas
* 2 CP:
    * 2 Switch 48 portas
    * 2 Patch Panel 48 portas
* 2 Access Points
* 2 outlets - Fibra (Para AP)
* 82 outlets - Cobre (RJ45)
* 1500m cable CAT6A
* 450m cable Fibra (40GbbaseSR4 + 100GbbaseSR10)

###Notas:

* Cada Access Point tem a sua própria tomada de fibra, a qual não aparece no esquema, apenas no inventário.
* No HC existem 2 Switch e 2 Patch Panel de modo a conseguir distribuir cobre e fibra para os pontos necessários.
* Os CPs acima apresentados têm 1 Switch e um Patch Panel cada, apenas aparecem em como 2 de modo a generalizar.
* Como redundância, serão sempre 2 cabos em vez de um na fibra, apesar de passarem pelo mesmo sítio.
Outro caminho foi considerado desnecessário uma vez que a cablagem é passada por baixo do edifício.
A medição destes mesmos cabos aparece na tabela abaixo com fundo verde e foram contabilizados no valor total.  
* Apesar a área total do piso ser de 1200m², não foi necessária a colocação de 2 Horizontal Cross-Connects uma vez que apenas metade edifício recorre a cablagem e tomadas.


![Cablagem_Piso0](Cablagem_Piso0.png)

## Piso 1

![Piso_1](GroundOne.png)

Neste piso, toda a cablagem é feita pelo telhado falso, este que fica a 2,5m do chão e o cabo de fibra que vem do piso debaixo foi contabilizado em termos de tamanho.
Ainda que a ligação a tomadas no teto seja desagradável, todas elas foram lá colocadas. Se fosse necessário agradar ao cliente, seria apenas necessário acrescentar 2.5m a todas as tomadas de modo a estas ficarem no chão. Descartou-se esta possibilidade para um menor uso de cablagem.

### Medidas:

|         | C_real (m) | L_real (m) | Área (m²) | Outlets |
|---------|--------|--------|--------|---------|
| B1      | 60     | 20     | 1200   | 116     |
| 21.1    | 3,8    | 5,5    | 20,9   | 6       |
| 21.2    | 4,48   | 8,27   | 37,05  | 8       |
| 21.3    | 5      | 8,27   | 41,35  | 10      |
| 21.4    | 5      | 8,27   | 41,35  | 10      |
| 21.5    | 5      | 8,27   | 41,35  | 10      |
| 21.6    | 5      | 9,31   | 46,55  | 10      |
| 21.7    | 5      | 9,31   | 46,55  | 10      |
| 21.8    | 5      | 9,31   | 46,55  | 10      |
| 21.9    | 6,13   | 13,10  | 80,30  | 18      |
| 21.10   | 11,03  | 4,83   | 53,28  | 12      |
| 21.11   | 11,03  | 4,83   | 53,28  | 12      |

### Inventário:

* 4 Half Rack Enclosure (Para HC e CP) :
    * HC (Sala 21.9) -> 12U
    * HC (Sala 21.3) -> 8U
    * 2 Cp -> 4U (x2)
* 1 HC (Sala 21.9):
    * 1 Switch Fibra Ótica 24 Portas
    * 1 Patch Panel Fibra Ótica 24 portas
    * 1 Switch Cobre 48 portas
    * 1 Patch Panel Cobre 48 portas
* 1 HC (Sala 21.3):
    * 1 Switch Cobre 48 portas
    * 1 Patch Panel Cobre 48 portas  
* 2 CP:
    * 2 Switch 24 portas
    * 2 Patch Panel 24 portas
* 2 Access Points 
* 2 outlets - Fibra (Para AP)  
* 116 outlets - Cobre (RJ45)
* 1200m cable cat6A
* 1000m cable Fibra (40GbbaseSR4 + 100GbbaseSR10)

###Notas:

* Cada Access Point tem a sua própria tomada de fibra, a qual não aparece no esquema, apenas no inventário.
* No HC da sala 21.9 existem 2 Switch e 2 Patch Panel de modo a conseguir distribuir cobre e fibra para os pontos necessários.
* No HC da sala 21.3 apenas existe 1 de cada uma vez que só cobre é utilizado na cablagem das ligações.  
* Os CPs acima apresentados têm 1 Switch e um Patch Panel cada, apenas aparecem em como 2 de modo a generalizar.
* Como redundância, serão sempre 2 cabos em vez de um na fibra, apesar de passarem pelo mesmo sítio.
  O outro caminho utilizado foi à volta do edifício, levando a cabos de fibra com uma distância maior e aumentando significativamente o orçamento e a totalidade de metros de fibra utilizados.
  A medição destes mesmos cabos aparece na tabela abaixo com fundo verde e foram contabilizados no valor total.
* Neste piso já foi necessária a utilização de 2 Horizontal Cross-Connects.



![Cablagem_Piso1](Cablagem_Piso1.png)

