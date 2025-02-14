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

<h2>Complexidade temporal</h2>

Em ciência da computação, a complexidade temporal de um algoritmo descreve como o tempo de execução desse algoritmo cresce em função do tamanho da entrada. Em outras palavras, ela nos diz como o tempo que um algoritmo leva para executar varia conforme aumentamos a quantidade de dados que ele precisa processar.

<h3>Por que a complexidade temporal é importante?</h3>

Ao escolher um algoritmo para resolver um problema, é fundamental considerar sua complexidade temporal. Isso nos permite prever o desempenho do algoritmo para entradas de tamanhos diferentes e comparar a eficiência de diferentes algoritmos para a mesma tarefa.

<h3>Como medir a complexidade temporal?</h3>

A complexidade temporal é geralmente expressa usando a notação Big O, que descreve o limite superior do crescimento do tempo de execução. A notação Big O ignora constantes multiplicativas e termos de ordem inferior, focando apenas no termo dominante que determina o comportamento assintótico do algoritmo.

Exemplos de complexidade temporal:
<ul>
  <li>O(1): Complexidade constante. O tempo de execução não depende do tamanho da entrada.</li>
  <li>O(log n): Complexidade logarítmica. O tempo de execução cresce logaritmicamente com o tamanho da entrada.</li>
  <li>O(n): Complexidade linear. O tempo de execução cresce linearmente com o tamanho da entrada.</li>
  <li>O(n log n): Complexidade linearítmica. O tempo de execução cresce proporcionalmente a n vezes o logaritmo de n.</li>
  <li>O(n²): Complexidade quadrática. O tempo de execução cresce quadraticamente com o tamanho da entrada.</li>
  <li>O(2^n): Complexidade exponencial. O tempo de execução cresce exponencialmente com o tamanho da entrada.</li>
</ul>

<h3>Como determinar a complexidade temporal de um algoritmo?</h3>
Para determinar a complexidade temporal de um algoritmo, é preciso analisar seu código e identificar as operações que são executadas repetidamente em função do tamanho da entrada. Em seguida, contamos o número de vezes que essas operações são executadas e expressamos esse número em termos de n, o tamanho da entrada.

<h3>Exemplo:</h3>
<h3>Considere o seguinte algoritmo para encontrar o maior elemento em um array:</h3>

function encontrarMaior(array) {
  let maior = array[0];
  for (let i = 1; i < array.length; i++) {
    if (array[i] > maior) {
      maior = array[i];
    }
  }
  return maior;
}

Esse algoritmo percorre o array uma vez, comparando cada elemento com o maior elemento encontrado até o momento. O número de comparações é proporcional ao tamanho do array, portanto, a complexidade temporal desse algoritmo é O(n).

<h3>Conclusão:</h3>
A complexidade temporal é uma ferramenta essencial para avaliar a eficiência de algoritmos e escolher o mais adequado para um determinado problema. Ao entender como o tempo de execução de um algoritmo varia com o tamanho da entrada, podemos tomar decisões mais informadas e otimizar o desempenho de nossos programas.

<h2>Em termos de notação Big O, a frase "podemos remover quaisquer constantes multiplicativas quando temos uma complexidade de tempo" significa que, ao analisar a eficiência de um algoritmo, podemos ignorar os fatores constantes que multiplicam a função que descreve o tempo de execução.</h2>

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

Vamos analisar as duas funções para entender suas complexidades de tempo:

Função bar(num):

def bar(num):
  if(num <= 1):
    return 1
  else:
    bar(num-1)
    
Ocorrências da função: A função bar(num) é chamada recursivamente com um argumento decrescido em 1 (num-1) até que num seja menor ou igual a 1.
Número de chamadas: Para um valor inicial de num, a função bar será chamada num vezes.

Complexidade de tempo: Como o número de chamadas da função cresce linearmente com o valor de num, a complexidade de tempo da função bar é O(n), onde n é o valor inicial de num.

Função dib(num):

def dib(num):
  if (num <= 1):
    return 1
  else:
    dib(num -1)
    dib(num -1)
    
Ocorrências da função: A função dib(num) faz duas chamadas recursivas para dib(num-1).

Número de chamadas:

Para dib(1): 1 chamada

Para dib(2): 1 chamada inicial + 2 chamadas de dib(1) = 3 chamadas

Para dib(3): 1 chamada inicial + 2 chamadas de dib(2) = 1 + 2 * 3 = 7 chamadas

Para dib(4): 1 chamada inicial + 2 chamadas de dib(3) = 1 + 2 * 7 = 15 chamadas

Padrão: O número de chamadas cresce exponencialmente com num. Especificamente, o número de chamadas é 2^num - 1.

Complexidade de tempo: Como o número de chamadas da função cresce exponencialmente com o valor de num, a complexidade de tempo da função dib é O(2^n), onde n é o valor inicial de num. No entanto, como a questão menciona O(n²), pode haver um erro na função fornecida ou na expectativa de complexidade. Se a intenção fosse ter O(n²), a função deveria ter uma estrutura diferente, como dois loops aninhados.
Em resumo:

