---
title: "2. Reserva y liberación de memoria"
layout: default
---

# **2. Reserva y liberación de memoria**

# Variables
```cpp
// Reserva
tipo* var = new tipo;
tipo* var = new tipo(valor_inicial); // Inicializa con un valor
// Uso
*var = valor;
// Liberación
delete var;
```

# Objetos
```cpp
// Reserva
tipo* obj = new tipo (arg1, arg2);
// Uso
obj->metodo();
obj->atributo = valor;
// Liberación
delete obj;
```

# Vector
```cpp
// Reserva
tipo* vec = new tipo[tam]
// Uso
vec[i] = valor;     // Equivalente a *(vec + i) = valor
// Liberación
delete[] vec;
```

# Matriz
```cpp
// Reserva
tipo** mat = new tipo*[fil];
for (int i = 0; i < fil; i++) {
   mat[i] = new tipo[col];
}
// Uso
mat[i][j] = valor;
// Liberación
for (int i = 0; i < fil; i++) {
   delete[] mat[i];
}
delete[] mat;
```