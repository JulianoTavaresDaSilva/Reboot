# Operação REBOOT — registro da equipe

Equipe: AJ

Integrantes: Juliano e Alexandre 

## Missão 1 — Inventário
Previsão ANTES de executar (vetor final, tamanho, capacidade e deslocamentos): Previsão era para o vetor fazer seu delocamento mantendo os dados desejados sem perda de dados no inserir ou sem deixar dados de sobra na hora de remover. 

Resultado observado na versão inicial: O vetor perdeu seus dados na hora de inserir, pois o for estava indo em um sentido que atrapalhava na hora do deslocamento, e o remover estava deixando um valor duplicado no final do array, pois seu for não percorria ele até o fim.

Causa da falha e correção (explique; não basta colar o código): No método inserir invertemos o sentido do lopping para evitar perda de dados, e no método remover arrumamos no i < tamanho - 2 para i < tamanho - 1, assim faz o método chegar até o ultimo elemento.

Custo de inserir no início e no fim com espaço; por quê? O custo de inserir no inicio é O(n), pois precisa fazer o deslocamento dos valores que ja estavam no vetor para abrir espaço para o novo valor e o custo para inserir no fim com espaço é O(1), pois é só inserir na posição tamanho.

Quem programou / quem testou / quem explicou: Realizamos todas as etapas em conjunto.

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
Previsão ANTES de executar (turno, processo, executado, restante, fila): Privisão para o escalonador era para ele criar os objetos que seriam executados e ir retirando da fila os que acabassem e retornando eles, não interessando a ordem em que entrassem, mas sim na ordem em que os objetos iam terminando com suas durações.

Ordem de conclusão e tempo total:

Causa das falhas e correções: As falhas eram que a variavel restante e durações por serem objetos apontavam para o mesmo espaço da memoria, para corrigir usamos .clone() para apontar um espaço diferente e manter a variavel duração imutável. Outra falha era que a variável executado não se adaptava quando a duração era menor que o quantum, para corrigir isso fizemos um if que checa se o quatum foi maior que o restante a variavel executado recebe o valor de restante e não de quantum.  

Por que um processo volta ao fim? Por que preservar o array de entrada? O processo que não termina volta para o fim da fila para dar a vez a outro precesso e ser executado novamente quando chegar sua vez, e o array de entrada é preservado via .clone() para evitar que seus valores originais sejam zerados e estraguem outras partes do sistema que precisem desses dados intactos. 

Quem programou / quem testou / quem explicou: Realizamos todas as etapas em conjunto.

## Fechamento individual (cada integrante responde)
Nome: Juliano Tavares da Silva
1. Tamanho e capacidade são a mesma coisa? Não capacidade é a quantidade de elementos que um array suporta, e o tamanho é a quantidade de elementos que o array tem no momento.
2. A fila pode começar fisicamente no índice 2? Se for uma fila circular não vejo problema, mas se for uma fila normal pode forçar a implementar funções extras na fila para suportar esse inicio no indice 2. O ideal é começar no indice 0.
3. O primeiro processo a chegar precisa terminar primeiro? Não cada processo tem uma duração e é essa duração junto com o quantum que defini quem vai sair primeiro, sai primeiro o processo que executar a mesma quantidade de vezes que sua duração indica.
4. Qual conteúdo você precisa praticar mais? Fila Circular e Escalonador, tenho uma base, mas alguns pontos ainda me sinto travado, pricipalmente quando preciso usar um deque ou implementar uma fila Circular do zero.

## Desafio extra, se houver tempo
Novo cenário de teste, resultado esperado e qual erro ele detecta:
