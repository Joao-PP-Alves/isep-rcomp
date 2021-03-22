RCOMP 2020-2021 Project - Sprint 1 - Member 1191513 folder
===========================================
(This folder is to be created/edited by the team member 1191513 only)

#### This is just an example for a team member with number 1191513 ####
### Each member should create a folder similar to this, matching his/her number. ###
The owner of this folder (member number 1191513) will commit here all the outcomes (results/artifacts/products)		       of his/her work during sprint 1. This may encompass any kind of standard file types.


## Edifício 1

Este Edifício é o principal em termos de rede informática pois é neste que se encontra 
instalado o DataCenter que abastecerá todos os outros edifícios deste campus. Será então
aqui alojado o Main cross-connect (MC) onde se inicia o backbone desta rede.

### Pressupostos:
* Todos os equipamentos incluidos na cable subsystem 2 (APs, HCs, CPs, etc.) têm entrada de fibra óptica. Estes equipamentos foram dimensionados apenas para suprimir as necessidades indicadas no ficheiro deste sprint, ou seja, não contemplam futuras expansões da rede apesar de existir a possibilidade de alguns deles poderem ainda ter portas de saída disponíveis.
* A difusão da rede pelos Access Points não sofre atenuação das paredes. Assim sendo, dadas as dimensões do edifício, é possível colocar apenas 1 célula por piso, conseguindo uma cobertura total dos dois pisos pois não existe nenhum ponto a mais de 25 metros.


## Piso 0 (Ground Floor)

![Piso_0](.png)

#### Medidas (Por Sala):

| Medidas   | Compr (m) | Larg (m)  | A (m²)    | Outlets   |
|---        |---        |---        |---        |---        |
| 10.1      | 11.5      | 7.3       | 83.95     | 18        |
| 10.2      | 11.5      | 11        | 126.5     | 26        |
| Desk      | -         | -         | -         | 5        |




#### Inventário:
* 52 Outlets
    * 49 RJ45 Outlets
    * 3 Fibre Outlets
    
#### Notas:
* Horizontal Cross-connect do piso 0 presente na sala 10.2, com 48 saídas, abastece essa mesma sala (26 outlets), o Access Point e o Consolidation point.
* Consolidation Point do piso 0 presente na sala 10.1, com 24 portas de saída, abastece essa mesma sala (18 outlets) e a mesa da sala 10.3 (5 outlets).

## Piso 1 (First Floor)

![Piso_1](.png)

| Medidas   | Compr (m) | Larg (m)  | A (m²)    | Outlets   |
|---        |---        |---        |---        |---        |
| 11.1      | -         | -         | -          | -         |
| 11.2      | 7.5       | 5.5       | 41.25     | 10        |
| 11.3      | 11.5      | 7         | 80.5      | 18        |
| 11.4      | 11.5      | 11        | 126.5     | 26        |
| 11.5      | -         | -         | -         | -         |


#### Inventário:
*  Outlets 
    * 54 RJ45 Outlets
    * 3 Fibre Outlets

#### Notas:
* Horizontal Cross-connect do piso 1 presente na sala 11.1, com 24 portas de saída, abastece a sala 11.2 (10 outlets), o Access Point e o Consolidation point.
* Consolidation Point do piso 1 presente na sala 11.3, com 48 portas de saída, abastece essa mesma sala (18 outlets) e a sala 11.4 (26 outlets).
