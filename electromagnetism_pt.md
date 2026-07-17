---
description: Princípios físicos para a estimulação magnética transcraniana (EMT)
---

# Princípios de Eletromagnetismo aplicado à EMT

Tudo começa com as quatro equações de Maxwell:

$$
\bf{\nabla}\times\bf{B} = \mu_0\bf{J} + \mu_0\varepsilon_0\frac{ \partial \bf{E}}{\partial t} \qquad \text{(Lei de Ampère)}
$$

$$
\bf{\nabla}\times\bf{E} = - \frac{\partial \bf{B}}{\partial t} \qquad \text{(Lei de Faraday)}
$$

$$
\bf{\nabla}\cdot\bf{B} = 0 \qquad \text{(Lei de Gauss)}
$$

$$
\bf{\nabla}\cdot\bf{E} = \frac{\rho}{{\varepsilon_0}} \qquad \text{(Lei de Coulomb)}
$$

Para conhecer os efeitos da EMT, precisamos calcular o campo elétrico induzido no tecido cerebral. Considere uma corrente elétrica $$I(t)$$ que varia ao longo do tempo e percorre uma bobina distante, no espaço livre. A corrente variável gerará um campo magnético que também varia com o tempo. De acordo com a lei da indução de Faraday, o campo magnético variável induzirá no espaço um campo elétrico primário associado $$\bf{E}_1$$.

No entanto, ao inserirmos um meio condutor próximo à bobina, o campo primário $$\bf{E}_1​$$ causará uma separação de cargas no meio condutor que, por sua vez, gerará um campo elétrico secundário ($$\bf{E}_2​$$). Portanto, se considerarmos que o cérebro é condutor e está suficientemente próximo da bobina de estimulação, o campo elétrico total induzido no tecido será a soma dos campos elétricos primário e secundário.

$$
\bf{E}_{total} = \bf{E}_1 + \bf{E}_2
$$

Para calcular o campo elétrico total no cérebro, podemos calcular separadamente $$\bf{E}_1$$ e $$\bf{E}_2$$, usando aproximações semelhantes, mas métodos diferentes. Antes de tudo, devemos considerar que a EMT é um problema quase estático.

Para a aproximação quase estática, consideramos:

1. Não há acúmulo de cargas;
2. Para a distância dada entre a bobina e a cabeça, não há tempo retardado; em outras palavras, não há diferença de fase entre os campos magnético e elétrico.

Também separamos em duas partes as soluções de $$\bf{E}_1$$ e $$\bf{E}_2$$. Primeiro, para $$\bf{E}_1$$, usamos a lei de Faraday, com a definição do potencial vetor magnético:

$$
\bf{E}_1(\bf{r}, t) = - \frac{\partial \bf{A}(\bf{r}, t)}{\partial t}
$$

Para $$\bf{E}_2$$, a interpretação é um pouco mais complicada. O campo $$\bf{E}_2$$ existe apenas no meio condutor e também está associado a um campo magnético secundário $$\bf{B}_2$$.

$$
\bf{\nabla}\times\bf{E}_2 = - \frac{\partial \bf{B}_2}{\partial t}
$$

$$
\bf{\nabla}\cdot\bf{E}_2 = \frac{\rho}{{\varepsilon_0}} \qquad \text{Válido em qualquer lugar do cérebro}
$$

No entanto, considerando a aproximação quase estática e que a condutividade do meio é muito baixa, $$\bf{B}_2$$ é desprezível e, portanto, temos:

$$
\bf{\nabla}\times\bf{E}_2 \approx 0
$$

Mas também sabemos que:

$$
\bf{J}=\sigma\bf{E}
$$

e então podemos substituir na equação de $$\bf{\nabla}\cdot\bf{E}_2$$ e obter:

$$
\bf{\nabla}\cdot\bf{E}_2 = \nabla \cdot {(\frac{\bf{J}}{\sigma})}
$$

Se considerarmos que a condutividade é igual em todos os pontos de um meio homogêneo, então ela é constante, e:

$$
\bf{\nabla}\cdot\bf{E}_2 = \frac{1}{\sigma} \nabla \cdot {\bf{J}}
$$

Então também podemos chegar a:

$$
\frac{\rho}{{\varepsilon_0}} = \frac{1}{\sigma} \nabla \cdot {\bf{J}}
$$

E, finalmente:

$$
\nabla \cdot {\bf{J}} = \frac{\sigma}{{\varepsilon_0}} \rho
$$

De acordo com a conservação das correntes em um sistema no qual nenhuma corrente elétrica \(ou carga\) é adicionada ao meio condutor, temos:

$$
\bf{\nabla}\cdot\bf{J} + \frac{\partial \rho }{\partial t} = 0
$$

Se combinarmos as duas últimas equações, obteremos:

$$
-\frac{\sigma}{{\varepsilon_0}} \rho = \frac{\partial\rho}{\partial t}
$$

A solução, então, é a função exponencial da forma:

$$
\rho(t) = \rho_0 e^{-\omega_0 t}
$$

$$\omega_0$$ é a frequência característica que surge da solução de qualquer derivada parcial em relação ao tempo, como a apresentada acima, levando a um tempo característico (ou constante de tempo) $$\tau$$. O inverso de $$\tau$$ define a frequência característica $$\omega_0$$, que, para esta aplicação, definimos com base nas propriedades do material condutor (o cérebro):

$$
\omega_0 \equiv \frac{\sigma}{\varepsilon_0}
$$

Que é, então:

$$
\omega_0 \approx 1.8 \times10^{-9} \text s
$$

Assim, a equação $$\nabla \cdot {\bf{J}} = \frac{\sigma} \rho$$ torna-se:

