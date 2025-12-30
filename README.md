# Puzzle_casas
Codigo para responder o puzzle das casas

Vide arquivo puzzle_tabuleiro_menos_1.ipynb

Em cada casa de um tabuleiro 5×5 está escrito 1 ou -1. Em cada passo, troca-se o número de cada uma das 25 casas pelo resultado da multiplicação dos números de suas casas vizinhas (são vizinhas se tiverem um lado em comum).

Posição inicial:

[[ 1 1 -1 1 1]
[ 1 1 1 1 1]
[ 1 1 1 1 1]
[ 1 1 1 1 1]
[ 1 1 1 1 1]]


Como fica o tabuleiro ao final de 2026 passos?

Resposta.

A forma mais simples de resolver é fazer algumas iterações, até chegar em algum ponto em que o padrão se repete.

Uma determinada posição vai sempre resultar no passo seguinte igual, porque as regras são determinísticas. E sempre vai chegar num momento em que o padrão vai se repetir, porque há um número finito de padrões possíveis.

Dá para fazer com lápis e papel, mas é mais bonito e preciso fazer com um computador. Vide código no Github.

Após a primeira iteração:


Após a segunda:


Segue um gif animado com algumas dessas iterações.


A partir da iteração 4, o padrão começa a se repetir, e com período 4.

2026 é da forma 4*x + 2, então vai coincidir exatamente com a iteração 6. Ou seja, vai resultar no padrão:


Em formato matricial:

[[ 1. 1. -1. 1. 1.]
[ 1. 1. 1. 1. 1.]
[ 1. 1. -1. 1. 1.]
[ 1. 1. 1. 1. 1.]
[-1. 1. 1. 1. -1.]]

Puzzle inspirado na Revista Eureka! n. 20
