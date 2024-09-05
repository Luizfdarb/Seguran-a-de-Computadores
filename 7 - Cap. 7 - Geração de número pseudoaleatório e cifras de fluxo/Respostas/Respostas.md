**Nome completo:** Luiz Fellipe de Almeida Rodrigues Barbosa

## 1. Diferença entre Aleatoriedade Estatística e Imprevisibilidade

A **aleatoriedade estatística** se refere à capacidade de uma sequência parecer aleatória com base em testes estatísticos. Isso significa que, em termos de probabilidade, os elementos da sequência não têm padrões óbvios e exibem características de independência. No entanto, se essa sequência for gerada por um algoritmo, alguém que conheça o algoritmo e o ponto de partida pode prever os próximos números.

Por outro lado, **imprevisibilidade** implica que cada número na sequência é independente e não pode ser previsto, mesmo que o método de geração seja conhecido. Aqui, a imprevisibilidade é o fator-chave para garantir que a sequência seja verdadeiramente segura e resistente a qualquer tentativa de previsão.

## 2. Considerações de Projeto para uma Cifra de Fluxo

Ao projetar uma cifra de fluxo, algumas considerações são cruciais:

1. **Período longo da sequência de encriptação**: Como os números gerados não são verdadeiramente aleatórios, um longo período dificulta a criptoanálise, garantindo que o padrão não se repita facilmente.
  
2. **Semelhança ao fluxo de números verdadeiramente aleatórios**: A sequência deve se assemelhar ao máximo possível a um fluxo de números aleatórios verdadeiros. Isso significa que os bytes devem ter uma distribuição uniforme, tornando a criptoanálise mais difícil.

3. **Tamanho da chave de entrada**: Deve ser suficientemente grande para resistir a ataques de força bruta. Um tamanho adequado aumenta a segurança da cifra.

## 3. Perigos de Reutilizar uma Chave em Cifras de Fluxo

Reutilizar a mesma chave em uma cifra de fluxo pode ser extremamente perigoso. Se dois textos diferentes forem encriptados com a mesma chave, uma criptoanálise simples pode revelar o conteúdo de ambos. Quando os dois textos cifrados são submetidos a uma operação XOR, o resultado é o XOR dos textos claros originais, expondo assim informações sensíveis.

## 4. Operações Primitivas Utilizadas no RC4

O algoritmo RC4 utiliza três operações primitivas:

- **Módulo**: Para garantir que os valores permaneçam dentro de um intervalo específico.
- **Troca de bytes**: Para misturar os bytes no vetor de estado.
- **XOR**: Para combinar os bytes da chave com os bytes do texto claro, produzindo o texto cifrado.


## 5. Se apanharmos um algoritmo de congruência linear com um componente aditivo de 0:
<b>X<sub>n+1</sub> = (aX<sub>n</sub>) mod m</b>

<b>então, podemos mostrar que, se m é primo, e se determinado valor de a produz o período máximo de m − 1, então a<sup>k</sup> também produzirá o período máximo, desde que k seja menor que m e que m − 1 não seja divisível por k. Demonstre isso usando X<sub>0</sub> = 1 e m = 31, e produzindo as sequências para a<sup>k</sup> = 3, 3<sup>2</sup>, 3<sup>3</sup> e 3<sup>4</sup>.</b>

&nbsp;

Calcula o período de um gerador linearmente congruente:

```
def calcular_periodo_GLC(semente, multiplicador, modulo, constante):
    X_0 = semente  # Valor inicial
    sequencia = [X_0]
    
    # Gerando a sequência até encontrar um padrão repetido
    while True:
        x_anterior = sequencia[-1]
        proximo_x = ((multiplicador * x_anterior) + constante) % modulo
        if proximo_x in sequencia:
            periodo = len(sequencia) - sequencia.index(proximo_x)
            return periodo
        sequencia.append(proximo_x)
```

```
modulo = 31
semente = 1
constante = 0
```

```
print("Para m = {}, temos:".format(modulo))

exponentes = [1, 2, 3, 4]
for k in exponentes:
    a = 3 ** k
    resultado = calcular_periodo_GLC(semente, a, modulo, constante)
    print("O período para a = {} é: {}".format(a, resultado))
```

    Para m = 31, temos:
    O período para a = 3 é: 30
    O período para a = 9 é: 15
    O período para a = 27 é: 10
    O período para a = 81 é: 15


Temos que o a = 3 produz o período máximo m \- 1 = 31 \- 1 = 30.

&nbsp;

## 6. (a) Qual é o período máximo que pode ser obtido do seguinte gerador?
<b>X<sub>n+1</sub> = (aX<sub>n</sub>) mod 2<sup>4</sup></b>

&nbsp;

```
modulo = 16
semente = 1
constante = 0
```


```
print("Para m = {}, temos:".format(modulo))

for a in range(1, modulo):
    resultado = calcular_periodo_GLC(semente, a, modulo, constante)
    print("O período para a = {} é: {}".format(a, resultado))
```

    Para m = 16, temos:
    O período para a = 1 é: 1
    O período para a = 2 é: 1
    O período para a = 3 é: 4
    O período para a = 4 é: 1
    O período para a = 5 é: 4
    O período para a = 6 é: 1
    O período para a = 7 é: 2
    O período para a = 8 é: 1
    O período para a = 9 é: 2
    O período para a = 10 é: 1
    O período para a = 11 é: 4
    O período para a = 12 é: 1
    O período para a = 13 é: 4
    O período para a = 14 é: 1
    O período para a = 15 é: 2

