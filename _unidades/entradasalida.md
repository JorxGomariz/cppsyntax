---
title: "7. Entrada/Salida en C++"
order: 7
layout: default
---

# **7. Entrada/Salida en C++**

# Redefinición del operador <<
En el .h \
*Nota 1: friend permite acceder a los miembros protegidos y privados de la clase.* \
*Nota 2: También se podría haber hecho sin friend, usando los getters* \
*Nota 3: Dado que obj es const, si hay que acceder a sus métodos ( obj.metodo() ), esos métodos deben ser const*
```cpp
#include <iostream>
friend std::ostream& operator<<(std::ostream& os, const Clase& obj);
```

En el .cc
```cpp
std::ostream& operator<<(std::ostream& os, const Clase& obj) {
    // Aquí escribir lo que quieras en el stream, p. ej.:
    os << obj.atributo;  
    return os;
}
```