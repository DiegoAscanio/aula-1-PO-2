<style>
  .cabecalho {
    position: absolute;
    top: 10%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 48px;
    font-weight: bold;
  }
  .conteudo {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }
</style>


![bg opacity](./background.png)
# Pesquisa Operacional II
## Revisão de Álgebra Linear

Prof. Ms.c Diego Ascânio Santos

Belo Horizonte, 2023.

---
<style scoped>
  h1 {
    position: absolute;
    top: 45%;
    bottom: 45%;
    margin-left: 37.5%;
    color: #000000;
  }
</style>

# Vetores

---
![bg opacity](./background.png)
<div class="cabecalho">
Vetores - Definição
</div>
<div class="conteudo">
Uma entidade matemática que representa um ponto em um espaço de N dimensões (n-dimensional).
<ul>
  <li>Representado por coordenadas - (x, y, z);</li>
  <li>Podem ser somados (subtraídos) ou multiplicados por valores escalares;</li>
  <li>Possuem magnitude (norma) e direção;</li>
</ul>
</div>

---
<div class="cabecalho">
Vetores - Aplicações
</div>
<div class="conteudo">
  <ol>
    <li>Descrição de movimentos e forças físicas em mecânica e física;</li>
    <li>Representação de dados multidimensionais em estatística e aprendizado de máquina;</li>
    <li>Descrição de campos físicos, como o campo elétrico ou magnético, em física;</li>
    <li>Representação de cargas, tensões e inclinações na Engenharia Civil;</li>
    <li>Cálculo e modelo de comportamentos estruturais de edificações (prédios, pontes, barragens, etc.);</li>
  </ol>
</div>

---
<style scoped>
  h1 {
    position: absolute;
    top: 35%;
    bottom: 45%;
    margin-left: -5%;
    text-align: center;
    color: #000000;
  }
  h2 {
    position: absolute;
    top: 55%;
    margin-left: 22.5%;
    text-align: center;
    color: #000000;
  }

</style>
![bg opacity](./background.png)

# Como é feito o cálculo e a modelagem de comportamentos estruturais?
## Através de sistemas lineares!

---
<div class="cabecalho">
Sistemas Lineares - Definição
</div>
<div class="conteudo">
<p>
Diversos problemas da Engenharia, Estatística, Química, Ciências Sociais Aplicadas, dentre outras áreas consistem em encontrar os valores de mútiplas variáveis que se relacionam entre si através de equações lineares.
</p>
<p>
Exemplos:
<ul>
  <li>Estequeometria (balanceamento de reações químicas);</li>
  <li>Predição de preços de imóveis;</li>
  <li>Tráfego de Veículos</li>
</ul>
</p>
</div>

---
<style scoped>
p {
  font-size: 20px;
}
</style>
![bg opacity](./background.png)
<div class="cabecalho">
Sistemas Lineares - Estequeometria
</div>

Consideremos a equação $H_2 + O_2 \rightarrow H_2O$. Encontra-se desbalanceada <!-- Pois, o numero de átomos de Oxigenio da esquerda é distinto do átomos da direita-->

Como balancear a equação? Adicionando-se variáveis aos elementos e montando um sistema para encontrar seus valores:

$x_{1}H_{2} + x_{2}O_{2} \rightarrow x_{3} H_{2}O$

Isso implica que:

$$
\begin{cases} 
2x = 2z 
\\ 
2y = z
\end{cases}
$$

Numa forma escalonada:

$$
\begin{cases} 
2x+ 0y - 2z = 0
\\ 
0x + 2y - z = 0
\\
0x + 0y + 0z = 0
\end{cases}
$$

---
<style scoped>
p {
  font-size: 22px;
}
.cabecalho_2 {
  font-size: 32px;
}
</style>
<div class="cabecalho cabecalho_2">
Sistemas Lineares - Representação Vetorial / Matricial.
</div>

Considerando a forma escalonada do sistema linear de Estequeometria que estamos estudando:

$$
\begin{cases} 
2x+ 0y - 2z = 0
\\ 
0x + 2y - z = 0
\\
0x + 0y + 0z = 0
\end{cases}
$$

É possível realizar uma representação matricial da forma $Ax = b$:

$$
\begin{bmatrix}
2 & 0 & -2 \\
0 & 2 & -1 \\
0 & 0 & 0 \\
\end{bmatrix} 
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
= 
\begin{bmatrix}
0 \\
0 \\
0 \\
\end{bmatrix}
$$

É possível, porém não recomendado, interpretar uma matriz como um vetor de vetores. Como descobrir se um sistema linear possui soluções (determinadas ou indeterminadas) ou não possui sem solucioná-lo de imediato?

---
<style scoped>
p {
  font-size: 20px;
}
.cabecalho_2 {
  font-size: 32px;
}
</style>
<div class="cabecalho cabecalho_2">Dependência e Independência Linear</div>

Como descrobrir se um sistema linear possui ou não soluções (Determinadas, Indeterminadas ou Impossíveis) sem resolvê-lo de imediato?

Através do estudo da (In)Dependência Linear dos vetores coluna que compõem sua matriz $A$ de coeficientes.

Podemos considerar que vetores x, y, z são linearmente independentes se e somente-se:

$$
\alpha_{1}x + \alpha_{2}y + \alpha_{3}z = 0, \alpha_{1} = \alpha_{2} = \alpha_{3} = 0
$$

Se existir qualquer valor $\alpha_{i} \neq 0$, então, existe dependência linear entre os vetores.

Porque isto é importante?

Pois, se os vetores coluna de um sistema linear forem linearmente independentes, logo, para qualquer termo independente b o sistema terá solução possível e determinada.

Agora, se forem linearmente dependentes, então, o sistema pode ser impossível ou possível e indeterminado ao depender dos termos b.

---


