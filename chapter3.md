---
title       : Propriedade dos vetores
description : Conhecendo o tamanho, tipo, estrutura e nomes 

--- type:NormalExercise lang:r xp:100 skills:1 key:0001083ccf
## Tipos de dados

Quando você começar a manipular os dados vai verificar que eles são guardados de diferças formas: alguns são valores numéricos (renda de uma família), outros são texto (como tuítes feitos com a '#foraTemer'), ou variáveis categóricas armazenadas como texto (se uma instituição é "pública" ou "privada"), ou ainda vetores lógicos (que não serão comuns em bases de dados, mas você precisará criá-los e manipulá-los com desenvoltura para selecionar os dados que deseja).

*** =instructions
Os vetores que você criou no último exercício estão em sua área de trabalho. Verifique a classe de cada um deles com a função `class()`.

*** =hint

*** =pre_exercise_code
```{r}
numero <- c(10, 20, 30)
inteiro <- c(5L, 10L, 15L) 
texto <- c("vetor", "de", "textos")
logico <- c(TRUE, FALSE, NA)
```

*** =sample_code
```{r}
# verifique a classe de numero

# verifique a classe de inteiro

# verifique a classe de texto

# Verifique a classe de logico

```

*** =solution
```{r}
# verifique a classe de numero
class(numero)
# verifique a classe de inteiro
class(inteiro)
# verifique a classe de texto
class(texto)
# Verifique a classe de logico
class(logico)
```

*** =sct
```{r}
test_student_typed("class(numero)")
test_student_typed("class(inteiro)")
test_student_typed("class(texto)")
test_student_typed("class(logico)")
success_msg("Muito bem!! Leia a classe de cada um dos objetos no console.")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:2441711488
## Família "é?"


*** =instructions

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

```

--- type:NormalExercise lang:r xp:100 skills:1 key:b34afae546
## Família como 


*** =instructions

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

```

--- type:NormalExercise lang:r xp:100 skills:1 key:5fb49ba2a9
## Tamanho


*** =instructions

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

```

--- type:NormalExercise lang:r xp:100 skills:1 key:c06c1d8c80
## Estrutura 


*** =instructions

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

```
