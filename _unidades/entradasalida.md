---
title: "7. Entrada/Salida en C++"
order: 7
layout: default
---

# **7. Entrada/Salida en C++**

# operator <<
En el .h \
*Nota: friend permite acceder a los miembros protegidos y privados de la clase.* \
*Ojo! También se podría haber hecho sin friend, usando los getters*
```cpp
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