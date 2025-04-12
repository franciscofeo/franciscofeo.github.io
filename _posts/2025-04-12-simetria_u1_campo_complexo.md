---
title: "A Simetria Global U(1) no Campo Escalar Complexo"
layout: post
tags: [grupos, simetria, clássica, campos]
category: Teoria de Campos
image:
  path: https://www.polytechnique.edu/sites/default/files/styles/contenu_detail/public/content/actualites/images/2023-03/waves-g11da699b5_1920.jpg?itok=JRQvW3NW
  alt: 
---

Na teoria clássica de campos, a simetria desempenha um papel fundamental ao restringir e guiar a forma das leis físicas. Transformações simétricas — como rotações, translações ou transformações de gauge — revelam invariâncias que conduzem à conservação de quantidades físicas, como energia, momento e carga, por meio do teorema de Noether. Assim, a simetria não só simplifica a formulação das teorias, como também está intimamente ligada à estrutura e ao comportamento dos campos clássicos.

## Simetrias e Grupos

### Tipos de Simetrias

Quando estamos falando de simetrias no contexto de teoria de campos, temos 4 tipos:

- Simetrias Locais
- Simetrias Globais
- Simetrias Internas
- Simetrias de Espaço-Tempo

Na teoria de campos, as simetrias definem as leis físicas e moldam as interações. Simetrias globais mantêm os parâmetros constantes no espaço-tempo e estão ligadas a leis de conservação via o teorema de Noether. Simetrias locais, por outro lado, variam ponto a ponto e exigem a introdução de campos de gauge para preservar a invariância da teoria, como no caso do campo eletromagnético.

As simetrias internas afetam propriedades como carga ou isospin, enquanto as simetrias de espaço-tempo estão ligadas à conservação de energia e momento. As simetrias de gauge, que são locais e internas, fundamentam as interações do modelo padrão, determinando as forças fundamentais e os bósons correspondentes.

### O grupo $U(1)$

Teoria de grupos é um assunto bastante interessante e extenso. Sendo assim, vamos focar apenas em um grupo específico
sem entrar em detalhes técnicos como grupos e álgebras de Lie, geradores, etc. 

Grupos são estruturas abstratas que precisam respeitar certas propriedades: presença de associatividade, existência do elemento neutro e elemento inverso. A propriedade de comutatividade não é obrigatória, grupos que comutam são chamados de **Grupos Abelianos**.

Na física, a maioria dos grupos estudados 
são subgrupos de $GL(\mathbb{C}, n)$ (grupo linear complexo) e
têm seus elementos representados por matrizes, o $U(1)$ não é exceção. 
Esse grupo é chamado de **Grupo Unitário** que é definido como:

$$
  U(1) : \{ U \in GL(\mathbb{C}, n) \: | \: U^\dagger U = \mathbb{1}  \}
$$

ou seja, são matrizes $1 \times 1$ onde a expressão acima é cumprida.

Sem entrar em detalhes sobre Representações de Grupos, vamos entender como podemos escrever os elementos de $U(1)$ e aplicar isso à um vetor genérico.
Seja $v$ um vetor. Quando dizemos que esse vetor se transforma sob uma representação fundamental de $U(1)$ quer dizer que ele se torna:

\begin{equation}
    v' = e^{i\theta}v
\end{equation}

ou seja, ele ganha uma fase. Lembre-se que números complexos podem ser escritos na forma $z = re^{i\theta}$ (com $\theta \in \mathbb{R}$), nesse caso temos que $r = 1$.

## O campo escalar $\phi(x)$

Na Teoria Clássica de Campos, um campo escalar é uma entidade que associa um número a cada ponto do espaço-tempo, podendo ser real ou complexo. Um campo escalar real atribui um valor numérico real a cada ponto, como ocorre na descrição clássica de fenômenos como a temperatura em uma sala ou a densidade de massa em um fluido. Já um campo escalar complexo estende essa ideia ao permitir que esses valores sejam números complexos.

Sabemos que quando estamos falando de teoria de campos, o termo *densidade lagrangiana* é o correto já que estamos em um contexto
contínuo, porém, nesse trabalho o termo *lagrangiana* terá o mesmo significado e será usado mais vezes.

A lagrangiana mais simples de um campo escalar (complexo) é da forma:

\begin{equation}
    \mathcal{L} = \frac{1}{2}\partial_\mu \phi^\\dagger \partial^\mu \phi - m^2\phi^\\dagger \phi
