# dynamic-programming
Estudando programação dinamica com o curso "Dynamic Programming- Learn to Solve Algorithmic Problems &amp; Coding Challenges" do freeCodeCamp.org]


<h2>O que é uma função arbitraria:</h2>
Em programação, uma função arbitrária, também conhecida como função de ordem superior ou higher-order function, é uma função que pode receber outras funções como argumentos e/ou retornar funções como resultado. Essa capacidade confere às funções arbitrárias um poder expressivo e flexibilidade significativos, permitindo a criação de código mais modular, reutilizável e abstrato.
</br>
<h3>Características principais:</h3>
Receber funções como argumentos: Uma função arbitrária pode aceitar outras funções como entrada, o que possibilita a personalização do seu comportamento. Essa característica é útil para implementar padrões de projeto como strategy ou template method, nos quais o algoritmo geral é definido, mas etapas específicas são delegadas a funções externas.

Retornar funções como resultado: Uma função arbitrária também pode gerar novas funções como saída. Essa funcionalidade é valiosa para criar fábricas de funções ou para implementar currying, técnica que transforma uma função que recebe múltiplos argumentos em uma sequência de funções que recebem um argumento cada.

<h2>O que é um caso base em programação:</h2>
Em programação, um caso base é a condição de parada de uma função recursiva.

<h3>Função recursiva</h3>

Uma função recursiva é aquela que chama a si mesma dentro de sua própria definição. Em outras palavras, a função resolve um problema dividindo-o em subproblemas menores e mais simples, até que um desses subproblemas seja tão simples que possa ser resolvido diretamente. Esse caso mais simples é o caso base.

Caso base
O caso base é a condição que define quando a recursão deve parar. Sem um caso base, a função recursiva continuaria se chamando infinitamente, levando a um erro de estouro de pilha (stack overflow).
Exemplo:
A função abaixo calcula o fatorial de um número inteiro positivo:
def fatorial(n):
  if n == 0:  # Caso base: fatorial de 0 é 1
    return 1
  else:
    return n * fatorial(n-1)  # Chamada recursiva

</br>
Nesse exemplo, o caso base é n == 0. Quando a função fatorial é chamada com o argumento 0, ela retorna 1, encerrando a recursão. Caso contrário, a função chama a si mesma com um argumento menor (n-1) até que o caso base seja atingido.

</br>

<h3>Importância do caso base</h3>
O caso base é fundamental para garantir que a recursão termine em algum momento e que a função não entre em um loop infinito. É importante definir o caso base de forma clara e garantir que ele seja atingido em todas as chamadas recursivas.

</br>

Observação:
É possível ter múltiplos casos base em uma função recursiva, cada um correspondendo a uma condição de parada diferente.


<h2>Complexidade Espacial</h2>
Em programação, a complexidade espacial de um algoritmo descreve a quantidade de memória que ele utiliza para executar suas tarefas, em função do tamanho da entrada. Em outras palavras, ela avalia o espaço adicional de memória que um algoritmo necessita, além do espaço ocupado pelos dados de entrada.

</br>

Como medir a complexidade espacial?
</br>
A complexidade espacial é geralmente expressa usando a notação assintótica Big O, que descreve o crescimento da demanda de memória em relação ao aumento do tamanho da entrada. Por exemplo:
<ul>
  <li>O(1): Complexidade espacial constante. O algoritmo utiliza uma quantidade fixa de memória, independentemente do tamanho da entrada.</li>
  <li>O(n): Complexidade espacial linear. A quantidade de memória utilizada cresce linearmente com o tamanho da entrada.</li>
  <li>O(n²): Complexidade espacial quadrática. A quantidade de memória utilizada cresce quadraticamente com o tamanho da entrada.</li>
  <li>O(log n): Complexidade espacial logarítmica. A quantidade de memória utilizada cresce logaritmicamente com o tamanho da entrada.</li>
</ul>

Fatores que influenciam a complexidade espacial:
<ul>
  <li>Variáveis: O número e o tipo de variáveis utilizadas no algoritmo afetam a complexidade espacial.</li>
  <li>Estruturas de dados: O uso de estruturas de dados como arrays, listas ou árvores pode influenciar a quantidade de memória necessária.</li>
  <li>Recursão: Algoritmos recursivos podem ter uma complexidade espacial maior devido à necessidade de armazenar informações sobre as chamadas recursivas na pilha de execução.</li>
</ul>

<h3>Importância da complexidade espacial:</h3>
<ul>
  <li>Otimização de recursos: Ao analisar a complexidade espacial, é possível otimizar o uso de memória do algoritmo, o que é especialmente importante em ambientes com recursos limitados.</li>
  <li>Desempenho: Em alguns casos, a complexidade espacial pode afetar o desempenho do algoritmo, pois o acesso à memória pode ser mais lento do que outras operações.</li>
  <li>Escalabilidade: Ao lidar com grandes conjuntos de dados, a complexidade espacial pode ser um fator determinante na capacidade do algoritmo de lidar com eles de forma eficiente.</li>
</ul>

