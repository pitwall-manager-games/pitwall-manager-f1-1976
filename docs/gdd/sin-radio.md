# Sin Radio — Comunicaciones en 1976

## Contexto

En la temporada 1976, las comunicaciones por radio entre el muro de boxes y
el piloto eran prácticamente inexistentes. Los equipos se comunicaban mediante
carteles (pit board) mostrados al piloto cuando cruzaba la línea de meta.

## Implicaciones en el Diseño del Juego

- **Sin delay por cansancio:** No existe latencia de comunicación por radio.
  El cansancio solo afecta al rendimiento en pista, no a la transmisión de órdenes.
- **Órdenes por vuelta:** Las instrucciones solo se pueden transmitir al
  completar una vuelta.
- **Información limitada:** El jugador no conoce el estado exacto del coche
  hasta que el piloto pasa por meta.

## Flujo de Comunicación

1. El jugador marca órdenes en la interfaz (ritmo, empuje, llamada a boxes, etc.)
2. Las órdenes quedan en estado "pendiente"
3. Cuando el piloto cruza la línea de meta, vé el cartel del equipo
4. Todas las órdenes pendientes se ejecutan simultáneamente

## Contraste con F1 2000

| Aspecto | F1 2000 | F1 1976 |
|---------|---------|---------|
| Canal | Radio | Cartel en meta |
| Frecuencia | Continua (con delay) | Cada vuelta |
| Delay por cansancio | Sí | No |
| Feedback | Tiempo real (con latencia) | Solo al cruzar meta |