\end{equation}

onde $\mu=0, 1, 2, 3$ e estamos no espaço-tempo de Minkowski com a métrica sendo $diag(-, +, +, +)$.

Existe uma forma mais geral de escrever a lagrangiana acima:

\begin{equation}
    \mathcal{L} = \frac{1}{2}\partial_\mu \phi^\\dagger \partial^\mu \phi - V(\phi^\\dagger \phi)
\end{equation}

onde $V(\phi, \phi^\\dagger)$ é o termo de potencial e pode tomar muitas formas, tendo um papel muito interessante
em simetrias sob o grupo $\mathbb{Z}_2$ e no processo de Quebra Espontânea de Simetria que não será abordado
aqui.

## Transformação do campo escalar sob $U(1)$


Como visto nas seções anteriores, aplicando $U(1)$ em $\phi$ e $\phi^\\dagger$ obtemos:

\begin{equation}
    \phi' = e^{i\theta}\phi
\end{equation}

e 

\begin{equation}
    (\phi^\\dagger)' = e^{i\theta}\phi^\\dagger
\end{equation}

Nesse caso, $\theta$ é uma constante pois ela não depende das coordenadas do espaço-tempo, ou seja, é uma transformação global.

A primeira questão que queremos responder à aplicar qualquer transformação no nosso campo é verificar
se isso deixa a lagrangiana invariante.

Assim, vamos estudar primeiramente o termo $V(\phi, \phi^\\dagger)$. Veja que, se mostrarmos que o produto de $\phi$ e $\phi^\\dagger$ é invariante, então
podemos afirmar que $V(\phi \phi^\\dagger)$ também é invariante. Por isso,

\begin{equation}
    \phi'(\phi^{\\dagger})' = (e^{i\theta}\phi)(e^{-i\theta}\phi^\\dagger)
\end{equation}

\begin{equation}
    \phi'(\phi^{\\dagger})' = (e^{i\theta} e^{-i\theta})\phi \phi^\\dagger = \phi \phi^\\dagger
\end{equation}

Mostramos que o termo de potencial é invariante. Vamos agora ao termo cinético que leva em consideração
as derivadas do campo.

\begin{equation}
    \partial_\mu (\phi^\\dagger)' \partial^\mu \phi' = \partial_\mu (e^{i\theta}\phi)\partial^\mu(e^{-i\theta}\phi^\\dagger)
\end{equation}

como estamos utilizando uma simetria global, $\theta$ não sofrerá influência das derivadas:

\begin{equation}
    \partial_\mu (\phi^\\dagger)' \partial^\mu \phi' = (e^{i\theta} e^{i\theta}) \partial_\mu \phi^\\dagger \partial^\mu \phi = \partial_\mu \phi^\\dagger \partial^\mu\phi
\end{equation}

E vemos que o termo cinético também é invariante.

Portanto, podemos concluir que o campo escalar complexo é invariante sob transformações de simetria global do grupo $U(1)$. Isso nos leva a alguns resultados bem interessantes
e com outras grandezas que são invariantes.

## A Corrente de Noether $j^\mu$


Dada uma função exponencial, sua expansão em Série de Taylor truncando em termos de 2ª Ordem é dada por:

\begin{equation}
    e^\alpha \approx \sum_{n=0}^{\infty} \frac{\alpha^n}{n!}
\end{equation}

Ignorando termos de ordem 2 para cima, temos que

\begin{equation}
    e^{i\theta} \approx 1 + i\theta
\end{equation}

Substituindo esse valor na transformação do campo $\phi$ e $\phi\dagger$:

\begin{equation}
    \phi' \approx \phi + i\theta\phi = \phi + i\delta\phi
\end{equation}

\begin{equation}
    (\phi^\dagger)' \approx \phi^\dagger + i\theta\phi^\dagger = \phi^\dagger + i\delta\phi^\dagger
\end{equation}

Antes de continuar, devemos ver como é a identidade de uma integração por partes
quando temos derivadas do tipo $\partial_\mu$.
Seja o produto de funções $\partial_\mu(A^\mu(x)B(x))$:

\begin{equation}
    \partial_\mu(A^\mu(x)B(x)) = (\partial_\mu A^\mu)B + A^\mu(\partial_\mu B)
\end{equation}

\begin{equation}
    A^\mu(\partial_\mu B) = \partial_\mu(A^\mu B) - (\partial_\mu A^\mu)B 
\end{equation}

