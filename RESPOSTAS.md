# Operação REBOOT — registro da equipe

Equipe:
Integrantes:

## Missão 1 — Inventário
Previsão ANTES de executar (vetor final, tamanho, capacidade e deslocamentos): Previsão era para o vetor fazer seu delocamento mantendo os dados desejados sem perda de dados no inserir ou sem deixar dados de sobra na hora de remover. 

Resultado observado na versão inicial: O vetor perdeu seus dados na hora de inserir, pois o for estava indo em um sentido que atrapalhava na hora do deslocamento, e o remover estava deixando um valor duplicado no final do array, pois seu for não percorria ele até o fim.

Causa da falha e correção (explique; não basta colar o código): No método inserir invertemos o sentido do lopping para evitar perda de dados, e no método remover arrumamos no i < tamanho - 2 para i < tamanho - 1, assim faz o método chegar até o ultimo elemento.

Custo de inserir no início e no fim com espaço; por quê? Custo é O(n), pois tem que fazer o deslocamento dos valores do array.

Quem programou / quem testou / quem explicou: Ambos os membros

## Missão 2 — Fila circular
Previsão ANTES de executar (posições físicas, início, fim, tamanho e ordem lógica):
Previsão antes de executar é que dê errado, porque o método cheia() está errado, e a fila "CIRCULAR" está incompleta sem o % dados.lenght 

Resultado observado:
De fato falhou e não loopou porque estava incompleta

Causa da falha e correção:
Causa da falha: falta de % dados.lenght que pega o módulo e faz a base da fila circular funcionar

Como distinguir cheia de vazia? Como obter O(1) nas operações?
Obtemos O(1) nas operações através do resto da divisão do fim e do inicio + 1.

Quem programou / quem testou / quem explicou: Ambos os membros

## Missão 3 — Escalonador
Previsão ANTES de executar (turno, processo, executado, restante, fila):

Ordem de conclusão e tempo total:

Causa das falhas e correções: valor de executados deve se adaptar ao quanto resta de duração para cada objeto.

Por que um processo volta ao fim? Por que preservar o array de entrada?

Quem programou / quem testou / quem explicou: Ambos os membros

## Fechamento individual (cada integrante responde)
Nome:
1. Tamanho e capacidade são a mesma coisa?
2. A fila pode começar fisicamente no índice 2?
3. O primeiro processo a chegar precisa terminar primeiro?
4. Qual conteúdo você precisa praticar mais?

## Desafio extra, se houver tempo
Novo cenário de teste, resultado esperado e qual erro ele detecta:
