---
title: "O Efeito Dzhanibekov: Quando as rotações tornam-se imprevisíveis"
layout: post
tags: [rotação, clássica]
category: Mecânica Clássica
image:
  path: https://miro.medium.com/v2/resize:fit:1100/format:webp/1*s7hGZ0JTaUNh9dw_Z4jeng.gif
  alt: 
---

Imagine que você está no vácuo do espaço e solta uma chave de fenda para que ela gire livremente. Agora, de repente, sem aviso, ela dá uma cambalhota inesperada e muda de direção! Esse fenômeno intrigante é conhecido como **Efeito Dzhanibekov** e foi observado pela primeira vez em gravidade zero pelo cosmonauta Vladimir Dzhanibekov. Por mais que esse efeito não ocorra apenas em gravidade zero, ele é bastante conhecido por esse nome.

Esse efeito revela uma peculiaridade da dinâmica rotacional de corpos rígidos: um objeto sólido girando em torno de seu **Eixo Intermediário de Inércia** pode sofrer inversões repentinas e imprevisíveis. Mas por que isso acontece? E como essa instabilidade está conectada a conceitos profundos da mecânica clássica?

Antes de atacarmos o problema, precisamos realizar algumas revisões de conceitos fundamentais para compreender rotações de corpos rígidos.

## Revisão: Momento Angular

O $\textbf{momento angular}$ $\mathbf{L}$ é uma grandeza física fundamental na mecânica rotacional, representando a quantidade de movimento de rotação de um corpo em torno de um ponto ou eixo. Ele é definido como:

$$
\mathbf{L} = \mathbf{r} \times \mathbf{p}
$$

onde $\mathbf{r}$ é o vetor posição da partícula em relação ao ponto de referência e $\mathbf{p} = m\mathbf{v}$ é o momento linear da partícula.

Para um corpo rígido em rotação, o momento angular é dado por:

$$
\mathbf{L} = I \boldsymbol{\omega}
$$

onde $I$ é o momento de inércia e $\boldsymbol{\omega}$ é o vetor velocidade angular.

## Revisão: Momento de Inércia em rotações

O **Momento de Inércia** é uma grandeza física que quantifica a resistência de um corpo à variação de seu estado de rotação. Ele desempenha um papel semelhante ao da massa na segunda lei de Newton, mas aplicado ao movimento rotacional. Em termos matemáticos, para um sistema discreto de partículas, ele é definido como:

$$
I = \sum_{i} m_i r_i^2
$$

onde: $m_i$ é a massa de cada partícula do corpo e $r_{i}$ é a distância da partícula com relação ao eixo de rotação

Para um corpo contínuo, essa soma se transforma em uma integral:

$$
I = \int_C r^2 dm
$$

A unidade do momento de inércia no Sistema Internacional (SI) é o $\text{kg} \cdot \text{m}^2$.

O momento de inércia depende da distribuição de massa em relação ao eixo de rotação: quanto mais distante a massa está do eixo, maior o momento de inércia e maior será a dificuldade para alterar sua rotação.

### Matriz do Momento de Inércia

Quando um corpo rígido tem uma forma irregular, o Momento de Inércia depende da direção do eixo de rotação. Nesse caso, usamos a **Matriz do Momento de Inércia**, que relaciona o momento angular com a velocidade angular:

$$
\mathbf{L} = \mathbf{I} \boldsymbol{\omega}
$$

Em coordenadas, essa matriz é expressa como:

$$
\mathbf{I} =
\begin{bmatrix}
I_{xx} & I_{xy} & I_{xz} \\
I_{yx} & I_{yy} & I_{yz} \\
I_{zx} & I_{zy} & I_{zz}
\end{bmatrix}
$$

### Eixos Principais de Inércia

Sempre existem eixos em que a matriz do momento de inércia é diagonal, ou seja:

$$
\mathbf{I} =
\begin{bmatrix}
I_1 & 0 & 0 \\
0 & I_2 & 0 \\
0 & 0 & I_3
\end{bmatrix}
$$

Esses eixos são chamados de $\textbf{eixos principais de inércia}$ e correspondem aos autovetores da matriz $\mathbf{I}$. Os valores $( I_1, I_2, I_3)$ são os $\textbf{momentos principais de inércia}$. Em um sistema sem forças externas, a rotação ao longo desses eixos é estável.

## Agora sim, o Efeito Dzhanibekov!

Por causa da minha incapacidade em desenhar, vamos imaginar um objeto qualquer assimétrico (pode ser o seu celular: um bloco retangular). Sabendo que podemos diagonalizar a matriz momento de inércia, temos que o [[Momento Angular]] é:

$$
\vec{L} =
\begin{bmatrix}
I_1 & 0 & 0 \\
0 & I_2 & 0 \\
0 & 0 & I_3
\end{bmatrix} \vec{\omega}
$$

