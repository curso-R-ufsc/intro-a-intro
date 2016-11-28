---
title       : Começando com o R
description : Noções básicas de R
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf
--- type:NormalExercise lang:r xp:100 skills:1 key:aee54d223d
## O início

Para começar o que é o `R`? De acordo com [a definição da comunidade](http://pt.stackoverflow.com/tags/r/info), o R é um ambiente e linguagem de programação de código aberto para computação estatística, bioinformática e gráficos. Legal! E o que isso quer dizer? Bem, quer dizer que ele é capaz de realizar cálculos grandes e complexos com enorme confiabilidade e rapidez. Além disso, pode gerar todo tipo de gráfico(https://www.google.com.br/search?q=ggplot2+graphics&biw=1366&bih=662&source=lnms&tbm=isch&sa=X&ved=0ahUKEwjkrJOX2cLQAhUMl5AKHcvZD30Q_AUIBigB), [documentos interativos](http://timelyportfolio.github.io/rCharts_nyt_home_price/) e apresentação dinâmca de dados ([shiny](https://tomasbarcellos.shinyapps.io/imoveis-floripa/)).

Este "curso" no DataCamp é apenas uma apresentação muito rápida daquilo que é extremamente básico no R, isto é:

1. Uma apresentação inicial do R e deste site

2. Ferramentas, pacotes e comunidade

3. Sintexe e objetos

4. Tipos de objetos


*** =instructions
Apenas aperte o botão "Submit" para ver o `R`em ação!
*** =hint

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Você não precisa entender isso ainda
dados <- rnorm(1e6) # Cria 1 milhão de dados aleatórios
                    # com distribuição normal

mean(dados) # calcula média dos dados
hist(dados, main = "Histograma que criei", ylab = "Frequencia") # faz histograma dos dados
```

*** =solution
```{r}
# Você não precisa entender isso ainda
dados <- rnorm(1e6) # Cria 1 milhão de dados aleatórios
                    # com distribuição normal

mean(dados) # calcula média dos dados
hist(dados, main = "Histograma que criei", ylab = "Frequencia") # faz histograma dos dados
```

*** =sct
```{r}
test_an_object("dados")
test_function('rnorm', args = 'n', not_called_msg = 'Você não precisa mudar nada no código. Resete o exercício <kbd>ctrl</kbd> + <kbd>R</kbd> e apenas clique em "Submit"',
              incorrect_msg = 'Você não precisa mudar nada no código. Resete o exercício <kbd>ctrl</kbd> + <kbd>R</kbd> e apenas clique em "Submit"')
test_function('mean', args = "x", not_called_msg = 'Você não precisa mudar nada no código. Resete o exercício <kbd>ctrl</kbd> + <kbd>R</kbd> e apenas clique em "Submit"',
              incorrect_msg = 'Você não precisa mudar nada no código. Resete o exercício <kbd>ctrl</kbd> + <kbd>R</kbd> e apenas clique em "Submit"')
test_function('hist', args = c("x", "main", "ylab"), not_called_msg = 'Você não precisa mudar nada no código. Resete o exercício <kbd>ctrl</kbd> + <kbd>R</kbd> e apenas clique em "Submit"',
              incorrect_msg = 'Você não precisa mudar nada no código. Resete o exercício <kbd>ctrl</kbd> + <kbd>R</kbd> e apenas clique em "Submit"')
success_msg("Observe o console: a media dos dados foi impressa. E um grafico criado ao lado do script. Rapido, não?!")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:dcb32212d2
## Conhecendo o R e DataCamp

O `R` é um programa de código aberto com uma comunidade muito ativa. A equipe responsável para manter o `R` mantém o site: https://www.r-project.org/, onde você pode [baixar sua versão mais recente (3.3.2)](https://cran.fiocruz.br/). O `R` está disponível para todos os sistemas operacionais e é gratuito, ou seja, você pode usar ele onde quiser sem nenhuma limitação (no trabalho ou em casa). Esta realidade é muito diferente de outros softwares estatísticos como SPSS, SAS e Stata. 

Geralmente, no lugar onde você está lendo este texto ficam algumas lições.

*** =instructions

O `DataCamp` é o site que está rodando este curso. Ele possibilita criar cursos de `R` com esta interface legal. Ele permite que você aprenda `R`sem precisar baixa ele, porque quando você clicar em "Submit", ele vai rodar o código que você escrever no *script*. Nesta parte costuma ter instruções para o exercício, mas neste caso elas estão no script para usar melhor o espaço da tela :P

Quando clicar em "Hint" você receberá alguma dica.

*** =hint
Leia as intruções no script.
*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Todo texto que começa com '#' é um comentário no R e não faz nada

# Se você apertar ctrl + enter apenas a linha selecionada será executada
# Se você clicar em "Submit" todo o conteúdo do script é executado

# Agora que você sabe como não fazer nada, digite '5 + 10' na linha abaixo


# E veja o comando ser executado no console (abaixo)
```

*** =solution
```{r}
# Todo texto que começa com '#' é um comentário no R e não faz nada

# Se você apertar ctrl + enter apenas a linha selecionada será executada
# Se você clicar em "Submit" todo o conteúdo do script é executado

# Agora que você sabe como não fazer nada, digite '5 + 10' na linha abaixo
5 + 10

# E veja o comando ser executado no console (abaixo)
```

*** =sct
```{r}
test_output_contains("5+10",
                     incorrect_msg = "Voce precisa somar 5 e 10 para terminar este exercicio!")
success_msg("Muito bem!! Viu como e facil fazer uma conta?")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:63e01c769d
## Pedindo ajuda

Você logo logo perceberá que você precisará pedir ajuda muito frequentemente. Você pode fazer isso por alguns canais.

O primeiro deles é o próprio `R`: há uma função para pedir ajuda sobre outras funções e documentação do `R` em geral, `help('alguma_funcao')`. Ela também pode ser acessada por `?alguma_funcao`.

Há ainda outra forma de pedir ajuda: `help.search("alguma duvida")` ou `??"alguma duvida"`. Nesta você pode botar um tema ou uma expressão.

A última maneira é pedir ajuda a outras pessoas. Uma ótima forma de fazer isso é por meio do site de perguntas e respostas [StackOverflow](http://pt.stackoverflow.com/). Tem até dicas sobre [como fazer](http://pt.stackoverflow.com/help/how-to-ask) uma pergunta.

*** =instructions
Chegou a sua vez:

* Busque ajuda sobre a função `max`

* Pergunte ao `R`sobre `"regression"` (sim, as expressões devem ser buscadas em inglês)

*** =hint


*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Peça ajuda sobre a função 'max': help(max)

# Agora busque pela expressão "regression" (as aspas são necessárias aqui)

```

*** =solution
```{r}
# Peça ajuda sobre a função 'max': help(max)
?max
# Agora busque pela expressão "regression" (as aspas são necessárias aqui)
??"regression"
```

*** =sct
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

test_student_typed(c("help(max)",
                     "?max"),
                   not_typed_msg = "Voce se esqueceu de usar a `?` ou a funcao help(max)")

test_student_typed(c('help.search("regression")', ??"regression"),
                   not_typed_msg = 'Voce se esqueceu de usar a `??` ou a funcao help.search("regression")')


success_msg("Muito bem! Agora que voce ja sabe tirar sua duvidas, vamos colocar algumas na sua mente!")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:0f9f2276da
## Objetos

Nesta capítulo veremos um pouco sobre o objeto mais básico do R, o vetor, e como gerenciar sua área de trabalho. Aprenderemos, basicamente, algumas formas de criar e remover um objeto (no caso um vetor), como verificar suas propriedades e alterar seus elementos. Ao final veremos como salvar e carregar sua área de trabalho e/ou objetos específicos.

Objetos são apenas "nomes" que você dá ao resultado de determinada tarefa que o `R`tenha desempenhado. Estes nomes são dados por meio de um operador de assignação (assignement operator), que podem ser `<-` ou `=`. A definição (ou assignação) de um objeto é feita assim: `nome <- "objeto"`. Para imprimir um objeto basta digitar seu nome em numa nova linha.

*** =instructions

Crie os seguintes objetos:

* Defina **x** como 100 usando `<-`
* Defina **pais** como  "Brasil" (não esqueça das aspas) usando `=`

E então imprima-os:

* Imprima **x**
* Imprima **pais**

*** =hint

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Defina x como 100 usando `<-`

# Defina pais como  "Brasil" (não esqueça das aspas) usando `=`

# Imprima x

# Imprima pais

```

*** =solution
```{r}
# Defina x como 100. Use `<-`
x <- 100
# Defina pais como  "Brasil" usando `=` (não esqueça das aspas)
pais = "Brasil"
# Imprima x
x
# Imprima pais
pais
```

*** =sct
```{r}
test_student_typed("x <- 100", not_typed_msg = "Verifique o valor que atribuiu a `x`?")
test_student_typed('pais = "Brasil"', not_typed_msg = "Tem certeza de que digitou corretamente o `pais`?")
test_output_contains('100', incorrect_msg = "Lembre de imprimir `x`")
test_output_contains('"Brasil"', incorrect_msg = "Lembre de imprimir `pais`")

```


--- type:NormalExercise lang:r xp:100 skills:1 key:6b51fb04d2
## Criando vetores

As variáveis criadas no `R`não precisam ter apenas um valor. Na verdade elas costumarão ter inúmeros valores. Para unir diversos valores em uma única variável, basta concatenar eles por meio da função `c()`.

Por exemplo `num <- c(10, 20, 30)` ou ainda `txt <- c("vetor", "de", "textos")`. Desta forma você pode criar vetores de todos os tipos de variáveis e com o tamanho que desejar.


*** =instructions

Vamos criar um vetor para cada tipo básico de dado:

* Defina **numero** contendo 10, 20 e 30
* Defina **inteiro**: contendo 5L, 10L e 15L
* Defina **texto** contendo os elementos "vetor", "de" e "textos"
* Defina **logico** com TRUE, FALSE e NA

*** =hint
Lembre-se que um objeto é criado com o operador `<-`. Exemplo: `logico <- c(TRUE, FALSE, NA)`.

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# crie o vetor numero


# Crie um vetor de inteiros. Nao esqueca do L


# Crie um vetor de texto. Nao esqueca dos aspas


# Crie um vetor logico. Os valores precisam ser maiúsculos


```

*** =solution
```{r}
# crie o vetor numero
numero <- c(10, 20, 30)

# Crie um vetor de inteiros. Nao esqueca do L
inteiro <- c(5L, 10L, 15L) 

# Crie um vetor de texto. Nao esqueca dos aspas
texto <- c("vetor", "de", "textos")

# Crie um vetor logico. Os valores precisam ser maiúsculos
logico <- c(TRUE, FALSE, NA)

```

*** =sct
```{r}
test_object("numero")
test_object("inteiro")
test_object("texto")
test_object("logico")

success_msg("Parabens! Agora vamos conhecer um pouco mais sobre os tipos dos dados")
```
