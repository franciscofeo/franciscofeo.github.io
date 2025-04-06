---
title: "Spin em Quântica e Rotações na Mecânica Clássica: Isomorfismo entre Álgebras de Lie"
layout: post
tags: [grupos, simetria, quântica]
category: Teoria de Grupos
image:
  path: https://wallpapercave.com/wp/wp14227726.jpg
  alt: 
---

Estudar Grupos e Álgebras de Lie é fundamental na física teórica porque eles capturam a essência das simetrias contínuas que regem as leis da natureza. Desde a conservação de energia até a estrutura das interações fundamentais, todas estão enraizadas em simetrias expressas por esses objetos matemáticos. Grupos de Lie descrevem transformações contínuas como rotações e translações, enquanto suas álgebras associadas facilitam os cálculos infinitesimais dessas transformações. Na teoria quântica de campos, na relatividade e na física de partículas, as álgebras de Lie organizam os operadores que geram transformações, revelando as leis de conservação e a estrutura dos estados físicos possíveis.

Antes de partirmos para a verificação de fato do isomorfismo entre $\mathfrak{su}(2)$ e $\mathfrak{so}(3)$, vamos nos familiarizar com alguns conceitos. Vou deixar de forma bem introdutória pois cada um desses tópicos é bastante rico e complexo para ser explicado em uma publicação de um blog.

## O que são esses Grupos de Lie?

Em um post anterior eu expliquei um pouco sobre o que é essa estrutura abstrata chamada de Grupo, agora vamos nos aprofundar um pouco mais em um tópico específico.

No contexto da Teoria de Grupos, os **Grupos de Lie** surgem como uma ponte fascinante entre a álgebra e a geometria, desempenhando um papel essencial na física teórica, especialmente na formulação das simetrias contínuas que regem as leis da natureza. Para compreendê-los de forma intuitiva, podemos pensar neles como objetos matemáticos que combinam a estrutura de grupos com a fluidez das variedades diferenciáveis.

Isso significa que podemos aplicar ferramentas do cálculo diferencial para entender as transformações contínuas descritas por um grupo de Lie, o que é fundamental para estudar simetrias em sistemas físicos. Um exemplo clássico é o grupo das rotações no espaço tridimensional, $SO(3)$, que é um grupo de Lie — suas rotações formam um grupo, e esse grupo pode ser representado como uma variedade diferenciável tridimensional.

A estrutura de variedade permite que definamos objetos infinitesimais — como vetores tangentes — em torno do elemento identidade do grupo, o que nos leva naturalmente à definição da Álgebras de Lie associada. Esta álgebra captura a estrutura infinitesimal do grupo, revelando como pequenas transformações se comportam e interagem. Assim, enquanto o grupo de Lie descreve simetrias globais, sua álgebra de Lie associada nos dá acesso à estrutura local dessas simetrias — uma ferramenta indispensável, por exemplo, na mecânica quântica, relatividade e na teoria de gauge.

## Um pouco sobre Álgebras de Lie

Como introduzi acima, uma Álgebra de Lie associada à um grupo $G$ é definida como sendo o espaço tangente ao grupo no elemento neutro $e \in G$. Esse espaço tangente é um espaço vetorial que é munido de uma operação chamada de **Colchete de Lie** que, dado uma álgebra de Lie $\mathfrak{g}$, é definido como: 

$$
[\cdot \:, \cdot]: \mathfrak{g} \times \mathfrak{g}  \longrightarrow \mathfrak{g}
$$

O colchete de Lie deve satisfazer algumas propriedades:

1. Bilinearidade

$$
[ax + y, z] = a[x, z] + [y, z]
$$

$$
[x, ay + z] = a[x, y] + [x, y]
$$

2. Antissimetria

$$
[x, y] = -[y, x]
$$

3. Identidade de Jacobi

$$
[x, [y,z]] + [y, [z, x]] + [z, [x, y]] = 0
$$

Uma das formas para descobrirmos como é a Álgebra de Lie de determinado grupo de Lie é tomar a curva abaixo:

$$
g(t) = 1 + At + \mathcal{O}(t^2)
$$

onde $\mathcal{O}(t^2)$ são termos de ordem superior a $t$ e que geralmente desconsideramos pois $t$ toma valores muito pequenos.
Essa curva (para $t$ pequeno) representa os elementos do grupo $G$ próximos à identidade e é bastante útil pois $A$ é simplesmente um elemento da álgebra .

