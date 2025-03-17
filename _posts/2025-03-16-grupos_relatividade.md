---
title: Como Álgebra Abstrata, Geometria Hiperbólica e Relatividade se misturam?
layout: post
tags: [relatividade, simetria, grupos]
category: Teoria de Grupos
image:
  path: https://plenarinho.leg.br/wp-content/uploads/2019/05/destaque_einstein.jpg
  alt: 
---

Vamos explorar como a Teoria de Grupos se relaciona com a Teoria da Relatividade Especial de Einstein e que utilizando apenas Álgebra Linear conseguimos chegar na mesma estrutura das Transformações de Lorentz.


## Teoria de quê?

A **teoria de grupos** é uma área da Álgebra Abstrata que estuda conjuntos equipados com uma operação que "combina" elementos, seguindo regras bem definidas. Podemos pensar nela como o estudo das simetrias e transformações que mantêm uma estrutura inalterada.


Pela própria definição, um grupo $\mathbb{G}$ é basicamente um conjunto que possui uma operação comumente denotada por "$\cdot$" que relaciona dois elementos desse conjunto à um outro elemento desse conjunto $f: \mathbb{G} \times \mathbb{G} \rightarrow \mathbb{G}$ e que deve possuir algumas propriedades

- Associatividade

$$
a \cdot (b \cdot c) = (a \cdot b) \cdot c; \: \: \forall a,b,c \in \mathbb{G}
$$

- Existência de um elemento neutro

$$
a \cdot e = e \cdot a = a; \: \: \forall a\in \mathbb{G}
$$

- Existência de um elemento inverso

$$
a \cdot a^{-1} =  a^{-1} \cdot a = e; \: \: \forall a \in \mathbb{G}
$$

Estas propriedades derivam de outras estruturas chamadas de subgrupos e monóides, mas não vou entrar no mérito de explicar cada uma pois o objetivo aqui é apenas entender a definição de grupo.

Existe também uma outra propriedade chamada de comutatividade que não foi colocada acima pois ela não dita se um conjunto é ou não um grupo. Caso um grupo possua essa propriedade, nós chamamos de **Grupo Abeliano**.

## O Grupo Ortogonal Indefinido $O(p, q)$


O grupo $O(1, 1)$ é um tipo do grupo chamado "Grupo Ortogonal Indefinido" $O(p, q)$ que é dado por:

Seja $V= \mathbb{R}^{p+q}$ com $p,q \in \mathbb{N}_{0}$ e $\omega$ uma forma bilinear 
(por agora apenas aceite isso, no futuro posso explicar com mais detalhes o que são formas bilineares e sesquilineares) do tipo 
$\omega(x, y) = <x, \eta (p,q)y>_R$  onde $\eta$ é uma matriz diagonal com $p$ elementos $+1$ e $q$ elementos -1. 
Com isso, temos a definição geral do grupo $O(p, q)$:

$$
O(p,q) := \{ M\in \mathbb{GL}(p+q, \mathbb{R}), \: M^{-1} = \eta M^T\eta\}
$$

Tem uma infinidade de tópicos que podemos abordar apenas com a definição acima, como explorar os grupos ortogonais complexos ou o próprio grupo ortogonal $O(n)$. Mas o foco aqui é apenas o grupo $O(1, 1)$ que vai ser detalhado mais abaixo.

## Revisão das Transformações de Lorentz

As **transformações de Lorentz** são mudanças de coordenadas que preservam a **métrica de Minkowski** no espaço-tempo. No caso mais simples, com apenas uma dimensão espacial e uma temporal ( 2 dimensões), as coordenadas de um evento são dadas por um vetor:

$$
\vec{x} = \begin{pmatrix}
t \\
x
\end{pmatrix}
$$

A métrica para o espaço-tempo de Minkowski no caso bidimensional é:

$$
g_{\mu\nu} =\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
$$

Essas matrizes aparecerão na próxima seção. Mas para esse caso, realizando um boost nós vemos que as novas variáveis são transformadas da seguinte forma:

$$
t' = \gamma\left( t - \frac{v}{c^2}x \right)
$$

$$
x' = \gamma (x - vt)
$$

onde o fator de Lorentz $\gamma$ é dado por $\gamma = \frac{1}{\sqrt{ 1 - (\frac{v}{c})^2 }}$ .

