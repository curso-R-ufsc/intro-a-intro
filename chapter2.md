---
title       : Tipos de dados
description : Números, caracteres e lógicos



?



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
test_student_typed('pais <- "Brasil"', not_typed_msg = "Tem certeza de que digitou corretamente o `pais`?")
test_output_contains('100', incorrect_msg = "Lembre de imprimir `x`")
test_output_contains('"Brasil"', incorrect_msg = "Lembre de imprimir `pais`")

```


--- type:NormalExercise lang:r xp:100 skills:1 key:6b51fb04d2
## Criando vetores

As variáveis criadas no `R`não precisam ter apenas um valor. Na verdade elas costumarão ter inúmeros valores. Para unir diversos valores em uma única variável, basta concatenar eles por meio da função `c()`. Por exemplo `num <- c(10, 20, 30)` ou ainda `txt <- c("vetor", "de", "textos")`. Desta forma você pode criar vetores de todos os tipos de variáveis e com o tamanho que desejar.


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


--- type:NormalExercise lang:r xp:100 skills:1 key:0001083ccf
## Tipos de dados

Quando você começar a manipular os dados vai verificar que eles são guardados de diferças formas: alguns são valores numéricos (renda de uma família), outros são texto (como tuítes feitos com a '#foraTemer'), ou variáveis categóricas armazenadas como texto (se uma instituição é "pública" ou "privada"), ou ainda vetores lógicos (que não serão comuns em bases de dados, mas você precisará criá-los e manipulá-los com desenvoltura para selecionar os dados que deseja).

*** =instructions

*** =hint

*** =pre_exercise_code
```{r}
classes <- factor("Burguesia", "Proleta")
logico <- c(TRUE, FALSE, NA)
```

*** =sample_code
```{r}
# verifique a classe de 24

# verifique a classe de 14L

# verifique a classe de "Um texto"

# verifique a classe de classes

# Verifique a classe de logico

```

*** =solution
```{r}

```

*** =sct
```{r}
test_student_typed("class(24)")
test_student_typed("class(24)")
test_student_typed("class(24)")
test_student_typed("class(classes)")
test_student_typed("class(logico)")

```
