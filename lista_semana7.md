# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.


______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'


______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?


D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".


______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:


D)

Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada. Saldo restante: 0

Compra 3 aprovada com limite de crédito. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

B) Preload -> Create -> Update

______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.

______

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)

```
Algoritmo podeVotar
Var
    int: idade
Inicio:
    idade <- Digite("Insira sua idade: )
    Se (idade < 16):
        Escreva("Não pode votar")
    Senão:
        Se (16 <= idade <18):
            Escreva("Voto facultativo!")
        Senão:
            Escreva("Voto obrigatório")
        FimSe
    FimSe
fimAlgoritmo
```
______

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.
    fimMetodo

    Método CalcularArea():
        - Defininr variável area
        - Atribuir um valor k vezes x para a variável area
    fimMetodo
FimClasse

Classe Retangulo estende FormaGeometrica:
    Atributos herdados:
        -cor
    Novos atributos:
        -base
        -altura

    Método CalcularArea():
        - Defininr variável area
        - Atribuir area = base vezes altura
        - Imprimir texto citando a forma geométrica (retângulo), sua cor e área
    fimMetodo
fimClasse

Classe Circulo estende FormaGeometrica:
    Atributos herdados:
        -cor
    Novos atributos:
        -raio

    Método CalcularArea():
        - Defininr variável area
        - Atribuir area = pi vezes raio ao quadrado
        - Imprimir texto citando a forma geométrica(círculo), sua cor e área
    fimMetodo
fimClasse

Definir novo objeto "retangulo1" 
Executar a funçao CalcularArea() utilizando o objeto "retangulo1"

Definir novo objeto "circulo1" 
Executar a funçao CalcularArea() utilizando o objeto "circulo1"


```

______

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

``` 
algoritmo desempenhoCarro
var
    real: tempo, distancia, velocidadei, aceleracao, velocidademax, tempomax, velocidade, velocidadefinal
inicio
    distancia <- distancia1
    velocidade <- velocidadei
    Se velocidadefinal < velocidademax ou tempo < tempomax:
        velocidadefinal <- velocidade ** 2 + 2 * aceleracao * distancia1 # Fórmula de Torricelli
        # distancia1 = velocidadei * tempo + (aceleracao * tempo ** 2) / 2
        # (aceleracao * tempo ** 2) / 2 + velocidadei * tempo - distancia1 == 0
        # Fórmula de Bhaskara:
        tempo = -velocidade1 + ((velocidade1) ** 2 - 4 * distancia1 * aceleracao / 2) ** (1/2)
    fimSe
FimAlgoritmo
```
    



______

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

```
Função MultiplicacaoDeMatrizes(matrizA, matrizB):
    # Verifica se o número de colunas da primeira matriz é igual ao número de linhas da segunda
    Se colunas(matrizA) ≠ linhas(matrizB) então:
        Retornar "As matrizes não podem ser somadas. A quantidade de colunas da primeira é diferente da quantidade de linhas da segunda."
    Senão:
        linhas <- tamanho(matrizA) # Na multiplicação de matrizes, a matriz resultado tem o número de linhas da primeira matriz
        colunas <- tamanho(matrizB[0]) # # Na multiplicação de matrizes, a matriz resultado tem o número de linhas da segunda matriz.
        matrizResultado <- novaMatriz(linhas, colunas)

        # Loop para percorrer cada elemento das matrizes e calcular a multiplicação
        Para i de 1 até linhas faça:
            Para j de 1 até colunas faça:
                C <- C matrizA[i][j] * matrizB[i][j]
            matrizResultado[i][j] <- C

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6]]
matrizB <- [[9, 8, 7], [6, 5, 4]]

matrizMultiplicação <- SomaDeMatrizes(matrizA, matrizB)
Escrever("Multiplicação das matrizes:")
ImprimirMatriz(matrizMultiplicação)
```