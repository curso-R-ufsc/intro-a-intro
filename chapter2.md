---
title       : Tipos de dados
description : Números, caracteres e lógicos
--- type:NormalExercise lang:r xp:100 skills:1 key:e83dac591d
## Objetos

Nesta capítulo veremos um pouco sobre o objeto mais básico do R, o vetor, e como gerenciar sua área de trabalho. Aprenderemos, basicamente, algumas formas de criar e remover um objeto (no caso um vetor), como verificar suas propriedades e alterar seus elementos. Ao final veremos como salvar e carregar sua área de trabalho e/ou objetos específicos.

Objetos são apenas "nomes" que você dá ao resultado de determinada tarefa que o `R`tenha desempenhado. Estes nomes são dados por meio de um operador de assignação (assignement operator), que podem ser `<-` ou `=`. A definição (ou assignação) de um objeto é feita assim: `nome <- "objeto"`. Para imprimir um objeto basta digitar seu nome em numa nova linha.

*** =instructions

Crie os seguintes objetos:

* Defina **x** como 100 usando `<-`
* Defina **pais** como  "Brasil" (não esqueça das aspas) usando `=`

E então imprima
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
# Defina x como 100 usando `<-`
x <- 100
# Defina pais como  "Brasil" (não esqueça das aspas) usando `=`
pais = "Brasil"
# Imprima x
x
# Imprima pais
pais
```

*** =sct
```{r}
test_object("x")
test_object("pais")
test_function("<-")
test_function("=")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:5d0ebb9c4c
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
