## Agentes Lógicos

   <p align="justify">Agentes lógicos são descritos como um sistema que utiliza uma base de conhecimento atrelado a um conjunto de regras, em que ao ser alimentado por informações consegue inferir e deduzir informações a partir dos dados por eles obtidos, sendo capazes de realizar operações lógicas de primeira ordem, ou seja, consegue entender e representar problemas complexos.  É considerado um agente autônomo, toma decisões de forma lógica e racional, muito utilizado em sistemas com bases de informações incompletas, como em sistemas de detecção de falhas por exemplo</p>

### Agentes Baseados em conhecimento

 <p align="justify">É um agente lógico que é utilizado para resolver problemas epecíficos, com a base de dados em conhecimentos prévios, podendo ser utilizados também em conjunto de imagens. Um exemplo muito comum são sistemas médicos, que ao utilizar a base de dados de doenças e sintomas anteriores sugere a melhor metodologia a ser utilizado no paciente, assim como utilizar as imagens de ressonância magnética para detectar a uma possível doença.</p> 

### Lógica 

 <p align="justify">Á lógica nesse contexto, é o modo de como o agente estuda e irá atuar com seus problemas,  é utilizado lógica formal para fazer as representações das informações, sua aplicação e sua tomada de informações.</p> 

### Processo de Inferência
 <p align="justify">É um processo em que o agente lógico chega a conclusões por lógica a partir de um conjunto de informações, com as regras de inferência e seus conjuntos de premissas. Uma dessas premissas é a regra modus ponens, que é importante para permitir que os agentes lógicos tomem decisões  com base em informações limitadas.</p> 
 
 ### Agentes baseados em lógica proposicional
 
 <p align="justify">São programas feitos por computador que realizam ações e tomam decisões de acordo com sua avaliação lógica de afirmações e proposições. São pensados e projetados para processar a informação, entende-la de modo lógico, usando de processos de inferência e de base de fatos, que são conjuntos de informações conhecidas. Na lógica proposicional são muito utilizados em aplicações que exigem a tomada de decisões precisas , como sistemas de suporte à decisão e sistemas de gerenciamento de recursos. São capazes de processar informações de forma rápida e precisa, mas muitas vezes tende a ter dificuldades em lidar com informações imprecisas ou incertas.</p>
 
 Projetos e problemas
 
 <p align="justify">Um  exemplo ao qual pode ser aplicado é a implementação do jogo da velha para jogar contra um jogador humano ou outro agente. Ele verifica primeiro se há um movimento vencedor disponível e o faz. Caso contrário, ele verifica se o oponente tem um movimento vencedor e tenta bloqueá-lo. Se nenhuma dessas condições for atendida, ele escolhe um movimento aleatório. E pode ser visto no código abaixo:</p> 
 
 ```python
 
 import random

class TicTacToeAgent:
    def __init__(self, player):
        self.player = player
        self.knowledge_base = []

    def make_move(self, board):
        # Verifica se há um movimento vencedor
        for move in self.get_available_moves(board):
            if self.is_winning_move(board, move):
                return move

        # Verifica se o oponente tem um movimento vencedor e bloqueia
        for move in self.get_available_moves(board):
            if self.is_winning_move(board, move, self.get_opponent()):
                return move

        # Escolhe um movimento aleatório
        return random.choice(self.get_available_moves(board))

    def get_available_moves(self, board):
        return [i for i in range(9) if board[i] == ' ']

    def is_winning_move(self, board, move, player=None):
        if not player:
            player = self.player

        test_board = list(board)
        test_board[move] = player

        # Verifica linhas
        for i in range(3):
            if test_board[i*3] == test_board[i*3+1] == test_board[i*3+2] == player:
                return True

        # Verifica colunas
        for i in range(3):
            if test_board[i] == test_board[i+3] == test_board[i+6] == player:
                return True

        # Verifica diagonais
        if test_board[0] == test_board[4] == test_board[8] == player:
            return True
        if test_board[2] == test_board[4] == test_board[6] == player:
            return True

        return False

    def get_opponent(self):
        if self.player == 'X':
            return 'O'
        else:
            return 'X'
 
 
 
 ```
