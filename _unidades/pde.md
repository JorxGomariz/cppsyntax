---
title: "5. Programación Dirigida por Eventos"
order: 5
layout: default
---

# **5. Programación Dirigida por Eventos**
En el .h y .cc
```cpp
// Biblioteca
#include <boost/signals2.hpp>

// Definición del tipo de señal
using my_signal_t = boost::signals2::signal<void(Tipo)>;

// === Definición de la señal ===
// Si no está en una clase...
my_signal_t &get_signal(){
    static my_signal_t s;
    return s
}

// Si está en una clase...
// En los atributos, estará definida la señal:
private:
    my_signal_t signal;
// Por tanto, habrá un método que retorne la señal pero no hará falta crearla
my_signal_t &Clase::get_signal(){
    return signal;
}

// Uso
get_signal()(argumento);
```
En el main...
```cpp
// Mensaje de la alerta
void alerta(Tipo arg) {
  // ...
}

// Conectamos la señal a la alerta
get_signal().connect(alerta);
``