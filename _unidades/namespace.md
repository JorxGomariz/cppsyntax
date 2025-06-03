---
title: "3. Namespaces"
order: 3
layout: default
---

# **3. Namespaces**

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