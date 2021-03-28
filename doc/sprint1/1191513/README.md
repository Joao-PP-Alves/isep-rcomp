RCOMP 2020-2021 Project - Sprint 1 - Member 1191513 folder


## Edifício 1

Este Edifício é o principal em termos de rede informática pois é neste que se encontra 
instalado o DataCenter que abastecerá todos os outros edifícios deste campus. Será então
aqui alojado o Main Cross-connect (MC) onde se inicia o backbone desta rede.

### Pressupostos:
* Todos os equipamentos incluídos na cable subsystem 3 e 2 (MC, ICs, HCs) bem como os APs e CPs têm entrada de fibra óptica. Estes equipamentos foram dimensionados apenas para suprimir as necessidades indicadas no ficheiro deste sprint, ou seja, não contemplam futuras expansões da rede apesar de existir a possibilidade de alguns deles poderem ainda ter portas de saída disponíveis.
* A difusão da rede pelos Access Points não sofre atenuação das paredes. Assim sendo, dadas as dimensões do edifício, é possível colocar apenas 1 célula por piso, conseguindo uma cobertura total dos dois pisos pois não existe nenhum ponto a mais de 25 metros. De forma a evitar interferências desnecessárias entre estes 2 APs, um difundirá no canal 1 e o outro no canal 11.
* Todas as medidas foram recolhidas utilizando uma régua ajustada à escala respetiva de cada imagem.

## Piso 0 (Ground Floor)

![Piso_0](B1G0-Final.jpg)

#### Medidas (Por Sala):

| Medidas   | Compr (m) | Larg (m)  | A (m²)    | Outlets   |
|---        |---        |---        |---        |---        |
| 10.1      | 11.5      | 7.3       | 83.95     | 18        |
| 10.2      | 11.5      | 11        | 126.5     | 26        |
| Desk      | -         | -         | -         | 5        |

#### Notas:
* Horizontal Cross-connect do piso 0 presente na sala 10.2, com 48 saídas, abastece essa mesma sala (26 outlets), o Access Point e o Consolidation point.
* Consolidation Point do piso 0 presente na sala 10.1, com 24 portas de saída, abastece essa mesma sala (18 outlets) e a mesa da sala 10.3 (5 outlets).
* Redundância foi implementada para todos os cabos de fibra ótica dimensionados.

#### Inventário:
* Telecommunications enclosure (HC, 10U size)
    * 1 Switch com entrada fibra ótica e 48 ethernet outlets
    * 1 Patch panel de 48 ethernet outlets
    * 1 Switch com pelo menos 2 saídas de fibra ótica e respetivo Patch panel

* Telecommunications enclosure (CP, 4U size)
    * 1 Switch fibra ótica com patch panel de 24 ethernet outlets)
    * 1 Patch panel de 24 ethernet outlets
* 1 AP 
* 52 Outlets
    * 49 RJ45 Outlets
    * 3 Fibre Outlets
* 49 RJ45 Patch cords
* 950 metros cabo cobre CAT6A
* 100 metros cabo fibra ótica categoria 40GbaseSR4
    

## Piso 1 (First Floor)

![Piso_1](B1G1-Final.jpg)

| Medidas   | Compr (m) | Larg (m)  | A (m²)    | Outlets   |
|---        |---        |---        |---        |---        |
| 11.1      | -         | -         | -          | -         |
| 11.2      | 7.5       | 5.5       | 41.25     | 10        |
| 11.3      | 11.5      | 7         | 80.5      | 18        |
| 11.4      | 11.5      | 11        | 126.5     | 26        |
| 11.5      | -         | -         | -         | -         |

#### Notas:
* Horizontal Cross-connect do piso 1 presente na sala 11.1, com 24 portas de saída, abastece a sala 11.2 (10 outlets), o Access Point e o Consolidation point.
* Consolidation Point do piso 1 presente na sala 11.3, com 48 portas de saída, abastece essa mesma sala (18 outlets) e a sala 11.4 (26 outlets).
* Redundância foi implementada para todos os cabos de fibra ótica dimensionados.

#### Inventário:
* 1 MC-IC
* Telecommunications enclosure (HC, 6U size)
    * 1 Switch com entrada fibra ótica e 24 ethernet outlets
    * 1 Patch panel de 24 ethernet outlets
    * 1 Switch com pelo menos 2 saídas de fibra ótica e respetivo Patch panel

* Telecommunications enclosure (CP, 8U size)
    * 1 Switch fibra ótica com patch panel de 48 ethernet outlets)
    * 1 Patch panel de 48 ethernet outlets
    
* 1 AP
*  Outlets 
    * 54 RJ45 Outlets
    * 3 Fibre Outlets 
* 54 Patch cords
* 780 metros cabo cobre CAT6A
* 90 metros cabo fibra ótica categoria 40GbaseSR4

#### Dimensionamento da cablagem:
![Cable_measurement](excel.jpg)