$$
\nabla \cdot {\bf{J}} = 0
$$

Isso significa que a corrente total no sistema é o divergente da densidade de corrente somado à variação temporal da densidade de carga. Além disso, se $$\rho$$ tende a zero, temos:

$$
\bf{\nabla}\cdot\bf{E}_2 = 0
$$

E, pelo fato de que:

$$
\bf{\nabla}\times\bf{E}_2 = 0
$$

Então $$\bf{E}_2$$ pode ser escrito como o gradiente de um potencial escalar, que, por sua vez, é:

$$
\bf{E}_2 = - \nabla V
$$

Se substituirmos no divergente de $$\bf{E}_2$$, teremos dois casos possíveis:

$$
\bf{\nabla}\cdot\bf{E}_2 = \frac{\rho}{\varepsilon_0} = - \nabla^2V
$$

$$
\nabla^2V = - \frac{\rho}{\varepsilon_0} \qquad \text{Equação de Poisson}
$$

E o segundo caso:

$$
\bf{\nabla}\cdot\bf{E}_2 = 0 = - \nabla^2V
$$

$$
\nabla^2V = 0 \qquad \text{Equação de Laplace}
$$

Para ambos os casos, há maneiras possíveis de resolver o potencial e, então, obter o campo elétrico secundário $$\bf{E}_2$$. Observe que $$\bf{E}_1$$ e $$\bf{E}_2$$ ocorrem ao mesmo tempo, portanto é possível haver uma separação de cargas que leve à existência de $$\bf{E}_2$$ sem acúmulo de cargas ao longo do tempo.

Outro parâmetro a considerar na aproximação quase estática é a profundidade de penetração $$\delta$$. A profundidade de penetração é a distância na qual o campo elétrico decai, à medida que avança no condutor, por um fator de $$1/e$$. Essa definição pode ser encontrada no Capítulo 9.4 de Introduction to Electrodynamics, de Griffiths, que trata de ondas eletromagnéticas em condutores (4ª edição, página 417). Em nosso caso, o diâmetro $$D$$ da cabeça é muito maior do que a profundidade de penetração. Considere as duas equações de Maxwell:

$$
\bf{\nabla}\times\bf{E} = - \frac{\partial \bf{B}}{\partial t} \qquad \text{(i)}
$$

$$
\bf{\nabla}\times\bf{B} = \mu_0\bf{J} + \mu_0\varepsilon_0\frac{ \partial \bf{E}}{\partial t} \qquad \text{(ii)}
$$

Se aplicarmos o rotacional a $$\text{i}$$ e $$\text{ii}$$, seguindo a identidade matemática:

$$
\bf{\nabla}\times(\bf{\nabla}\times\bf{A}) = \bf{\nabla}(\bf{\nabla}\dot\bf{A}) + \nabla^2\bf{A}
$$

Chegaremos a:

$$
\nabla^2\bf{E}=\mu\epsilon \frac{\partial^2\bf{E}}{\partial^2 t} +\mu\sigma \frac{\partial\bf{E}}{\partial t}
$$

Que admite a solução de onda plana:

$$
\tilde{E}(z,t) = \tilde{E}_0e^{i(\tilde{k}z-\omega t)}
$$

em que $$\tilde{k}$$ é o número de onda complexo, escrito como:

$$
\tilde{k}^2=\mu\epsilon\omega^2 + i\mu\sigma\omega
$$

Tenha cuidado: $$\omega$$ nesta equação não tem relação com $$\omega_0$$, apresentado acima para a solução da densidade de carga $$\rho_0$$. Extraindo a raiz quadrada:

$$
\tilde{k}=k + i\kappa
$$

$$
k=\omega\sqrt{\frac{\epsilon\mu}{2}}\Bigg[\sqrt{1+\Big(\frac{\sigma}{\epsilon\omega}\Big)^2}+1\Bigg]^{1/2} \quad, \quad \kappa\equiv\omega\sqrt{\frac{\epsilon\mu}{2}}\Bigg[\sqrt{1+\Big(\frac{\sigma}{\epsilon\omega}\Big)^2}-1\Bigg]^{1/2}
$$

A atenuação vem da parte imaginária de $$\tilde{k}$$, que reduz $$\tilde{E}(z,t)$$ à medida que $$z$$ aumenta. Então:

$$
\tilde{E}(z,t) = \tilde{E}_0e^{-\kappa z}e^{i(kz-\omega t)}
$$

Por fim, a profundidade de penetração $$\delta$$ vem da distância na qual o campo elétrico decai, à medida que avança no condutor, por um fator de $$1/e$$, e é:

$$
\delta=\frac{1}{\kappa}
$$

Por fim, considerando que:

$$
\omega_0 \equiv \frac{\sigma}{\varepsilon_0}
$$

E que $$\omega/\omega_0\ll1$$, obtemos:

$$
\delta \equiv \frac{1}{2}\mu_0\sigma\omega
$$

Também podemos escrever $$E(z,t)$$ como:

$$
\nabla^2{\bf{E}}= -(i\mu_0\sigma\omega + \mu_0\epsilon\omega^2)\bf{E}
$$

Se tomarmos a condutividade do cérebro como $$\sigma=0.4 / \Omega\text{-m}$$ e $$\omega=10^5 \text{Hz}$$, então $$\delta^2=4.0 \times 10^5 \text{cm}^2$$ e, portanto, $$(D/\delta)^2\ll1$$. De acordo com Heller et al. (1992), essa é a essência da aproximação quase estática e leva a:

$$
\nabla^2{\bf{E}}= 0
$$

Portanto, um campo elétrico estático não pode penetrar em um condutor...
