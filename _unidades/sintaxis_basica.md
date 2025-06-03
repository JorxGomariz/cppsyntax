---
title: "1. Sintaxis básica"
order: 1
layout: default
---

# **1. Sintaxis básica**

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
Para vectores y matrices...
```cpp
// Vector
tipo vec[tam];
vec[i] = valor;
// Matriz
tipo mat[fil][col];
mat[i][j] = valor;
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
tipo* ptr = &var; // & extrae la dirección de memoria de la variable
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

# Funciones
Paso por valor:
```cpp
tipo funcionValor(tipo parametro){
    parametro = otro_valor;     // El parámetro no cambia fuera de la función (copia local)
    return parametro;
}
funcionValor(var);              // var no se ha modificado
```
Paso por referencia:
```cpp
void funcionRef(tipo& parametro){
    parametro = otro_valor;     // El parámetro cambia fuera de la función
}
funcionRef(var)                    // var se ha modificado
```

# Condicionales
if:
```cpp
if (condicion1){
    // Codigo 1
}
else if (condicion2){
    // Codigo 2
}
else {
    // Codigo else
}
```
switch:
```cpp
switch (expresion){
    case valor1:        // if expresion == valor1
        // Codigo 1
        break;
    case valor2:
        // Codigo 2
        break;
    // ...
    default:
        // Codigo default
        break;
}
```

# Bucles
while:
```cpp
while (condicion){
    // Bloque que se repite mientras la condicion sea verdadera
}
```
do-while:
```cpp
do {
    // Bloque que se ejecuta al menos una vez
} while (condicion);
```
for:
```cpp
// Clásico:
for (tipo i = inicio; i < fin; i++){
    // Bloque que se repite (inicialización; condición; actualización)
}
// Moderno:
for (auto elemento : contenedor){
    // Bloque que recorre cada elemento del contenedor
}
```

# Estructura de un programa genérico
```cpp
// Archivos de cabecera y bibliotecas
#include <biblioteca>

// Declaración de funciones y variables globales
tipo funcion(tipo parametro);

// Programa principal
int main(){
    // Implementacion
    return 0; // Retorna éxito
}

// Definición de funciones
tipo funcion(tipo parametro){
    // Implementacion
}
```