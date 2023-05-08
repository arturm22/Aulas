## Resolvendo problemas por busca

  Com o intuito de solucinar problemas, é necessário defini-los com precisão de uma forma que se permita descrever e encaixar os problemas em algorítmos de busca de uso geral.  

### Agente de solução de problemas

  <p align="justify">O objetivo de um algorítmo de busca é maximizar seu desempenho, que além dos dados também pode adotar metas a esses algoritimos, também se busca um menor uso de memória e velocidade de resposta do agente.</p>
  <p align="justify">Para problemas de busca, representações atômicas são mais comumente utilizadas visto que consideram os objetivos e ações futuras comparando com os resultados desejáveis. Essa estrutura adota um ou mais objetivos que treinam seu comportamento para ajudar limitar seus resultados assim como suas ações dentro do problema. Quando o ambiente é desconhecido o agente fará ações de modo aleatório, com várias ações e com vários valores para eventualmente alcançar o resultado esperado.</p>




Os Agente de soluções de problemas são baseados em objetivos e consideram ações
futuras e o quanto seus resultados são desejáveis. Eles utilizam representações
atômicas, onde não há estrutura interna visível para os algoritmos de resolução de
problemas e os estados são considerados como um todo.
Na formulação de objetivo os agentes adotam um ou mais objetivos que ajudam a
organizar o comportamento, limitando o que o agente está tentando alcançar e as ações a
considerar.
A tarefa do agente é descobrir como agir agora e no futuro para alcançar seus objetivos. A
formulação de problemas decide que ações e estados devem ser considerados, dado
um objetivo.
O agente precisa de informações para executar suas ações. Se o ambiente for
desconhecido ele terá que fazer ações de forma aleatória. Um agente com várias opções
imediatas de valor desconhecido pode decidir o que fazer examinando primeiro ações
futuras que levam eventualmente a estados de valor conhecido.

Agentes inteligentes devem maximizar sua medida de desempenho. Como mencionamos
no Capítulo 2, alcançar isso às vezes é simplificado se o agente puder adotar uma meta e visar
satisfazendo-o. Vejamos primeiro por que e como um agente pode fazer isso.