De acordo com os testes realizados, variando a e também X<sub>0</sub>, temos que o período máximo é 4.

&nbsp;

**(b) Qual deverá ser o valor de a?**

Verificamos que os números que dão o maior período são 3, 5, 11 ou 13.

&nbsp;

**(c) Que restrições são exigidas na semente?**

Não ser um número no formato 2k, ou seja, ser ímpar. Visto que os testes mostraram que para obter o período máximo a semente não pode ser par.

&nbsp;

## 7. Que valor de chave RC4 deixará S inalterado durante a inicialização? Ou seja, após a permutação inicial de S, as entradas de S serão quais aos valores de 0 a 255 na ordem crescente.
Uma chave de tamanho 255 bytes, com o primeiro byte e o segundo sendo iguais a zero, e os restantes em ordem decrescente (de 255 a 2). Pois, de acordo com o algoritmo, teremos:

K[0] = 0, na primeira iteração.

K[1] = 0, na segunda iteração.

Para a terceira, temos k[2] = 255 e o processe segue até k[255].

k[3]=254;

k[4]=253;

k[5]=252;

...

k[255] = 2.

&nbsp;

## 8. O algoritmo Blum Blum Shub é baseado na teoria dos resíduos quadráticos e utiliza três números inteiros para realizar os cálculos: p, q e s.

**(a) Escolha dois números primos grandes p e q, onde p e q sejam congruentes a 3 mod 4 e não tenham fatores primos comuns. Por exemplo, você pode escolher p = 499 e q = 503.**

Analisando a tabela de primos até mil e verificando se o resto é igual a 3 quando dividido por 4, os números escolhidos foram p = 719 e q = 787.

&nbsp;

**(b) Calcule n = p ∗ q. Neste caso, n seria igual a 499 ∗ 503 = 250997.**

n = 719 \* 787 = 565.853.

&nbsp;

**(c) Escolha um número inteiro s entre 1 e n − 1 que seja co-primo com n. Por exemplo, você pode escolher s = 17.**

7, pois o MDC(565853, 7) = 1.

&nbsp;

**(d) Calcule o valor inicial x<sub>0</sub> = (s<sup>2</sup>) mod n. Neste caso, x<sub>0</sub> seria igual a (17<sup>2</sup>) mod 250997 = 289.**

x<sub>0</sub> = (s<sup>2</sup>) mod n = (7<sup>2</sup>) mod 565853 = 49 mod 565853 = 49.


&nbsp;

**(e) Agora, vamos gerar uma sequência de números aleatórios usando o algoritmo Blum Blum Shub. Para gerar cada número da sequência, use a seguinte fórmula: x<sub>i</sub> = (x<sup>2</sup><sub>i−1</sub>) mod n.**

x<sub>1</sub> = (x<sub>0</sub><sup>2</sup>) mod n = (49<sup>2</sup>) mod 565853 = 2401 mod 565853 = 2401.

x<sub>2</sub> = (x<sub>1</sub><sup>2</sup>) mod n = (2401<sup>2</sup>) mod 565853 = 5764801 mod 565853 = 106271.

&nbsp;

**(f) Execute a fórmula várias vezes para gerar uma sequência de números aleatórios. Por exemplo, você pode executar a fórmula 10 vezes para obter 10 números aleatórios.**

**Aqui está a sequência de números aleatórios gerados usando o algoritmo Blum Blum Shub com os valores do exemplo:**

**289, 253306, 14107, 23546, 67740, 144593, 79829, 46219, 132936, 9863**

**Qual foi a sua sequência?**

x<sub>0</sub> = (s<sup>2</sup>) mod n = (7<sup>2</sup>) mod 565853 = 49 mod 565853 = 49.

x<sub>1</sub> = (x<sub>0</sub><sup>2</sup>) mod n = (49<sup>2</sup>) mod 565853 = 2401 mod 565853 = 2401.

x<sub>2</sub> = (x<sub>1</sub><sup>2</sup>) mod n = (2401<sup>2</sup>) mod 565853 = 5764801 mod 565853 = 106271.

x<sub>3</sub> = (x<sub>2</sub><sup>2</sup>) mod n = (106271<sup>2</sup>) mod 565853 = 1129356794944 mod 565853 = 216600

x<sub>4</sub> = (x<sub>3</sub><sup>2</sup>) mod n = (216600<sup>2</sup>) mod 565853 = 46915560000 mod 565853 = 121917

x<sub>5</sub> = (x<sub>4</sub><sup>2</sup>) mod n = (121917<sup>2</sup>) mod 565853 = 14863754889 mod 565853 = 494138

x<sub>6</sub> = (x<sub>5</sub><sup>2</sup>) mod n = (494138<sup>2</sup>) mod 565853 = 244172363044 mod 565853 = 3308

x<sub>7</sub> = (x<sub>6</sub><sup>2</sup>) mod n = (3308<sup>2</sup>) mod 565853 = 10942864 mod 565853 = 191657

x<sub>8</sub> = (x<sub>7</sub><sup>2</sup>) mod n = (191657<sup>2</sup>) mod 565853 = 36732405649 mod 565853 = 58154

x<sub>9</sub> = (x<sub>8</sub><sup>2</sup>) mod n = (58154<sup>2</sup>) mod 565853 = 3381887716 mod 565853 = 350188

A sequência dos 10 primeiros foi:

49, 2401, 106271, 216600, 121917, 494138, 3308, 191657, 58154 e 350188.

&nbsp;

**Livro-texto da disciplina:** STALLINGS, William. Criptografia e segurança de redes. Princípios e práticas, Ed. 6. 2014
