## Introdução

Como forma de realizar a representação de algorítimos de busca, esse texto busca abordar as representações atômicas e fatoradas de modo que demonstre suas abordagens e suas principais caractériticas. Sendo assim dependendo de qual abordagem será utilizado e quais as condições que foram declaradas, cabe-se escolher o melhor método e que melhor se encaixe de modo a resolver o problema, seja ele do tipo Nó, Arco, Trajeto, K e Globais e etc.


## Apresentação do conteúdo 

###	Representação atómica vs fatorada

Podemos dizer que na representação atómica estamos indo em um sentido, e buscando elementos que sejam idênticos sendo que os estados podem ser diferentes entre si,  já, na fatorada são diferentes e outras condições são avaliadas o que geram soluções mais ótimas em relação a  custos, até porque pode-se associar estados mesmo sendo diferentes.

### Definindo Problemas de Satisfação de Condições

Problemas de satisfação de condições, CSPs ou constraint notification problems,  são problemas matemáticos cujoo um conjunto de objetos em que os estados dos mesmos devem ter experimentado várias restrições. Sendo vistas como entidades, a CSPs representam  um conjunto homogêneo de restrições finitas sobre as variáveis do problema, que pode ser resolvida por métodos de restrição. Os CSPs são utilizados em Inteligência Artificial , uma vez em casos que a regularidade presente em sua formulação forneça uma base comum para análise e resolução de problemas de famílias não relacionadas, sendo de alta complexidade e custosos experimentados e onde também são utilizados métodos heurísticos e de busca combinatória para que possam resolver tais problemas em tempo aceitável. 

Esse tipo de problema tira vantagem da estrutura de estados e usam heurísticas específicas de domínio para permitir a solução de problemas complexos,  a ideia principal é eliminar as grandes porções do espaço de busca de uma vez só, identificando combinações de variáveis que violam as condições. Desta forma, as CSPs representam  um conjunto homogêneo de restrições finitas sobre a variável do problema, e tal problema é resolvido por métodos de restrição  por algoritmos de busca que tem a vantagem de usar heurísticas específicas de domínio, e com isso solucionando problemas complexos, com atribuições consistentes, e sem violar nenhuma condição imposta.

Tipos de condições
 Existem quatro condições: 

• Unitária: Condição no qual possui apenas uma única variável; 
• Binária: Condição no qual possui apenas duas variáveis; 
• Ternária: Condição no qual possui apenas três variáveis; 
• Global ou N-´arias: Condição no qual possui quantidade arbitrária de variáveis. 

 Classificadas como:
 
• Absolutas: Condições no qual no podem ser violadas; 
• Preferenciais: Condições que devem ser satisfeitas quando possível. 

Consistências  
As consistências são do tipo:
•	Nó; 
•	Arco; 
•	Trajeto 
•	K; 
•	Globais. 

Consistência de nós
É dito nó consistente se nenhum valor de seu domínio viola uma restrição unária envolvendo a variável. É possível remover todas as restrições unárias de um grafo de restrições, removendo as restrições do domínio, então para que no grafo o nó seja consistente se todas as variáveis do grafo ou todos os nós devem consistentes.
Consistência de arcos
Pode-se dizer que uma rede é arco consistente se todos os seus arcos são arco consistentes, em que é obtida por sucessivas eliminações de valores inconsistentes, assim quando se elimina um valor, outros podem se tornar inconsistentes e podem ser eliminados também, assim sendo como uma onda que propaga, tendo as escolhas mais restritas até encontrar a solução.
A consistência de trajeto
A consistência de trajeto, está relacionada com o uso de condições implícitas, que são modeladas por triplas variáveis, isso quer dizer que para que o trajeto seja consistente precisa-se de uma nova condição.
