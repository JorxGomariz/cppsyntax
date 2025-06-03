---
title: "8. Biblioteca Estándar de C++"
order: 8
layout: default
---

# **8. Biblioteca Estándar de C++**

# std::string
```cpp
// Biblioteca
#include <string>

// Ejemplo de uso
std::string s = "Hola";         // Inicializacion
s = s + " Mundo";               // Concatenacion
char c = s[0];                  // Acceso a caracter
std::string copia = s1;         // Se pueden asignar strings

// Funciones básicas
size_t longitud = s.size();     // Tamaño
bool vacia = s.empty();         // Está vacía
s.clear()                       // Deja la cadena vacía
size_t pos = s.find("Mu");      // Posición de la primera ocurrencia, o std::string::npos si no se encuentra
s.erase(5,6)                    // Borra 6 caracteres desde la posición 5
```

# std::vector
```cpp
// Biblioteca
#include <vector>

// Ejemplo de uso
std::vector<int> v(3,10);        // Vector de enteros de 3 elementos, cada uno con valor 10
int x = v[0]                     // Acceso a posición 0

// Funciones básicas
size_t tam = v.size();           // Tamaño del vector
bool vacio = v.empty();          // Está vacío
v.push_back(7);                  // Añade un 7 al final
v.pop_back();                    // Elimina el último elemento
v.insert(v.begin() + 1, 42);     // Inserta el 42 en la posición 1 (y desplaza el resto)
v.erase(v.begin());              // Elimina el primer elemento
int primero = v.front();         // Primer elemento
int ultimo = v.back();           // Último elemento
```
