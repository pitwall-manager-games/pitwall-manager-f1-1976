# Pizarra (Pit Board) — Lógica del Cartel en Meta

## Funcionamiento

- El jugador puede marcar órdenes en cualquier momento durante la vuelta
- Las órdenes quedan en estado "pendiente" hasta que el piloto cruza la línea
  de meta, donde un cartel del equipo se las muestra
- Al cruzar la meta, todas las órdenes pendientes se ejecutan simultáneamente,
  simulando la lectura del cartel por parte del piloto

## Órdenes Disponibles

- Ritmo (Ataque, Normal, Defender, Conservar)
- Empuje (A fondo, Normal, Reservar)
- Llamada a boxes (con compuesto y carga de combustible)
- Modo motor (Alto rendimiento, Normal, Ahorro)

## Diferencias con el Sistema de Radio (F1 2000)

| Aspecto | F1 2000 (Radio) | F1 1976 (Pit Board) |
|---------|-----------------|---------------------|
| Instrucciones continuas | Sí, con delay | No |
| Ejecución | Asíncrona, según delay | Batch, al cruzar meta |
| Órdenes parciales | Se pueden cambiar vuelta a vuelta | Se acumulan y ejecutan juntas |
| Feedback del piloto | Por radio (con delay) | Visual (cartel) |

## Notas de Implementación

- El estado "pendiente" debe ser visible en la interfaz para que el jugador
  sepa qué órdenes están esperando ejecución
- Si el piloto no cruza la meta (abandono), las órdenes pendientes nunca se ejecutan