## Algumas propriedades dos grupos $SU(2)$ e $SO(3)$

Não entrarei em muitos detalhes mas o grupo $SU(2)$ é definido como

$$
SU(2): \{ M \in U(2) \: | \: \det M = 1 \}
$$

É chamado de grupo especial unitário, especial pois seu determinante é igual a 1 e unitário porque como ele é um subgrupo de $U(n)$, nós temos que $U^\dagger U = \mathbb{I}$. Onde as matrizes $U$ são complexas

Para o grupo $SO(3)$ temos um formato parecido porém as matrizes são reais:

$$
SO(3): \{ M \in O(3) \: | \: \det M = 1 \}
$$

e temos que $O^TO = \mathbb{I}$.

## A álgebra $\mathfrak{su}(2)$

Vamos verificar como é a estrutura das matrizes de $\mathfrak{su}(2)$:

$$
g(t) = 1 + At + \mathcal{O}(t^2)
$$

Pelas propriedades do grupo SU(2) temos que $U^{\dagger} = U ^{-1}$ e $\det U = 1$ para todo $U \in SU(2)$. Sendo assim, vamos usar a primeira propriedade:

$$
g(t)^{\dagger}g(t) = 1
$$

$$
(1 + A^{\dagger}t)(1 + At) = 1
$$

$$
1 + At + A^{\dagger}t + \mathcal{O}(t^2) = 1
$$

$$
(A + A^{\dagger})t = 0
$$

Isso tem que ser verdadeiro para qualquer valor de $t$, logo:

$$
A = -A^{\dagger}
$$

Vamos realizar um procedimento semelhante para a propriedade $\det U = 1$:

$$
\det (1 + At + \mathcal{O}(t^2)) = 1
$$

$$
1 + \det(At) = 1
$$

$$
t\det(A) = 0
$$

Lembrando da relação entre traço e determinante, temos que próximo à identidade o determinante de qualquer matriz é igual ao seu traço, então:

$$
Tr(A) = 0
$$

Portanto, vemos que á álgebra de Lie $\mathfrak{su}(2)$ é composta por matrizes $2 \times 2$ que são anti-hermitianas e possuem traço nulo:

$$
\mathfrak{su}(2): \{U \in Mat(\mathbb{C}, 2) \: | \: Tr(U) = 0, \: \:U = -U^{\dagger} \}
$$

Veja que as matrizes que satisfazem essas condições são as 3 matrizes de Pauli $\sigma_i$.
Realizando o cálculo de $[\sigma_{i}, \sigma_{j}]$ temos que o colchete de Lie no $\mathfrak{su}(2)$ tem a estrutura abaixo:

$$
[\sigma_{i}, \sigma _{j}] = 2i \epsilon_{ijk} \sigma _{k}
$$

## A álgebra $\mathfrak{so}(3)$

Vamos encontrar a estrutura da álgebra de Lie $\mathfrak{so}(3)$. Pelas propriedades do grupo SO(3) temos que $O^TO = \mathbb{1}$ e $\det O = 1$ para todo $O \in SO(3)$.
De forma semelhante ao que fizemos na álgebra $\mathfrak{su}(2)$ temos que:

$$
(1 + At + \mathcal{O}(t^2))^T(1 + At + \mathcal{O}(t^2)) = 1
$$

$$
1 + A^Tt + At  = 1
$$

$$
A = -A^T
$$

E por conta de $\det O = 1$ temos também que $Tr(A) = 0$.
Dessa forma, as matrizes de $\mathfrak{so}(3)$ são antissimétricas e possuem traço nulo:

$$
\mathfrak{so}(3): \{ O \in Mat(\mathbb{R}, 3) \: | \: Tr(O) = 0, \: O = -O^T\}
$$

Essas matrizes são nada mais nada menos que as matrizes de rotação $R_i$ geradoras de $SO(3)$.
O colchete de Lie para essa álgebra é dado pelo comutador das matrizes de rotação em $\mathbb{R}^3$ que pode ser generalizado por

$$
[R_{i}, R_{j}] = \epsilon_{ijk}R_{k}
$$

## Agora sim, o isomorfismo entre essas Álgebras de Lie

Vamos resumir tudo que vimos até agora.