A função bar(num) tem complexidade de tempo O(n) porque o número de chamadas recursivas cresce linearmente com num.
A função dib(num) tem complexidade de tempo O(2^n) (e não O(n²)) porque o número de chamadas recursivas cresce exponencialmente com num devido às duas chamadas recursivas.

<h3>Exemplo:</h3>
def dib(num):
  if (num <= 1):
    return 1
  else:
    dib(num -1)
    dib(num -1)

Neste código a complexidade de tempo é O(2²), já a complexidade de espaço é
Para fazer a análise da complexidade de espaço pegamnos um cenário da raiz a base e vemos quantos quadros de pilhas temos na pilha de chamadas então removemos os quadros até retornamos em um que terá outro quadro sobrando pós ele.

Sabemos que o número de quadros de pilha que usaremos é realmente apenas a altura da árvore. Então a altura da árvore é n como dissemos antes, significa que nossa profundidade máxima de pilha também é n.
Então temos no espaço a complexidade vinda da pilha de chamadas.


<h2>Vamos analisar a complexidade de espaço da função dib(num):</h2>
def dib(num):
  if (num <= 1):
    return 1
  else:
    dib(num -1)
    dib(num -1)
Entendendo a complexidade de espaço

A complexidade de espaço de um algoritmo se refere à quantidade de memória que ele utiliza durante sua execução, em função do tamanho da entrada.  Estamos interessados em como a quantidade de memória adicional cresce conforme o tamanho da entrada aumenta.

Análise da função dib(num)

Recursão: A função dib(num) é recursiva, ou seja, ela chama a si mesma.  Cada chamada recursiva adiciona uma nova "camada" à pilha de execução (ou call stack).

Pilha de execução: A pilha de execução armazena informações sobre as funções que estão sendo executadas, incluindo suas variáveis locais e o ponto de retorno. Cada chamada recursiva de dib(num) ocupa espaço na pilha.

Profundidade da recursão: A profundidade da recursão é determinada pelo valor inicial de num.  A cada chamada, num é decrementado em 1. A recursão para quando num chega a 1. Logo, a profundidade máxima da recursão é num.

Espaço utilizado: Cada chamada de dib(num) ocupa um espaço constante na pilha de execução para armazenar as informações da função (variáveis locais, etc.). Como a profundidade máxima da recursão é num, o espaço total utilizado na pilha será proporcional a num.

Conclusão

A complexidade de espaço da função dib(num) é O(n), onde n é o valor inicial de num. Isso significa que a quantidade de memória utilizada pela função cresce linearmente com o tamanho da entrada.

Exemplo:

dib(1): A profundidade da recursão é 1. Espaço utilizado: constante * 1.
dib(5): A profundidade da recursão é 5. Espaço utilizado: constante * 5.
dib(100): A profundidade da recursão é 100. Espaço utilizado: constante * 100.
Perceba que, embora a função faça duas chamadas recursivas dentro do else, a profundidade da pilha é determinada pela maior cadeia de chamadas aninhadas, não pela quantidade de chamadas em um nível específico.  É por isso que a complexidade é O(n) e não O(2^n).  O número total de chamadas é exponencial, mas o espaço usado na pilha é linear porque as chamadas ocorrem sequencialmente, não simultaneamente. Uma vez que uma ramificação da recursão termina, seu espaço na pilha é liberado.

<h2>Exemplo de complexidade de espaço O(n²)</h2>
Um exemplo clássico de complexidade de espaço O(n²) é a criação de uma matriz quadrada de tamanho n x n.

Código em Python:

def criar_matriz(n):
  """Cria uma matriz quadrada de tamanho n x n com valores iniciais 0."""
  matriz = []
  for i in range(n):
    linha = []
    for j in range(n):
      linha.append(0)
    matriz.append(linha)
  return matriz

# Exemplo de uso:
tamanho = 5
matriz_5x5 = criar_matriz(tamanho)

# Imprime a matriz (opcional)
for linha in matriz_5x5:
  print(linha)
Explicação da complexidade O(n²):

Estrutura de dados: A função criar_matriz(n) cria uma matriz, que é uma estrutura de dados bidimensional. No caso de uma matriz quadrada, tanto o número de linhas quanto o número de colunas são iguais a n.

Alocação de memória: Para armazenar essa matriz, é necessário alocar espaço para n linhas, e cada linha contém n elementos. Portanto, o número total de elementos na matriz é n * n = n².

Crescimento da memória: Conforme o valor de n (tamanho da matriz) aumenta, a quantidade de memória necessária para armazenar a matriz cresce quadraticamente. Por exemplo:

