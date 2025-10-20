# TDE 2 Performance em Sistemas Ciberfísicos
## Membros do grupo:
- **Letícia Miniuk Rosa Pereira**
- **Rayssa Gaievica Grafetti**
- **Victor Willian Rodrigues Bittencourt**
## Descrição:
A atividade consiste na realização dos seguintes, em um vídeo de até 10 minutos:

Implementação em Python:
- O algoritmo MRU;
- O Algoritmo LRU;
- O algoritmo FIFO;
  
1  - Teste com a sequencia de paginas para 8 quadros:
a ) 4,3,25,8,19,6,25,8,16,35,45,22,8,3,16,25,7
Qual quadro na memória possuirá a página 7?

 b)  4,5,7,9,46,45,14,4,64,7,65,2,1,6,8,45,14,11
Qual quadro na memória possuirá a página 11?

 c) 4,6,7,8,1,6,10,15,16,4,2,1,4,6,12,15,16,11 
qual quadro na memória possuirá a página 11?

2 - Qual a melhor politica de substituição?


### Resultados
Tudo foi respondido e explicado no vídeo <br>
Link do vídeo: **[MAPEAMENTO MEMÓRIA CACHE](https://youtu.be/d7ZrditEWv8)**



## Explicação dos códigos:
- MRU:<br>
  A função começa com uma lista vazia representando os quadros de memória, e um contador de faltas de página zerado.
  Depois analisa cada número da sequência de páginas e, se o número já estiver na lista de quadros, remove essa página de onde   ela está e a adiciona novamente no final da lista. Se o número não estiver na lista, temos uma falta de página. Se ainda       tiver espaço na lista de quadros, a nova página é adicionada ao final da lista, se não, ele remove a página do final da        lista (a usada mais recentemente) e adiciona a nova página no lugar. Cada vez que isso acontece, o contador de page fault      aumenta em 1, e finaliza retornando o estado final dos quadros de memória e o total de page faults (soma pgf + quad), pois o     primeiro preenchimento da memória também conta como uma falta de página para cada quadro.

- LRU:<br>
  A função começa com uma lista vazia representando os quadros de memória, e um contador de faltas de página zerado. Depois      analisa cada número da sequência de páginas e, se o número já estiver na lista de quadros, remove essa página de onde ela      está e a adiciona novamente no final da lista. Se o número não estiver na lista, temos uma falta de página. Se ainda tiver     espaço na lista de quadros, a nova página é adicionada ao final da lista, se não, ele remove a página do início da lista (a    usada menos recentemente) e adiciona a nova página no lugar. Cada vez que isso acontece, o contador de page fault aumenta em   1, e finaliza retornando o estado final dos quadros de memória e o total de page faults (soma pgf+quad), pois o primeiro       preenchimento da memória também conta como uma falta de página para cada quadro.

- FIFO:<br>
  A função começa com uma lista vazia representando os quadros de memória, e um contador de faltas de página zerado. Depois      analisa cada número da sequência de páginas e, se o número não estiver na lista, ele já conta como uma falta de página. Em     seguida, se ainda tiver espaço na lista de quadros, a nova página é simplesmente adicionada ao final da lista. Se não tiver    mais espaço, ele remove a página do início da lista (a que entrou primeiro, ou "First-In") e adiciona a nova página no         final. Diferente dos outros, se o número já estiver na lista de quadros, nada acontece e o código passa para o próximo         número. No final, ele imprime o total de faltas de página e o estado final dos quadros de memória.