Como sabemos, o grupo $SU(2)$ é um grupo de Lie que é composto por matrizes complexas $2 \times 2$ que é homeomorfo à esfera $\mathbb{S}^3$ onde a estrutura da matriz pode ser escrita da seguinte forma:

$$
U = \begin{pmatrix}
a && b \\
-\bar{b} && \bar{a}
\end{pmatrix} = \begin{pmatrix}
a + ib && c +id \\
-c + id && a -ib
\end{pmatrix}
$$

Veja que podemos reescrever a matriz acima como uma combinação de outras matrizes da seguinte forma:

$$
U = a \begin{pmatrix}
1 && 0 \\
0 && 1
\end{pmatrix} + ic \begin{pmatrix}
0 && -i \\
i && 0
\end{pmatrix} + id \begin{pmatrix}
0 && 1 \\
1 && 0
\end{pmatrix} + ib\begin{pmatrix}
1 && 0 \\
0 && -1
\end{pmatrix}
$$

Veja que as matrizes acima, exceto a primeira que obviamente é $\mathbb{1}$, são as matrizes de Pauli! Fazendo mais algumas contas nós conseguimos verificar que os geradores de $SU(2)$ são definidos como  $J = i\sigma_k$.
O colchete de Lie de $\mathfrak{su}(2)$ é $[\sigma_{i}, \sigma_{j}] = 2i\epsilon_{ijk}\sigma_{k}$.

Já o grupo $SO(3)$ é chamado de grupo de rotação em $\mathbb{R}^3$ onde são matrizes $3 \times 3$ tal que seus geradores $R_i$ são da forma:

$$
R_{1} = \begin{pmatrix}
0 && 0 && 0 \\
0 && 0 && -1  \\
1 && 0 && 0
\end{pmatrix}
$$

$$
R_{2} = \begin{pmatrix}
0 && 0 && -1 \\
0 && 0 && 0  \\
1 && 0 && 0
\end{pmatrix}
$$

$$
R_{3} = \begin{pmatrix}
0 && -1 && 0 \\
1 && 0 && 0  \\
0 && 0 && 0
\end{pmatrix}
$$

O colchete de Lie de $\mathfrak{so}(3)$ é $[R_{i}, R_{j}] = \epsilon_{ijk}R_{k}$

Observe que o formato do colchete de Lie de $\mathfrak{su}(2)$ e $\mathfrak{so}(3)$ é muito parecido, isso indica que essas duas álgebras podem ser isomorfas.

Mas certo, o que é um isomorfismo?

A função $f$ é um isomorfismo caso ela seja um homomorfismo inversível, lembrando que homomorfismo é uma operação que preserva a operação dos dois grupos. Assim, $f$ é isomorfismo se:

1. É linear
2. $f([a, b]) = [f(a), f(b)]$

Porém, antes de prosseguirmos precisamos fazer uma transformação no colchete de Lie de $\mathfrak{su}(2)$. Veja que podemos reescrever a expressão do colchete da seguinte forma:

$$
[J_{i}, J_{j}] = \epsilon_{ijk}J_{k}
$$

onde $J_{a} = -\frac{i}{2}\sigma_{a}$.
Sendo assim, veja que agora temos um mapeamento 1 para 1 desse colchete de Lie para o outro de $\mathfrak{so}(3)$. Então se fizermos a função linear mais simples possível:

$$
f: \mathfrak{su}(2) \longrightarrow \mathfrak{so}(3)
$$

$$
f(\sigma_{i}) = R_{i}
$$

Vamos demonstrar a condição 2:

$$
f([\sigma_{i}, \sigma_{j}]) = [R_{i}, R_{j}]
$$

$$
f(\epsilon_{ijk}\sigma_{k}) = \epsilon_{ijk}R_{k}
$$

$$
\epsilon_{ijk}f(\sigma_{k}) = \epsilon_{ijk}R_{k}
$$

Como definimos que $f(\sigma_{i}) = R_{i}$, então a condição é satisfeita e portanto $f$ é um isomorfismo.

Embora os grupos $SU(2)$ e $SO(3)$ não sejam isomorfos (assunto para outro post), suas álgebras compartilham exatamente a mesma estrutura. Isso significa que os geradores infinitesimais de ambos os grupos obedecem às mesmas relações de comutação. Essa equivalência matemática permite interpretar o spin quântico, descrito por $SU(2)$, como uma extensão natural das rotações clássicas tridimensionais descritas por $SO(3)$.