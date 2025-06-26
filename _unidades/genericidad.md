---
title: "6. Genericidad"
order: 6
layout: default
---

# **6. Genericidad**

# Plantilla de función
```cpp
template <typename T>
T funcionGenerica(T valor){
    // Implementacion
    return valor;
}

tipo x = funcionGenerica<tipo>(valor);
```

# Plantilla de clase
```cpp
template <typename T>
class ClaseGenerica {
public:
    // Por ejemplo, constructor genérico
    ClaseGenerica(T valor) : atributoGenerico(valor){
        // ...
    }
private:
    // Por ejemplo, atributo genérico
    T atributoGenerico
};

ClaseGenerica<tipo> obj(valor);
```

# Parámetros de un template
A un template se pueden le pasar varios tipos genéricos, así como otras cosas como enteros, cadenas...
```cpp
template <typename T, tipo N> 
struct Estructura {
  T funcionGenerica[N];
};

Estructura<tipo,valor> estr;
```
También valores por defecto
```cpp
template <typename T=tipo, tipo N=valor> 
struct Estructura {
  T funcionGenerica[N];
};

Estructura<> estr;
```

# Archivos .h y .tcc
En el .h
```cpp
#ifndef CLASEGENERICA_H
#define CLASEGENERICA_H

#include <bibliotecas>

namespace Genericidad {
template <typename T, tipo N>
class ClaseGenerica {
 public:
  ClaseGenerica();
  T funcionGenerica(T arg);
  ...
 private:
  T data[N];
  ...
};
}  // namespace Genericidad
#include "clasegenerica.tcc"  // MUY IMPORTANTE
#endif /*CLASEGENERICA_H*/
```
En el .tcc
```cpp
#include "clasegenerica.h"
namespace Genericidad
{
  template <typename T, tipo N>
	ClaseGenerica<T, N>::ClaseGenerica() : ... {}

  template <typename T, int16_t N>
	T ClaseGenerica<T, N>::funcionGenerica(T arg) {
		...
	}

  ...

}