---
title: "4. Namespaces"
order: 4
layout: default
---

# **4. Namespaces**

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