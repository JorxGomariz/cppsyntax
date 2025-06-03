---
title: "3. Espacios de nombres"
order: 3
layout: default
---

# **3. Espacios de nombres**

# Declaración
```cpp
namespace Espacio{
    // Implementación de clases, funciones,...
    void funcion();
}
```

# Uso
```cpp
// Sin using
Espacio::funcion();
// Con using: se puede usar directamente (Cuidado!)
using namespace Espacio;
funcion();
```