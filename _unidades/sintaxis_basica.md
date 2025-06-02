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

# Punteros
*Un puntero es una variable que almacena la dirección en memoria de otra variable cuyo tipo es compatible*

Declaración de puntero:
```cpp
tipo* ptr;
tipo *ptr; // Equivalente
```
Asignación de dirección:
```cpp
tipo var = valor;
tipo* ptr = &var;
```
Acceso al contenido:
```cpp
// ptr es la dirección de memoria y *ptr es el valor almacenado en la dirección de memoria
tipo dato = *ptr;
*ptr = otro_valor;  // modifica el contenido
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
Estructura instancia;
Estructura instancia = {valor1, valor2};
```
Para acceder a los miembros del struct...
```cpp
instancia.campo1 = valor;
tipo var = instancia.campo2;
```
Si la instancia es un puntero...
```cpp


