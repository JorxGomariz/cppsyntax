---
title: "4. Programación Orientada a Objetos"
order: 4
layout: default
---

# **4. Programación Orientada a Objetos**

# Definición de una clase genérica
Clase.h
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

    // Método normal de la clase base
    tipo metodoBase(tipo x);

    // Método virtual
    virtual tipo metodoVirtual(tipo x);

    // Método abstracto (no se implementa en la clase base)
    virtual tipo metodoPuro(tipo x) = 0;

protected:
    tipo atributoProtegido;         // Solo accesible en derivadas
private:
    tipo atributoPrivado;           // Solo accesible dentro de esta clase
};

// Clase derivada que hereda públicamente de ClaseBase
// Nota: override indica que se va a sobreescribir el método de la clase base (no obligatorio, pero recomendable)
class ClaseDerivada : public ClaseBase {
public:
    // Constructor de ClaseDerivada (llama a ClaseBase en lista de inicializacion)
    ClaseDerivada(tipo valorBase, tipo valorDerivado);

    // Destructor
    ~ClaseDerivada() override;

    // Metodo normal de la clase derivada
    tipo metodoDerivada(tipo x);

    // Sobreescritora de método virtual
    tipo metodoVirtual(tipo x) override;

    // Implementación de método puro
    tipo metodoPuro(tipo y) override;

    // Atributo estático
    static Tipo atributoEstatico;

private:
    atributoDerivada;
};

#endif // CLASE_H
```

Clase.cc
```cpp
#include "Clase.h"

// ======= Implementació de ClaseBase ========

// Constructor por defecto
ClaseBase::ClaseBase() : atributoProtegido(), atributoPrivado(){
    // ...
}

// Constructor con parámetros
ClaseBase::ClaseBase(tipo parametro) : atributoProtegido(parametro), atributoPrivado(parametro){
    // ...
}

// Destructor virtual
ClaseBase::~ClaseBase(){
    // ...
}

// Método normal de la clase base
tipo ClaseBase::metodoBase(tipo x){
    // Implementacion, por ejemplo:
    atributoPrivado = x;
}

// Método virtual
tipo ClaseBase::metodoVirtual(tipo x){
    // Implementacion
}

// ======== Implementación de ClaseDerivada =========

// Atributo estático
tipo ClaseDerivada::atributoEstatico = valor;

// Constructor (lista de inicialización de la base y de sus propios miembros)
ClaseDerivada::ClaseDerivada(tipo valorBase, tipo valorDerivado) : ClaseBase(valorBase), atributoDerivada(valorDerivado){
    // ...
}

// Destructor
ClaseDerivada::~ClaseDerivada(){
    // ...
}

// Método normal de la clase derivada
tipo ClaseDerivada::metodoDerivada(tipo x){
    // Implementacion, por ejemplo:
    atributoProtegido = atributoDerivada;   // Se puede acceder al protegido de la clase base. Si se llama igual que un atributo de la clase derivada... ClaseBase::atributoProtegido
    metodoBase(x);                          // Se puede llamar a un método de la clase base. Si se llama igual que un método de la clase derivada... ClaseBase::metodoBase(x)
}

// Override de método virtual
tipo ClaseDerivada::metodoVirtual(tipo x){
    // Nueva implementacion
}

// Implementación del método puro
tipo ClaseDerivada::metodoPuro(tipo x){
    // Implementacion
}
```

En el main...
```cpp
// Sin memoria dinámica
ClaseDerivada obj(valorBase, valorDerivada);

// Con memoria dinámica
ClaseDerivada* ptrObjDerivada = new ClaseDerivada();        // Puede usar todos los métodos público de la base
ClaseBase*     ptrObjBase     = new ClaseDerivada();        // Solo puede usar los métodos declarados en la base. Si se llama a un método virtual, se ejecuta la versión de la derivada
delete ptrObjDerivada;
delete ptrObjBase;
```