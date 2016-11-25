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
Apenas aperte o botão "Submit" para começarmos o curso
*** =hint

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}

```

*** =solution
```{r}

```

*** =sct
```{r}

success_msg("Bora la!")
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
# You can also prepare your dataset in a specific way in the pre exercise code

library(MindOnStats)
data(Movies)
movie_selection <- Movies[Movies$Genre %in% c("action", "animated", "comedy"),c("Genre", "Rating", "Run")]

# Clean up the environment
rm(Movies)
```

*** =sample_code
```{r}
# movie_selection is available in your workspace

# Check out the structure of movie_selection


# Select movies that have a rating of 5 or higher: good_movies


# Plot Run (i.e. run time) on the x axis, Rating on the y axis, and set the color using Genre

```

*** =solution
```{r}
# movie_selection is available in your workspace

# Check out the structure of movie_selection
str(movie_selection)

# Select movies that have a rating of 5 or higher: good_movies
good_movies <- movie_selection[movie_selection$Rating >= 5, ]

# Plot Run (i.e. run time) on the x axis, Rating on the y axis, and set the color using Genre
plot(good_movies$Run, good_movies$Rating, col = good_movies$Genre)
```

*** =sct
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

test_function("str", args = "object",
              not_called_msg = "You didn't call `str()`!",
              incorrect_msg = "You didn't call `str(object = ...)` with the correct argument, `object`.")

test_object("good_movies")

test_function("plot", args = "x")
test_function("plot", args = "y")
test_function("plot", args = "col")

test_error()

success_msg("Good work!")
```