## Voltando à Teoria de Grupos

Obviamente, para o grupo O(1, 1) a definição vista no primeiro tópico é válida. Portanto, vou economizar um pouco de latex e já seguir para as contas de verdade. Vamos calcular $\det(M^{-1})$:

$$
\det(M^{{-1}}) = \det(\eta) \det (M^T) \det(\eta)
$$

$$
\det(M^{-1}) = \det(\eta)^2\det(M^T)
$$

Lembrando das aulas de Álgebra Linear, sabemos que: caso a matriz $M$ admita uma inversa, então o determinante de $M^{-1}$ é igual ao inverso do determinante de $M$ e que $\det M = \det M^T$.  e que $\det(\eta) = 1$. Continuando:

$$
\frac{1}{\det M} = \det M 
$$

$$
\det M = \pm 1
$$

Veja que temos dois casos para o determinante, ele vale +1 ou -1. Vamos analisar o caso quando $\det M = +1$, esse é o chamado grupo $SO(1, 1)$ que é um subgrupo de $O(1, 1)$.
Lembrando que no grupo O(1, 1) temos matrizes $2 \times 2$, a propriedade $\eta M^T \eta$ é da forma:

$$
\eta M^T \eta =  \begin{pmatrix}
a & -c \\
-b & d  
\end{pmatrix} 
$$

e

$$
M^{-1} = \begin{pmatrix}
d & -b \\
-c & a 
\end{pmatrix}
$$

Assim,  temos que $d=a$ e $b=c$ deixando a matriz $M$ da forma:

$$
M = \begin{pmatrix}
a & b \\
b & a 
\end{pmatrix}
$$

E lembrando do determinante, temos a seguinte relação:

$$
a^2 - b^2 = 1
$$

Isso nos dá duas hipérboles tocando em -1 e +1 no eixo $x$ no plano cartesiano, e a hipérbole que está do lado "positivo" é considerada um subgrupo pois ela contém a matriz identidade quando $b=0$.
Chamei atenção para essa hipérbole na parte positiva propositalmente pois é ela que irá nos dar os resultados esperados sobre a relação com a Relatividade Especial. Para a parte positiva, podemos reescrever a matriz $M$ como:

$$
M = 
\begin{pmatrix}
\sqrt{ 1 + b^2 } & b \\
b & \sqrt{ 1 + b^2 }
\end{pmatrix}
$$

Como é de costume nessa etapa ao analisar as matrizes, podemos fazer $a = cosh z$ e $b=-sinhz$, deixando assim a nossa matriz como:

$$
M = \begin{pmatrix}
\cosh z & -senhz \\
-senhz & \cosh z 
\end{pmatrix}
$$

Após isso, podemos aprofundar nossa análise sobre como $SO(1, 1)$ é um Grupo de Lie (não precisa saber o que é isso por enquanto) e descobrir os seus geradores infinitesimais. Porém, vamos pular para a relação disso com a física.

Para quem já estudou as Transformações de Lorentz sobre uma perspectiva da geometria hiperbólica já conhece de cara a matriz acima, que é a matriz que faz o boost de Lorentz para um espaço-tempo bidimensional. Mas vamos abrir um pouco mais as contas para facilitar a visualização.

Fazendo: $tgh z = \frac{v}{c}$ e $z = arcTgh\left( \frac{v}{c} \right)$ e criando uma nova variável (pra quem já estudou um pouco de relatividade vai reconhecer esse carinha) $\gamma(v) = \frac{1}{\sqrt{ 1 - \left( \frac{v}{c} \right)^2 }}$ , nossa matriz $M$ ganha uma nova face:

$$
M(v) = \begin{pmatrix}
\gamma(v) & -\frac{v}{c}\gamma(v) \\
-\frac{v}{c}\gamma & \gamma(v) 
\end{pmatrix}
$$

Aplicando $M(v)$ em qualquer vetor, recuperamos as Transformações de Lorentz vista na seção anterior. 

Ou seja, o grupo $SO(1, 1)$ é exatamente o conjunto dessas matrizes de boosts hiperbólicos. Ele age como uma rotação no espaço-tempo de Minkowski e nos mostra mais uma vez que cada transformação de Lorentz é uma rotação hiperbólica que mantém a estrutura do espaço-tempo intacta.