Integrando ambos os lados em $V$, temos então a identidade de integração por partes para esse tipo de produto de funções com derivadas em $\mu$. Isso será útil nas próximas páginas.

Utilizando o Princípio Variacional, vamos analisar $\delta \mathcal{L}(\phi, \phi^\dagger, \partial_\mu \phi^\dagger, \partial^\mu \phi)$:

\begin{equation}
    \delta\mathcal{L} = \frac{\partial \mathcal{L}}{\partial \phi^\dagger}\delta\phi^\dagger + \frac{\partial\mathcal{L}}{\partial(\partial_\mu \phi^\dagger)}\delta(\partial_\mu \phi^\dagger) + \frac{\partial \mathcal{L}}{\partial \phi}\delta\phi + \frac{\partial \mathcal{L}}{\partial (\partial^\mu \phi)}\delta(\partial^\mu \phi)
\end{equation}

\begin{equation}
    \delta\mathcal{L} = \frac{\partial\mathcal{L}}{\partial\phi^\dagger}\delta\phi^\dagger + \frac{\partial\mathcal{L}}{\partial(\partial_\mu \phi^\dagger)}\partial_\mu(\delta \phi^\dagger) + \frac{\partial\mathcal{L}}{\partial\phi}\delta\phi + \frac{\partial\mathcal{L}}{\partial(\partial^\mu \phi)}\partial^\mu(\delta \phi)
\end{equation}

Os termos que possuem $\partial_\mu(\delta \phi^\dagger)$ e $\partial^\mu(\delta \phi)$ serão integrados por partes utilizando a identidade mostrada no começo da seção. Lembre-se que $\delta \mathcal{L}$ está dentro da integral da ação, dada por $\delta S = \int \delta \mathcal{L} d^4x$.
Com isso, na equação 16 vamos ter: $A^\mu = \frac{\mathcal{L}}{(\partial_\mu \phi^\dagger)}$ e $B = \delta \phi^\dagger$ e portanto, a variação da nossa lagrangiana se tornará:

\begin{equation}
    \delta\mathcal{L} = \left[ E. L. \right]\delta \phi^\dagger + \left[ E. L. \right]\delta \phi + \partial_\mu \left( \frac{\partial\mathcal{L}}{\partial(\partial_\mu \phi^\dagger)} \delta\phi^\dagger \right) + \partial^\mu \left( \frac{\partial\mathcal{L}}{\partial(\partial^\mu \phi)} \delta\phi \right)
\end{equation}

onde $E. L$ são as equações de Euler Lagrange.

Sabemos que as equações de Euler Lagrange vão para $0$ quando queremos que $\mathcal{L}$ seja invariante, porém, temos esses novos termos que darão o formato de $j^\mu$, chamado de **Corrente de Noether**. Lembrando que $\delta \mathcal{L}$ ser igual a $0$, não quer dizer estritamente que $\mathcal{L} = 0$, ela pode ser também uma derivada total, na forma $\partial_\mu \Sigma^\mu = \delta \mathcal{L}$, e por isso a forma mais geral da Corrente de Noether é dada por:

\begin{equation}
    j^\mu = \frac{\partial\mathcal{L}}{\partial(\partial^\mu \phi)} \delta\phi - \Sigma^\mu
\end{equation}

onde, $\Sigma^\mu = 0$ para simetrias internas e para simetrias de espaço-tempo teremos a presença do tensor energia-momento.

Realizando o cálculo da Corrente de Noether com a ajuda das expressões 13 e 14, temos que:

\begin{equation}
    j^\mu = i(\phi^\dagger \partial^\mu\phi - \phi \partial_\mu \phi^\dagger)
\end{equation}

Isso nos leva a ver que $j^\mu$ é uma grandeza conservada:

\begin{equation}
    \partial_\mu j^\mu = 0
\end{equation}

Uma corrente conservada, nos leva à existência de uma carga conservada e essa carga será o gerador dessa simetria. Nesse trabalho
não vamos entrar em detalhes disso mas no caso do campo escalar sob simetria $U(1)$ nós conseguimos chegar ao eletromagnetismo, o que deixa mais claro
o que seria essa carga e corrente.

Podemos encontrar a carga, $Q$, a partir da expressão abaixo:

\begin{equation}
    Q = \int d^3x j^0
\end{equation}

Para finalizar, podemos dizer que encontramos o Teorema de Noether que diz: *Toda simetria contínua de um sistema físico corresponde à uma corrente conservada*.