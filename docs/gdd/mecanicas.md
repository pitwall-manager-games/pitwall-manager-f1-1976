# Mecánicas de Juego

## El Motor de Simulación (Game Loop)

- El bucle se gestiona en `app.js` mediante un temporizador asíncrono
- Cada monoplaza posee un porcentaje de progreso de vuelta (0 % a 100 %)
- Al llegar al 100 %, completa una vuelta, se suma al contador global y se
  recalculan los tiempos
- Los tiempos, posiciones y datos de piloto (estrés, cansancio, desgaste) solo
  se actualizan en la interfaz cuando un monoplaza cruza la línea de meta,
  reflejando la falta de telemetría en tiempo real de la temporada 1976

## Variables de los Pilotos del Jugador

El usuario gestiona dos monoplazas independientes con las siguientes métricas:

### Ritmo

| Valor | Comportamiento |
|-------|----------------|
| Ataque | Intentar adelantar siempre que sea posible |
| Normal | Conducción de carrera estándar |
| Defender | Defender la posición frente a ataques rivales |
| Conservar | Bajar el ritmo para reducir el estrés del piloto |

### Modo Motor

| Modo | Velocidad | Consumo |
|------|-----------|---------|
| Alto rendimiento | Máxima | Máximo |
| Normal | Equilibrada | Equilibrado |
| Ahorro | Reducida | Reducido |

### Empuje (Push)

(Gestionado en `fiabilidad-mecanica.md`)

### Degradación de Neumáticos

(Gestionado en `neumaticos.md`)

### Combustible

(Gestionado en `combustible.md`)

### Estrés

- Aumenta cuando el piloto está atacando o defendiendo
- Disminuye cuando el ritmo es bajo (Conservar)
- Afecta al rendimiento del piloto
- Se recupera durante la carrera

### Cansancio

- Aumenta en las mismas situaciones que el estrés
- No se recupera durante la carrera
- Afecta al rendimiento del piloto
- No afecta al delay de órdenes (no hay radio en 1976)
