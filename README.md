# Trabalho de Sistemas Distribuídos - 2019 - 2

Projeto visa desenvolver métodos e conhecimento na implementação de um sistema distríbuído.

# Be'ngo!

A idéia é implementar um jogo de bingo em que 4 clients consigam acompanhar os "sorteios" em tempo real até que um dos
jogadores termine sua "cartela".

# Funcionamento:

Logo que o servidor inicia, o mesmo aguardará até que os 4 clients sejam conectados na sala, assim que houver a
confirmação do número de jogadores necessários para iniciar, cada um dos jogadores receberá uma sequência de 10 números (de 1 a 50)
aleatoriamente, assim serão definidas as "cartelas" a serem preenchidas de cada jogador. Quando o jogo iniciar, começarão as rodadas
de sorteio, em cada rodada, um número (de 1 a 50) será sorteado, e cada jogador receberá uma mensagem com sua marcação na rodada 
(se um de seus números foi sorteado ou não) e seu status (quantos de seus números já foram sorteados, e quantos faltam para ganhar
o jogo). Em determinado momento, um dos jogadores terá toda sua cartela preenchida, e o jogo será encerrado, com uma mensagem
de vitória no client vencedor, e derrota, para os demais.

# Componentes: 

1 servidor, 4 clientes e seus terminais.

# Teste de recuperação de falhas: 

-O jogo sempre inicia com 4 jogadores, porém, é possível que a comunicação de um desses jogadores
falhe no meio da partida, quando ocorrer, espera-se que consigamos prosseguir com a partida com um jogador a menos.

-Também é possível existir uma falha que derrube o servidor, nesse caso, conforme orientado, é necessário que o jogo possa voltar
a ser jogado no status que foi pausado.

Demonstração de funcionalidades: É necessário que possamos jogar o be'ngo, e que em algum momento um dos jogadores tenha todos
os seus números sorteados, mesmo que, após falhas, somente ele esteja na sala.

Teste de concorrência: É necessário que todos os jogadores tenham uma visão única dos números que estão sendo sorteados, pois,
somente o primeiro jogador a preencher sua cartela deve ganhar a partida 