Onde $I_{3} > I_{2} > I_{1}$. Como $\vec{\omega}$ é um vetor de 3 componentes, podemos expandir a expressão acima da forma:

$$
\vec{L} = I_{1}\omega_{1}\hat{e}_{1} + I_{2}\omega_{2}\hat{e}_{2} + I_{3}\omega_{3}\hat{e}_{3} = I_{i}\omega_{i}\hat{e}_{i}
$$

Onde $\hat{e}_{i}$ são os vetores unitários dos eixos principais de rotação. Veja que estou usando a notação de Einstein para suprimir o símbolo de somatória para os índices com letras do alfabeto latino.
Como não existe torque externo, temos que $\frac{d \vec{L}}{dt} = \vec{0}$. Utilizando a regra do produto para derivadas, temos:

$$
\frac{d\vec{L}}{dt} = I_{i}(\dot{\omega}_{i}\hat{e}_{i} + \omega_{i}\dot{\hat{e}}_{i}) = \vec{0}
$$

Sabemos que $\frac{d\dot{\hat{e}}_{i}}{dt} = \vec{\omega} \times \hat{e_i}$. Esse resultado aparece quando analisamos um objeto em rotação a partir de um referencial inercial $S$ à uma distância $\vec{r}$ desse objeto e também de um referencial $S'$ no próprio objeto. Posso falar disso outra hora pois as contas para chegar no resultado são um pouco extensas e demandam bastante imagens para deixar a compreensão mais fácil.

Portanto,

$$
\dot{\vec{L}} = I_i(\dot{\omega_{i}} \hat{e}_{i} + \omega_{i}(\vec{\omega} \times \hat{e}_{i}){}) = \vec{0}
$$

Podemos reescrever o produto vetorial da forma a seguir pois $\vec{\omega} = \omega_{1}\hat{e_1} + \omega_{2}\hat{e_2} + \omega_{3}\hat{e_3}$.

$$
\dot{\vec{L}} = I_{i}(\dot{\omega}_{i}\hat{e}_{i} + \omega_{i}\omega_{j}(\hat{e}_{j}\times  \hat{e}_{i})) = \vec{0}
$$

Também podemos expandir o produto vetorial acima utilizando o tensor de Levi-Civita $\epsilon_{ijk}$. Com isso, a expressão toma a seguinte forma:

$$
\dot{\vec{L}} = I_{i}(\dot{\omega}_{i}\hat{e}_{i} + \omega_{i}\omega_{j}\epsilon_{jik}\hat{e}_{k}) = \vec{0}
$$

Chegamos finalmente à forma geral do momento angular desse sistema. Como sabemos que $i, j, k$ são números que vão de 1 a 3, vamos obter as expressões para cada valor de $i$:

$$
I_{1}(\dot{\omega}_{1}\hat{e}_{1} - \omega_{1}\omega_{2}\hat{e}_{3} + \omega_{1}\omega_{3}\hat{e}_{2}) = 0
$$

$$
I_{2}(\dot{\omega}_{2}\hat{e}_{2} + \omega_{2}\omega_{1}\hat{e}_{3} - \omega_{2}\omega_{3}\hat{e}_{1}) = 0
$$

$$
I_{3}(\dot{\omega}_{3}\hat{e}_{3} - \omega_{3}\omega_{!}\hat{e}_{2} + \omega_{2}\omega_{3}\hat{e}_{2}) = 0
$$

Somando as equações e isolando cada $\hat{e}_i$, obtemos as **Equações de Euler** que descrevem a rotação de um corpo rígido:

$$
I_{1}\dot{\omega}_{1} = \omega_{2}\omega_{3}(I_{2} - I_{3})
$$

$$
I_{2}\dot{\omega}_{2} = \omega_{3}\omega_{1}(I_{3} - I_{1})
$$

$$
I_{3}\dot{\omega}_{3} = \omega_{2}\omega_{1}(I_{1} - I_{2})
$$

## De onde surge esse comportamento?

Ao analisarmos cada equação, vemos que elas representam uma EDO. Para cada caso, quando consideramos $\dot{\omega}_{i} = 0$ isso indica que $\omega _i$ é uma constante e ao substituir os valores para os casos acima chegamos à uma EDO de 2ª ordem e que a solução é (semelhante ao movimento harmônico simples e assim a solução oscila sem perturbação.

Porém, isso não é verdade para todos os 3 casos que discutimos ($I_{1},  I_{2}, I_{3}$). Veja que, quando fazemos $\dot{\omega_2} = 0$ (rotação ao redor do eixo com momento de inércia intermediário $I_{2}$) a solução é uma exponencial que cresce com o passar do tempo, ou seja, qualquer pequena perturbação no estado inicial irá crescer exponencialmente. Para essa situação, vemos que a rotação ao redor do eixo intermediário **não é estável** e qualquer pequena perturbação faz o corpo inverter sua orientação de forma caótica.