Se n = 2, a matriz terá 4 elementos (2x2).
Se n = 10, a matriz terá 100 elementos (10x10).
Se n = 100, a matriz terá 10.000 elementos (100x100).
Complexidade de espaço: Como a quantidade de memória utilizada pela matriz cresce proporcionalmente a n², dizemos que a complexidade de espaço da função criar_matriz(n) é O(n²).

Observação:

É importante distinguir complexidade de tempo de complexidade de espaço. Neste exemplo, a criação da matriz envolve dois loops aninhados, o que poderia levar à conclusão de que a complexidade de tempo também é O(n²). No entanto, estamos analisando a quantidade de memória utilizada, não o tempo de execução.

Outros exemplos de complexidade de espaço O(n²):

Matrizes: Qualquer algoritmo que crie e manipule matrizes quadradas de tamanho n terá complexidade de espaço O(n²).
Tabelas: Estruturas de dados que armazenam informações em formato de tabela, com n linhas e n colunas, também terão complexidade de espaço O(n²).
Importância da complexidade de espaço:

A complexidade de espaço é um fator importante a ser considerado ao escolher um algoritmo, especialmente quando se lida com grandes conjuntos de dados. Se a complexidade de espaço for muito alta, o algoritmo pode exigir uma quantidade excessiva de memória, o que pode levar a problemas de desempenho ou até mesmo impedir a execução do programa em sistemas com recursos limitados.

<h2>Caso em que a notação Big O é O(1):</h2>
def somar_elementos(lista):
  soma = 0  # Espaço constante O(1)
  for elemento in lista:  # Itera sobre a lista, sem alocar espaço adicional
    soma += elemento
  return soma
Nesse caso, a complexidade de espaço é O(1), pois a quantidade de memória utilizada (variável soma) não depende do tamanho da lista de entrada.


<h2>Sobnre o exemplo do fib() no vídeo:</h2>
Analisando apenas a complexidade do tempo, podemos dizer que a complexidade do fib, está em algum lugar entre a função dib() e a função lib(). Isso significa que a complexidade do tempo da função fib() é O(2^n,)

<h2>O que implica a complexidade do tempo ser O(2^n) </h2> 
Significa que em certos casos repetimos os valores nas subárvores fazendo assim com que seja possível reutilizar certos cálculos.

Programação dinâmica será qualquer instância onde temos um problema maior, neste caso, Fibonacci. E podemos decompô-lo em instâncias menores do mesmo problema, também temos uma estrutura sobreposta.
Devemos buscar qual padrão na árvore é duplicado.
Então iremos usar um padrão de programação chamado memorização, a memorização é na verdade uma das estratégias que podemos usar para resolver problemas de programação dinâmica 
Com amemorização procuramos armazenar alguns subproblemas duplicados. Dessa forma, podemos só pegar os resultados mais tarde.

<h2>Complexidade de Memória: Fibonacci com e sem Memorização</h2>
A diferença na complexidade de memória entre um algoritmo de Fibonacci com e sem memorização reside na forma como cada abordagem lida com os cálculos repetidos.

Fibonacci sem Memorização
Recursão Pura: A implementação clássica e recursiva do Fibonacci recalcula os mesmos valores várias vezes.
Complexidade Exponencial: A árvore de recursão cresce exponencialmente, resultando em muitas chamadas redundantes.
Memória Limitada: A memória utilizada é determinada pela profundidade da pilha de chamadas recursivas, que é proporcional a n.
Ineficiência: Para números grandes de n, o algoritmo se torna extremamente lento e pode levar a um estouro de pilha.
Fibonacci com Memorização
Armazenamento de Resultados: A técnica de memorização armazena os resultados dos cálculos em um dicionário ou tabela hash.
Reutilização: Antes de calcular um valor, o algoritmo verifica se ele já foi calculado e, em caso afirmativo, reutiliza o resultado armazenado.
Complexidade Linear: Cada valor de Fibonacci é calculado apenas uma vez.
Memória Adicional: Requer memória adicional para armazenar os resultados, resultando em uma complexidade de espaço O(n).
Eficiência Aprimorada: O algoritmo se torna muito mais rápido, pois evita cálculos repetidos.
Comparação
Característica	Fibonacci sem Memorização	Fibonacci com Memorização
Abordagem	Recursão pura	Programação dinâmica (Top-down)
Cálculos	Repetidos	Únicos
Complexidade de Tempo	Exponencial O(2^n)	Linear O(n)
Complexidade de Espaço	Logarítmica O(log n)	Linear O(n)
Eficiência	Baixa	Alta

Exportar para as Planilhas
Observações
A memorização oferece um compromisso entre tempo e espaço.
A escolha entre as abordagens depende dos requisitos do problema e dos recursos disponíveis.
Para valores de n muito grandes, a memorização é essencial para evitar cálculos repetidos e tornar o algoritmo viável.
Em resumo, a memorização transforma um algoritmo de Fibonacci com complexidade de tempo exponencial em um com complexidade linear, resultando em um uso mais eficiente dos recursos computacionais.
