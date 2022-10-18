# Cheatsheet
$$
% Macros para hacer más fácil todo
% Arma una derivada parcial
\newcommand{\pd}[2]{\frac{\partial#1}{\partial#2}}
% encloses the argument using stretchable parentheses
\newcommand{\pa}[1]{\left( #1 \right) } 
% encloses the argument using strechable brackets
\newcommand{\br}[1]{\left[ #1 \right] }
% encloses the argument using strechable curly brackets
\newcommand{\llave}[1]{\left\{#1\right\}}
% Define un vector dada una variable,  n
\newcommand{\avector}[2]{(#1_1,#1_2,\ldots,#1_{#2})}
% Real Numbers
\newcommand{\R}{\mathbb{R}}
% leftrightarrow shortcut
\newcommand{\LRA}{\leftrightarrow}
$$

> Recordar: Este documento requiere de los [[Macros para Latex]] para funcionar. Para usarlos, copiarlos al principio del documento (justo después del título). 
> Para más información, buscar en [[Template]]

## Sintáctico

#### Hace una lista punteada

- element
- element
	- element

#### Hace una lista ordenada

1. Primer Item
2.    Segundo Item
	1.   Tercer Item

#### Crea un bloque para citas

>Crea un apartado para escribir cosas interesantes.

#### Para incluir una tabla (y otros tips)
> Note: Inline math works in Typora

| 1               | 2         | 3              |
| --------------- | --------- | -------------- |
| **Bold**        | *italics* | ~~tachado~~    |
| ==highlighted== | `codigo`  | $$ Q.E.D \LRA ∎ $$ |
| 
## Matemática

### De los Macros:

#### Arma una derivada parcial

$$
\pd{x}{y}
$$

#### Paréntesis que funcionan bien

$$
\pa{a + b} \cdot \pa{a+c}
$$

#### Corchetes que funcionan bien

$$
\br{a + b} \cdot \br{a + c}
$$

#### Llaves que funcionan bien

$$
\llave{a + b} \cdot \llave{a + c}
$$

#### Define un vector dada una variable,  n

$$
\avector{u}{8}
$$

#### Numeros Relaes

$$
\R
$$

#### Leftrightarrow

$$
\LRA
$$

### Expresiones Comunes

#### Sistema de ecuaciones

$$
Q_{i}\pa{p_i}=
\left\{
\begin{array}{cl}
{Q\pa{p_{i}}} & {\text { if } p_{i}<p_{j}} \\
{\alpha_{i} Q\pa{p_{i}}} & {\text { if } p_{i}=p_{j}} \\
{0} & {\text { if } p_{i}>p_{j}}
\end{array}
\right.
$$

#### Optimización intertemporal

$$
\begin{align}
\max_{c_{t+s}, \  m_{t+s}} L : \ \sum_{s=0}^{\infty} \beta^{s} U\pa{c_{t+s}, m_{t+s}}+
&\lambda_{t+s}\br{x_{t+s} +m_t+s  + \pa{1+R_{t+s}} b_{t+s} \\
-\pa{1+\pi_{t+s+1}} b_{t+s+1}-\pa{1+\pi_{t+s+1}} m_{t+s+1}-c_{t+s}}
\end{align}
$$

#### Condiciones de primer orden

$$
\begin{align}
&\underline{\underline{CPO}}: \\
&\pd{L}{c_{t+s}} = 0 & \LRA &	\quad \beta^s U'_{c_{t+s}} -\lambda_{t+s} = 0 &	\quad (1)\\
&\pd{L}{m_{t+s}} = 0 & \LRA &	\quad \beta^s U'_{m_{t+s}} + \lambda_{ t+s} -\lambda_{t+s-1}\pa{1+\pi_{t+s}} = 0 &	\quad (2)\\
&\pd{L}{b_{t+s}} = 0 & \LRA &	\quad \lambda_{t+s}\pa{1+R_{t+s}} 
-\lambda_{t+s-1}\pa{1+\pi_{t+s}} = 0  &	\quad (3)\\

\end{align}
$$

#### Underbraces

$$
\underbrace{\pd{\pi_{2}}{K_{1}}}_\text{Total effect}= \underbrace{\pd{\pi_2}{K_1}}_\text{Direct effect}+ \underbrace{\pd{\pi_2}{\sigma_1^*}\pd{\sigma_1^*(K_1)}{K_1}}_\text{Strategic effect deterrance (SED)}
$$

#### Resolución de ecuaciones en tabla

$$
\begin{aligned}
p&=a-b\left(\frac{a-w}{2 b}\right) &\pi^r&=\left(p-w\right)Q\\
p &= a-\frac{a}{2}+\frac{w}{2} &\pi^r&=(\frac{a+w}{2}-w)\frac{a-w}{2 b}\\
p &=\frac{a+w}{2} & \pi^r&= \frac{a-w}{2 } \cdot \frac{a-w}{2b}\\
&& \pi^r&=\frac{(a-w)^2}{4 b}\\
\end{aligned}
$$

