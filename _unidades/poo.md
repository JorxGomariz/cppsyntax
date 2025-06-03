---
title: "3. Programación Orientada a Objetos"
order: 3
layout: default
---

# **3. Programación Orientada a Objetos**

# Definición de una clase genérica
En el .h
```cpp
#ifndef CLASE_H
#define CLASE_H

#include "archivoNecesario.h"

// Clase base
class ClaseBase{
public:
    // Constructor por defecto
    ClaseBase();

    // Constructor con parámetros
    ClaseBase(tipo parametro);

    // Destructor virtual (para permitir herencia polimórfica)
    virtual ~ClaseBase();

    // Método virtual normal
    virtual tipo metodoVirtual(tipo x);

    // Método puramente abstracto (genera clase abstracta)
    virtual tipo metodoPuro(tipo y) = 0;

protected:
    tipo atributoProtegido;         // Solo accesible en derivadas
private:
    tipo atributoPrivado;           // Solo accesible dentro de esta clase
}

// Clase derivada que hereda públicamente de ClaseBase
// Nota: override indica que se va a sobreescribir el método de la clase base (no obligatorio, pero recomendable)
class ClaseDerivada : public ClaseBase {
public:
    // Constructor de ClaseDerivada (llama a ClaseBase en lista de inicializacion)
    ClaseDerivada(tipo valorBase, tipo valorDerivado);

    // Destructor
    ~ClaseDerivada() override;

    // Sobreescritora de método virtual
    tipo metodoVirtual(tipo x) override;

    // Implementación de método puro
    tipo metodoPuro(tipo y) override;

    // Atributo estático
    static Tipo atributoEstatico;

private:
    atributoDerivado;
}

#endif // CLASE_H
```

En el .cc