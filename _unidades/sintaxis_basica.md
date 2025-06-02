---
title: "Sintaxis básica"
layout: default
---

# **Sintaxis básica**

# Comentarios

```cpp
// Comentario de una línea
/*
    Comentario de
    varias líneas
*/
```

# Declaración y asignación de variables
```cpp
tipo var;           // Declaración de una variable
tipo var = valor;   // Declaración con inicialización
var = otro_valor;   // Asignación de una variable
```
Si se quiere una constante...
```cpp
const tipo varConstante = valor;
```

# Estructuras
```cpp
struct Estructura{
    tipo campo1;
    tipo campo2;
    // ...
}
```
Para crear una instancia...
```cpp
Estructura inst;
Estructura inst = {val1, val2};
