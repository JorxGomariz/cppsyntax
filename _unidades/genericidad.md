---
title: "6. Genericidad"
order: 6
layout: default
---

# **6. Genericidad**
# Archivos .h y .tcc
En el .h
```cpp
#ifndef CLASEGENERICA_H
#define CLASEGENERICA_H

#include <bibliotecas>

namespace Genericidad {
template <typename T=tipoPorDefecto, tipo N=valorPorDefecto>
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
``