Exemplo:
</br>
Considere um algoritmo que recebe um array de números inteiros como entrada e retorna a soma de todos os elementos. A complexidade espacial desse algoritmo é O(1), pois ele utiliza apenas algumas variáveis ​​adicionais para armazenar a soma e o índice do array, independentemente do tamanho da entrada.

</br>

Observação:
A complexidade espacial é apenas um dos aspectos a serem considerados ao analisar a eficiência de um algoritmo. A complexidade de tempo, que descreve o tempo de execução do algoritmo, também é importante.
</br>
Em termos de notação Big O, a frase "podemos remover quaisquer constantes multiplicativas quando temos uma complexidade de tempo" significa que, ao analisar a eficiência de um algoritmo, podemos ignorar os fatores constantes que multiplicam a função que descreve o tempo de execução.

</br>

Para entender melhor, vamos analisar um exemplo:
</br>
Suponha que um algoritmo leve 2n + 5 passos para ser executado, onde n é o tamanho da entrada. A notação Big O foca em como o tempo de execução cresce em relação ao tamanho da entrada, ignorando os termos que não afetam o crescimento.
</br>
O termo 2n cresce linearmente com n.
</br>
O termo 5 é uma constante e não se altera com o aumento de n.
</br>
Na notação Big O, desprezamos as constantes multiplicativas (2, no caso) e os termos de menor ordem (5, no caso). Portanto, a complexidade de tempo desse algoritmo é O(n), indicando um crescimento linear em relação ao tamanho da entrada.
</br>

<h3>Por que ignoramos as constantes multiplicativas?</h3>
</br>
A notação Big O descreve o limite assintótico superior do tempo de execução de um algoritmo. Em outras palavras, ela nos diz como o tempo de execução cresce à medida que o tamanho da entrada se torna muito grande.
</br>
Quando n é muito grande, as constantes multiplicativas se tornam irrelevantes em comparação com o termo dominante. Por exemplo, se n = 1 bilhão, 2n será muito maior que 5, e a diferença entre 2n e 100n será relativamente pequena.
</br>

<h3>Em resumo:</h3>
A notação Big O simplifica a análise da complexidade de tempo, permitindo que nos concentremos no fator de crescimento dominante. Ao remover as constantes multiplicativas, podemos comparar algoritmos de forma mais clara e identificar qual deles terá um desempenho melhor para entradas grandes.
Em análise de algoritmos, O(n) tempo e O(n) espaço são duas formas de expressar a complexidade de um algoritmo, que se referem, respectivamente, ao tempo de execução e à quantidade de memória que um algoritmo utiliza em função do tamanho da entrada (n).
</br>

<h3>O(n) tempo (Complexidade de tempo linear):</h3>

Significa que o tempo de execução de um algoritmo cresce linearmente com o tamanho da entrada.
</br>
Se o tamanho da entrada dobra, o tempo de execução também dobra (aproximadamente).
</br>
Geralmente, algoritmos que percorrem todos os elementos de uma estrutura de dados (como um array ou uma lista) têm complexidade de tempo O(n).
</br>

Exemplo:
</br>
def encontrar_maior(lista):
    maior = lista[0]  # O(1)
    for elemento in lista:  # O(n)
        if elemento > maior:
            maior = elemento  # O(1)
    return maior  # O(1)
</br>
Nesse exemplo, a função encontrar_maior percorre a lista uma vez para encontrar o maior elemento. O tempo de execução é dominado pelo loop for, que é executado n vezes, onde n é o tamanho da lista. Portanto, a complexidade de tempo é O(n).

<h3>O(n) espaço (Complexidade de espaço linear):</h3>

Significa que a quantidade de memória utilizada por um algoritmo cresce linearmente com o tamanho da entrada.
</br>
Se o tamanho da entrada dobra, a quantidade de memória utilizada também dobra (aproximadamente).
</br>
Geralmente, algoritmos que criam uma nova estrutura de dados com tamanho proporcional à entrada têm complexidade de espaço O(n).
</br>

Exemplo:
</br>
def copiar_lista(lista):
    nova_lista = []  # O(1)
    for elemento in lista:  # O(n)
        nova_lista.append(elemento)  # O(1)
    return nova_lista  # O(1)
Nesse exemplo, a função copiar_lista cria uma nova lista com os mesmos elementos da lista original. O tamanho da nova lista é proporcional ao tamanho da lista original. Portanto, a complexidade de espaço é O(n).

<h3>Observações:</h3>

A complexidade de tempo e espaço são importantes para avaliar a eficiência de um algoritmo, especialmente quando lidamos com grandes conjuntos de dados.

É possível ter algoritmos com diferentes combinações de complexidade de tempo e espaço (por exemplo, O(n) tempo e O(1) espaço, ou O(n²) tempo e O(n) espaço).

Ao escolher um algoritmo, é importante considerar tanto a complexidade de tempo quanto a de espaço, levando em conta os recursos disponíveis e os requisitos do problema.

Espero que esta explicação detalhada tenha sido útil! Se tiver mais perguntas, sinta-se à vontade para perguntar.


<h3>Complexidade temporal</h3>
