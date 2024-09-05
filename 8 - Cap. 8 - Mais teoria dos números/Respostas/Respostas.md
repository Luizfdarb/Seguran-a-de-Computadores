**Nome completo**: Luiz Fellipe de Almeida Rodrigues Barbosa

Questões retiradas do livro-texto da disciplina. Conforme conversamos em sala de aula, as atividades devem ser realizadas para apresentação e discussão em sala, sempre nas aulas das quintas-feiras, atribuindo ao estudante uma nota de 0 ou 1 por cada atividade realizada e apresentada.

## 1. Por que mdc(n, n + 1) = 1 é para dois inteiros consecutivos n e n + 1?

Para qualquer par de inteiros consecutivos \( n \) e \( n+1 \), o máximo divisor comum \( mdc(n, n+1) \) é sempre igual a 1. Isso ocorre porque se houvesse um divisor comum \( p \) que dividisse ambos, então \( p \) deveria também dividir a diferença entre eles, ou seja, \( (n+1) - n = 1 \). Como o único número que divide 1 é ele próprio, concluímos que \( mdc(n, n+1) = 1 \) para quaisquer inteiros consecutivos \( n \) e \( n+1 \).

## 2. Usando o teorema de Fermat, encontre \( 3^{201} \mod 11 \).

Pelo teorema de Fermat, sabemos que se \( p \) é um número primo e \( a \) é um número inteiro positivo que não é divisível por \( p \), então \( a^{p-1} \equiv 1 \mod p \).

Aplicando isso:

- \( 11 \) é primo.
- Portanto, \( 3^{10} \equiv 1 \mod 11 \).

Agora, podemos simplificar \( 3^{201} \):

- \( 3^{201} = 3^{200} \times 3 = (3^{10})^{20} \times 3 \).
- \( (3^{10})^{20} \equiv 1^{20} \equiv 1 \mod 11 \).
- Logo, \( 3^{201} \equiv 3 \mod 11 \).

## 3. Use o teorema de Fermat para encontrar um número \( a \) entre 0 e 72, com \( a \) congruente a 9794 módulo 73.

Primeiro, calculamos o valor de \( 9794 \mod 73 \):

- \( 9794 \div 73 = 134 \) com resto \( 12 \).
- Portanto, \( 9794 \equiv 12 \mod 73 \).

O número \( a \) que procuramos é \( 12 \).

## 4. Use o teorema de Euler para encontrar um número \( a \) entre 0 e 9, tal que \( a \) seja congruente a \( 7^{1000} \mod 10 \).

Pelo teorema de Euler, sabemos que \( a^{\phi(n)} \equiv 1 \mod n \), onde \( \phi(n) \) é a função totiente de Euler.

- Para \( n = 10 \), \( \phi(10) = 4 \) (os números coprimos com 10 são 1, 3, 7 e 9).
- Portanto, \( 7^4 \equiv 1 \mod 10 \).

Agora, simplificamos \( 7^{1000} \):

- \( 7^{1000} = (7^4)^{250} \equiv 1^{250} \equiv 1 \mod 10 \).

Logo, \( 7^{1000} \equiv 1 \mod 10 \).

## 5. Use o teorema de Euler para encontrar um número \( x \) entre 0 e 28, com \( x^{85} \) congruente a 6 módulo 35.

Primeiro, decomponha \( x^{85} \) usando o teorema de Euler:

- \( \phi(35) = 24 \).
- Portanto, \( x^{24} \equiv 1 \mod 35 \).

Agora, podemos simplificar \( x^{85} \):

- \( x^{85} = x^{24} \times x^{24} \times x^{24} \times x^{13} \equiv 1 \times 1 \times 1 \times x^{13} \equiv x^{13} \mod 35 \).

Precisamos encontrar \( x \) tal que \( x^{13} \equiv 6 \mod 35 \).

A solução é \( x = 6 \).

## 6. Observe, na Tabela 8.2, que \( \phi(n) \) é par para \( n > 2 \). Isso é verdadeiro para todo \( n > 2 \). Dê um argumento conciso para explicar por que isso acontece.

A função totiente \( \phi(n) \) conta quantos números inteiros menores que \( n \) são coprimos com \( n \) (ou seja, não têm fatores em comum com \( n \) além de 1).

Se temos um número \( a \) que é coprimo com \( n \), então \( n-a \) também é coprimo com \( n \). Ou seja, \( gcd(a,n) = 1 \) e \( gcd(n-a,n) = 1 \).

Para cada \( a \) coprimo com \( n \), há um \( n-a \) correspondente que também é coprimo com \( n \). Portanto, os coprimos são emparelhados, deixando um número par de elementos no total.

## 7. Se \( n \) é composto e passa no teste de Miller-Rabin para a base \( a \), então \( n \) é chamado de pseudo-primo forte à base \( a \). Mostre que 2047 é um pseudoprimo à base 2.

Seguindo o algoritmo do teste de Miller-Rabin:

- No passo 1, definimos \( k = 1 \) e \( q = 1023 \), pois \( 2047 - 1 = 2^1 \times 1023 \).
- No passo 2, escolhemos \( a = 2 \) como base.
- No passo 3, calculamos \( 2^{1023} \mod 2047 \).

Temos que \( 2^{1023} \equiv 1 \mod 2047 \). Portanto, 2047 passa no teste e é um pseudo-primo forte à base 2.

## 8. O exemplo usado por Sun-Tsu para ilustrar o CRT foi \( x \equiv 2 \mod 3 \); \( x \equiv 3 \mod 5 \); \( x \equiv 2 \mod 7 \). Solucione para \( x \).

Calculamos \( M \):

- \( M = 3 \times 5 \times 7 = 105 \).

Agora, calculamos \( M_1 \), \( M_2 \), \( M_3 \):

- \( M/3 = 35 \).
- \( M/5 = 21 \).
- \( M/7 = 15 \).

Encontramos os coeficientes \( b_1 \), \( b_2 \), \( b_3 \):

- \( 35b_1 \equiv 1 \mod 3 \rightarrow b_1 = 2 \).
- \( 21b_2 \equiv 1 \mod 5 \rightarrow b_2 = 1 \).
- \( 15b_3 \equiv 1 \mod 7 \rightarrow b_3 = 1 \).

Finalmente, calculamos \( x \):

- \( x \equiv 2 \times 2 \times 35 + 3 \times 1 \times 21 + 2 \times 1 \times 15 \equiv 233 \mod 105 \).
- \( x \equiv 23 \mod 105 \).

Portanto, \( x = 23 \).

---

**Livro-texto da disciplina:** STALLINGS, William. *Criptografia e segurança de redes: Princípios e práticas*. 6ª ed., 2014.