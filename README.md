# As Transformações de Lorentz e a Lei de Adição de Velocidades

Luana M. Souza

*Seções 1.9 e 1.10 de Bernard Schutz: finalmente escrevendo a "receita" completa que transforma coordenadas de O para O̅, e o que acontece quando velocidades se somam*

> **Antes de começar:** esta é a continuação de [Hipérboles Invariantes](https://github.com/m0rang0azul/hiperboles--invariantes), que por sua vez usa resultados de [Invariância do Intervalo](https://github.com/m0rang0azul/invariancia-do-intervalo) e [Geometria do Espaço-Tempo](https://github.com/m0rang0azul/Relatividade-Geral---Diagrama-de-Minkowski). Nos posts anteriores, usamos a transformação de Lorentz sem deduzi-la (chamando-a de "Eq. 1.12" e tomando-a como dada), discutimos também a [Dilatação do Tempo e a Contração do Comprimento](https://github.com/m0rang0azul/Dilatacao-no-Tempo--Contracao-no-Comprimento). Agora, fechamos essa lacuna: vamos deduzir essas equações do zero, usando só o que já provamos até aqui.

---

## 1. Configuração e premissas iniciais

Para simplificar, consideramos apenas movimento ao longo do eixo $x$: o referencial $\bar O$ se move com velocidade constante $v$ (em unidades com $c=1$) na direção $x$ positiva de $O$. Partimos de três hipóteses que já usamos antes, nesta série:

:clock4: **Origens coincidentes:** $t=\bar t=0$ ocorre no mesmo evento que $x=\bar x=y=\bar y=z=\bar z=0$.

:clock10: **Invariância transversal:** como não há movimento relativo nas direções $y$ e $z$, as distâncias perpendiculares ao movimento não mudam (é o resultado que já tínhamos provado no post sobre invariância do intervalo, com a barra perpendicular): $\bar y = y,\ \bar z = z$.

:clock11: **Linearidade:** a transformação entre referenciais inerciais precisa ser linear (mesma hipótese da Seção 1.6), para que uma partícula livre continue se movendo em linha reta e com velocidade constante em qualquer referencial. Escrevemos a forma mais geral possível:

$$\bar t = \alpha\ t + \beta\ x \qquad \text{e} \qquad \bar x = \kappa\ t + \sigma\ x$$

onde $\alpha, \beta, \kappa, \sigma$ são coeficientes que só podem depender da velocidade relativa $v$.

> **Nota de notação:** usamos $\kappa$ (kappa) aqui, e não $\gamma$, de propósito. A letra $\gamma$ está reservada, nesta série, para o fator de Lorentz $\gamma = 1/\sqrt{1-v^2}$, que vai aparecer mais adiante. Misturar os dois símbolos é um erro de notação fácil de cometer, então vale a pena manter essa distinção clara desde o início.

---

## 2. Passo 1: a geometria dos eixos já nos dá duas equações

A boa notícia é que já fizemos boa parte do trabalho geométrico nos posts anteriores. Lembra da Seção 4 de [Geometria do Espaço-Tempo](../relogio-de-luz)? Lá descobrimos a inclinação dos dois eixos de $\bar O$ no papel de $O$:

:clock9: **O eixo $\bar t$** (a reta $\bar x = 0$) é a linha de universo da própria origem de $\bar O$, que se desloca com velocidade $v$ no referencial de $O$: $x = vt$.

:clock9: **O eixo $\bar x$** (a reta $\bar t = 0$) é o "agora" de $\bar O$, com inclinação recíproca: $t = vx$.

Vamos usar essas duas retas para fixar dois dos quatro coeficientes.

**Eixo $\bar t$:** substituindo $\bar x = 0$ na equação $\bar x = \kappa t + \sigma x$:

$$0 = \kappa t + \sigma x \quad\Longrightarrow\quad x = -\frac{\kappa}{\sigma} t$$

Comparando com $x=vt$, temos $-\kappa/\sigma = v$, ou seja:

$$\kappa = -v\sigma$$

**Eixo $\bar x$:** substituindo $\bar t = 0$ na equação $\bar t = \alpha t + \beta x$:

$$0 = \alpha t + \beta x \quad\Longrightarrow\quad t = -\frac{\beta}{\alpha} x$$

Comparando com $t=vx$, temos $-\beta/\alpha = v$, ou seja:

$$\beta = -v\alpha$$

Substituindo $\beta = -v\alpha$  e  $\kappa = -v\sigma$ de volta nas equações originais, a transformação já fica bem mais enxuta:

$$
\bar{t} = \alpha(t - vx) \quad \text{e} \quad \bar{x} = \sigma(x - vt) \quad \text{(i)}
$$

Dois coeficientes a menos, faltam só $\alpha$ e $\sigma$.

---

## 3. Passo 2: a simetria da luz força $\alpha = \sigma$

Para o próximo passo, usamos o segundo postulado de Einstein: a luz viaja à velocidade 1 em **qualquer** referencial inercial. Considere um raio de luz na direção $+x$, cuja linha de universo satisfaz $x=t$ no referencial de $O$. Pelo postulado, o mesmo raio precisa satisfazer $\bar x = \bar t$ no referencial de $\bar O$.

Substituindo $x=t$ nas Eqs. (i):

$$\bar t = \alpha(t - vt) = \alpha t\(1-v) \qquad \text{e} \qquad \bar x = \sigma(t - vt) = \sigma t\(1-v)$$

Para que $\bar x = \bar t$ (a luz continua andando a 45° no diagrama de $\bar O$), precisamos de:

$$\sigma t\(1-v) = \alpha t\(1-v) \quad\Longrightarrow\quad \boxed{\alpha = \sigma}$$

(desde que $v\ne 1$ e $t\ne 0$, o que é sempre o caso para observadores físicos). Essa é a mesma simetria que já tínhamos usado implicitamente lá no primeiro post, quando o fóton disparado em $\bar t=-a$ atinge o eixo espacial em $(\bar t=0,\ \bar x=a)$ e retorna em $\bar t=+a$ (o caso particular $a=2$ que usamos no exemplo do Exercício 1.3): a simetria entre ida e volta do raio de luz é exatamente o que garante que o fator de escala do tempo é igual ao do espaço.

Com $\alpha=\sigma$, a transformação fica:

$$
\bar t = \alpha\(t-vx) \qquad \text{e} \qquad \bar x = \alpha\(x-vt) \qquad \text{(ii)}
$$

Só falta descobrir quanto vale $\alpha$.

---

## 4. Passo 3: a invariância do intervalo determina $\alpha$

É aqui que usamos o resultado central do post anterior: o teorema de [Invariância do Intervalo](https://github.com/m0rang0azul/invariancia-do-intervalo). Para qualquer par de eventos,

$$-(\bar t)^2 + (\bar x)^2 = -t^2 + x^2$$

Substituindo as Eqs. (ii) do lado esquerdo:

$$-\big[\alpha(t-vx)\big]^2 + \big[\alpha(x-vt)\big]^2 = -t^2+x^2$$

Expandindo os dois binômios ao quadrado:

$$\alpha^2\Big[-(t^2 - 2vtx + v^2x^2) + (x^2 - 2vtx + v^2t^2)\Big] = -t^2+x^2$$

Repare que os termos cruzados $-2vtx$ se cancelam exatamente (um entra com sinal $+2vtx$, o outro com $-2vtx$, depois da distribuição do sinal de menos):

$$\alpha^2\Big[-t^2 + v^2t^2 + x^2 - v^2x^2\Big] = -t^2+x^2$$

Agrupando os termos em $t^2$ e em $x^2$:

$$\alpha^2\Big[-t^2(1-v^2) + x^2(1-v^2)\Big] = -t^2+x^2$$

$$\alpha^2\(1-v^2)\(-t^2+x^2) = -t^2+x^2$$

Para que essa igualdade valha para **qualquer** evento $(t,x)$, o fator que multiplica $(-t^2+x^2)$ do lado esquerdo precisa ser exatamente $1$:

$$\alpha^2\(1-v^2) = 1 \quad\Longrightarrow\quad \alpha^2 = \frac{1}{1-v^2} \quad\Longrightarrow\quad \alpha = \pm\frac{1}{\sqrt{1-v^2}}$$

Escolhemos o sinal positivo pelo mesmo tipo de argumento de continuidade que já usamos na prova de $\phi(v)=1$: quando $v=0$, os dois referenciais coincidem, e a transformação precisa virar a identidade ($\bar t=t,\ \bar x=x$), o que só acontece com o sinal $+$. Definindo o fator de Lorentz:

$$\gamma \equiv \frac{1}{\sqrt{1-v^2}}$$

concluímos que $\alpha = \gamma$.

---

## 5. As equações finais: a transformação de Lorentz (Eq. 1.12)

Juntando tudo:

$$\boxed{\begin{aligned}
\bar t &= \gamma\(t - vx) \\
\bar x &= \gamma\(x - vt) \\
\bar y &= y \\
\bar z &= z
\end{aligned}}$$

Essa é a transformação de Lorentz para um *boost* (um "chute" de velocidade) ao longo do eixo $x$. Agora sabemos exatamente de onde ela vem: da geometria dos eixos inclinados (Passo 1), da simetria da velocidade da luz (Passo 2), e da invariância do intervalo (Passo 3).

### O que essa fórmula está dizendo, fisicamente

:shipit: **Mistura de espaço e tempo:** repare que $\bar t$ depende não só de $t$, mas também de $x$. Isso é a tradução algébrica direta da relatividade da simultaneidade que já tínhamos visto geometricamente (Seção 4 do primeiro post): o "agora" de $\bar O$ não coincide com o "agora" de $O$.

:shipit: **Limite newtoniano ($v \ll 1$):** quando a velocidade é muito menor que a da luz, $v^2 \approx 0$, então $\gamma \approx 1$, e as equações se reduzem a $\bar t \approx t$ e $\bar x \approx x - vt$: exatamente a transformação de Galileu da física clássica.
 
:shipit: **A barreira de $c$:** se $v \to 1$, então $\gamma \to \infty$. Isso é um sinal de que nenhum referencial com massa pode atingir ou ultrapassar a velocidade da luz, as equações simplesmente "explodem" nesse limite.

---

## 6. Seção 1.10: a lei de adição de velocidades de Einstein

Com a transformação de Lorentz em mãos, podemos responder a uma pergunta natural: se uma partícula se move com velocidade $W$ no referencial $\bar O$, e $\bar O$ se move com velocidade $v$ em relação a $O$, qual é a velocidade $W'$ da partícula medida por $O$?

Na física newtoniana, a resposta seria simplesmente $W' = W + v$, vamos ver o que a relatividade diz.

### Dedução

Definimos $W \equiv d\bar x/d\bar t$ (velocidade da partícula em $\bar O$) e $W' \equiv dx/dt$ (velocidade da mesma partícula em $O$). Para relacionar os dois, precisamos da transformação **inversa** de Lorentz, de $\bar O$ para $O$ (basta trocar $v \to -v$ e inverter os papéis nas Eqs. da Seção 5):

$$dx = \gamma\(d\bar x + vd\bar t) \qquad \text{e} \qquad dt = \gamma\(d\bar t + vd\bar x)$$

Calculando a razão:

$$W' = \frac{dx}{dt} = \frac{\gamma\(d\bar x + vd\bar t)}{\gamma\(d\bar t + vd\bar x)} = \frac{d\bar x + vd\bar t}{d\bar t + vd\bar x}$$

(o fator $\gamma$ cancela entre numerador e denominador). Dividindo todo mundo por $d\bar t$:

$$W' = \frac{\dfrac{d\bar x}{d\bar t} + v}{1 + v\dfrac{d\bar x}{d\bar t}}$$

Como $W = d\bar x/d\bar t$, chegamos à **lei de adição de velocidades de Einstein** (Eq. 1.13 de Schutz):

$$\boxed{W' = \frac{W+v}{1+Wv}}$$

### Três consequências importantes

**1. Nunca se ultrapassa $c=1$.** Suponha, por absurdo, que $W'=1$ mesmo com $W<1$ e $v<1$:

$$
1 = \frac{W+v}{1+Wv} \qquad \Longrightarrow\ \qquad 1+Wv = W+v \qquad \Longrightarrow\ \qquad 1-v-W+Wv=0 \qquad \Longrightarrow\ \qquad (1-v)(1-W) =0
$$

Essa igualdade só é satisfeita se $v=1$ ou $W=1$. Ou seja: **somar duas velocidades estritamente menores que $1$ nunca produz uma velocidade maior ou igual a $1$.** A velocidade da luz funciona como um limite que a soma relativística respeita automaticamente, diferente da soma newtoniana.

**2. A luz continua andando a $1$, não importa o referencial.** Se a "partícula" for um fóton, $W=1$:

$$W' = \frac{1+v}{1+v} = 1$$

Não importa o valor de $v$: todo observador inercial mede exatamente $1$ para a velocidade da luz. É o segundo postulado de Einstein reaparecendo, agora como consequência algébrica da própria lei de adição, e não como hipótese extra.

**3. No regime cotidiano, viramos Galileu de novo.** Quando $v \ll 1$ e $W \ll 1$ (velocidades muito menores que a da luz), o termo $Wv$ no denominador fica desprezível perto de $1$:

$$W' \approx W + v$$

É por isso que a soma simples de velocidades funciona perfeitamente bem no dia a dia (carros, aviões, bolas de futebol): as correções relativísticas são da ordem de $Wv$, irrelevantes nessas velocidades.

---

## Referências

- SCHUTZ, Bernard. *A First Course in General Relativity*. 3ª ed. Cambridge: Cambridge University Press, 2022. Capítulo 1, Seção 1.9 e 1.10.

---

*Post baseado no experimento mental do relógio de luz e nos diagramas de Minkowski, seguindo a abordagem do livro de Bernard Schutz, "A First Course in General Relativity".*
