# R

![paprika_mask](https://user-images.githubusercontent.com/128937668/233753111-cf3e9133-2bb0-4b9d-b285-79342877a0b5.gif)

## semana 1: Introdução ao R-Studio

1. **Os softwares R e R-Studio**

O **R** é, ao mesmo tempo, uma linguagem de programação e um software gratuito de código aberto para *visualização de dados e computação estatística*.

O que é uma linguagem de programação? É por onde a máquina e o programador se comunicam. É uma linguagem formal que funciona por meio de uma série de instruções, símbolos, palavras-chave, regras semânticas e sintáticas.

Através de pacotes (ou *packages*) é possível aumentar as capacidades do R.

**Como instalar o R**

Para instalar o R siga os seguintes passos:

* Vá ao site do [cran](https://cran.r-project.org/).

* Se for Windows, vá em `install now for the first time`.

* Clique em `Download R-4.2.3 for Windows` e clique em avançar, avançar e avançar.

* Pronto! O R foi instalado.

**O R-Sudio**

O R-Studio é uma interface funcional e amigável para o R.

**Como instalar o R-Stduio**

Para instalar a última versão do R-Studio, siga os seguintes passos:

* Vá ao site do [R-Studio desktop](https://posit.co/download/rstudio-desktop/).

* Caso seu sistema operacional seja Windows, basta ir em `Download R-Studio Desktop for Windows`.

* Clique em executar e faça novamente a instalação padrão.

2. **Primeiros passos no R-Studio**

Para compreender as interfaces básicas do R-Studio, vá em file -> new file -> R script e abrirá uma janela.

No primeiro quadrante temos o *editor*, no segundo os *objetos*, no terceiro o *console* e no quarto o *output*.

* Editor/script: onde serão escritos todos os códigos.

* Console: onde os códigos são compilados e, caso tenha algum erro na estrutura do código, o erro é apresentado nesse painel.

* Objetos: painel com todos os objetos criados no presente trabalho.

* History: painel com um histórico dos comandos rodados.

* Files: mostra os arquivos no diretório de trabalho. É possível navegar entre os diretórios.

* Plots: painel onde os gráficos serão apresentados.

* Help: janela onde a documentação das funções serão apresentadas.

---

**Funções**

As funções em R seguem a mesma lógica de funções matemáticas:

**y = f(x)**

A função acima informa que a *variável* y depende dos valores de x para ser definida. O termo x é o que chamamos de argumento da função. Assim, por exemplo, se x é um valor de números e f(x) fornece a média de x, temos no R:

`y=mean(x)`

Assim, no **R**, sempre trabalharemos com funções que dependerão de um ou mais argumentos para que funcionem de maneira correta.

**Executar (ou rodar) o código no R**

Quando colocamos a nossa linha de código ou até mesmo todo o nosso script no editor de texto do R, ele não irá fazer nada. A menos que você dê uma ordem para o R executar o seu código.

Para executar o código existem duas formas:

* Usando o teclado: ctrl + enter

* Usando o mouse: clique no botão `Run`

Essa ordem pode ser para executar apenas uma linha de código, um conjunto de linhas ou até mesmo todo o seu script.

O que vai definir a parte do código que será executada?

Depende do que está selecionado pelo seu mouse.

Por exemplo, se você selecionar todas as linhas do script e pedir para executar, todo o script será executado.

Se você selecionar só uma parte, só essa parte irá rodar.

3. **Manipulação de objetos no R**

A linguagem R é **orientada a objetos** e, na prática, isso significa que tudo no R será um objeto.

imagine que esse 'objeto' é uma variável capaz de armazenar um valor ou uma de dados e o operador de atribuição é representado pelo = ou <-. Exemplo:

```
variavel1 = 5
variavel2 <- 2
```

Nesse exemplo, estou atribuindo o valor 5 para o objeto 'variavel1' e o valor 2 ao objeto 'variavel2'.

Para escrever comentários em seu código no R, basta apertar o # e tudo que será escrito na frente dele virá como comentário:

```
# definindo o objeto variavel1
variavel1 = 5
# definindo o objeto variavel2
variavel2 <- 2
```

Os comentários são excelentes estratégias na criação dos códigos para facilitar o entendimento do que está sendo feito.

Para criar palavras ou frases, elas devem vir entre aspas na sua definição:

```
# definindo o objeto variavel3
variavel3 = "Niterói"
# definindo o objeto variavel4
variável4 = "Rio de Janeiro"
```

De um modo geral, você vai escolher o nome que mais fizer sentido para o seu objeto, de forma que fique fácil de saber do que se trata. os nomes dos objetos não podem começar com números e com caracteres especiais. O R diferencia letras maiúsculas de minúsculas.

---

**Vetores**

Conjunto de elementos de uma mesma natureza. Podem ser numéricos ou não e a função **'c'** irá organizar os valores em um vetor e os elementos do vetor são separados por vírgula. Exemplos:

```
# Criando o vetor com os nomes de algumas cidades
cidade = c("Rio de Janeiro, "Niterói", "São Gonçalo", "Maricá", "Caxias", "Nilópolis", "Resende", "Macaé")
# Visualizando o vetor
cidade
```

Suponha que seja de interesse investigar o número de roubos nessas cidades em duas semanas:

```
# Criando o vetor número de roubos na 1a semana por cidade
roubos_1sem = c(20, 30, 40, 23, 22, 19, 32, 42)
# Visualizando o vetor
roubos_1sem
```

```
# Criando o vetor número de roubos na 2a semana por cidade
roubos_2sem = c(12, 39, 49, 13, 25, 19, 52, 18)
# Visualizando o vetor
roubos_2sem
```

No R temos as classes dos caracteres e dos números, basicamente. Existem outras classes mas não serão nosso foco agora.

```
# Checando a classe de um vetor
class(cidade)
class(roubos_2sem)
```

A simbologia utilizada pelo R para operadores aritméticos elementares é apresentada na seguinte tabela:

operador aritmético | símbolo
---|---|
soma | +
subtração | -
divisão | /
multiplicação | *
potência | ^

Assim, podemos relizar operações com os vetores:

```
# Dividindo o número de roubos da segunda semana por 7
roubos_2sem / 7
```

```
# Somando os roubos nas duas semanas
roubos_1sem + roubos_2sem
```

```
# Acessando elemento(s) de uma vetor
roubos_1sem[2]
```

```
# Tirando elemento(s) de um vetor
roubos_1sem[-2]
```

```
# Acessando elemento(s) de um vetor
roubos_1sem[c(1,3)]
```

**Aplicando funções básicas:**

```
# Máximo
max(roubos_1sem)
```

```
# Mínimo
min(roubos_1sem)
```

```
# Posição do valor máximo no vetor
which.max(roubos_1sem)
```

```
# Posição do valor mínimo no vetor
which.min(roubos_1sem)
```

```
# Tamanho do vetor
length(roubos_1sem)
```

```
# Ordenar o vetor
sort(roubos_1sem)
```

observação: para criar números quebrados, o R utiliza o 'ponto' como separador decimal:

```
# Raiz quadrada
R = sqrt(22)
R
```

---

**Exercícios propostos**

* Crie um vetor chamado de Alunos com os nomes Adriana, Carlos, Gustavo, Pedro, Letícia e Mariana.

* Crie um vetor chamado de Notas1 para armazenar as notas na primeria prova e inclua os valores: 45, 60, 80, 95, 31 e 77. Calcule a média e encontre os valores máximo e mínimo.

* Crie um vetor chamado de Notas2 para armazenar as notas na segunda prova e inclua os valores: 80, 45, 78, 46, 23 e 86. Calcule a média e encontre os valores máximo e mínimo.

* Assuma que a primeira prova tenha um peso 0.7 e a segunda prova um peso de 0.3. Considere que a nota final dos alunos será dada pela soma das duas provas multiplicadas pelos respectivos pesos. Armazene a nota final dos alunos na variável NotasF.

---

4. **Pedindo ajuda no R**

A documentação do R traz tudo o que nós precisamos saber para usarmos uma determinada função.

```
?mean
help(mean)
```

Com os comandos acima, é possível ter uma breve descrição do que a referida função executa bem como a definição de todos os seus argumentos.

---

5. **Salvando sua sessão no R**

Para *salvar* seu script, basta ir em File -> Save. Para encerrar, basta apertar o 'X'.
