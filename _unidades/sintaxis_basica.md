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
Asignación de dirección: \
*Nota: & extrae la dirección de memoria de la variable*
```cpp
tipo var = valor;
tipo* ptr = &var;
```
Acceso al contenido:
```cpp
// ptr es la dirección de memoria
ptr += n;           // Avanza n elementos del tipo
// *ptr es el valor almacenado en la dirección de memoria
*ptr = otro_valor;  // Modifica el contenido
```
Punteros nulos o sin inicializar:
```cpp
tipo* ptrNulo = nullptr;    // Literal puntero nulo
tipo* ptrSinInicializar;    // Cuidado! Apunta a donde sea
```

# Estructuras
```cpp
struct Estructura{
    tipo campo1;
    tipo campo2;
    tipo* campoPtr;
    // ...
};
```
Para crear una instancia...
```cpp
Estructura estr;
Estructura estr = {valor1, valor2, nullptr};
```
Para acceder a los miembros del struct...
```cpp
estr.campo1 = valor;
```
Con punteros...
```cpp
// Asignación de dirección
Estructura* ptrEstr = &estr;
// Acceso al contenido
ptrEstr->campo1 = valor;            // Equivale a (*ptrEst).campo1
ptrEst->campoPtr = &estr.campo1;    // campoPtr apunta al campo1 de estr.
```



