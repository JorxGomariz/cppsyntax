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
using signal_t = boost::signals2::signal<void(Tipo)>;

// === Definición de la señal ===
// Si no está en una clase...
signal_t &get_signal(){
    static signal_t s;       // Nos toca crear la señal (static)
    return s
}

// Si está en una clase...
// En los atributos, estará definida la señal:
private:
    signal_t s;
// Por tanto, habrá un método que retorne la señal pero no hará falta crearla
signal_t &Clase::get_signal(){
    return s;
}

// Uso
get_signal()(arg);
```
En el main...
```cpp
// Mensaje de la alerta
void alerta(Tipo arg) {
  // ...
}

// Conectamos la señal a la alerta
get_signal().connect(alerta);
```