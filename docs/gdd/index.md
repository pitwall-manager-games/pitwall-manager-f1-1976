# GDD — Pitwall Manager: F1 1976

## 1. Visión General

- **Título Definitivo:** Pitwall Manager: F1 1976
- **Género:** Estrategia / Gestión Deportiva en Tiempo Real
- **Rol del Jugador:** Director de Equipo (Team Principal / Jefe de Estrategia)
- **Plataforma:** Navegadores Web (Escritorio)
- **Tecnologías:** HTML5, CSS3, JavaScript Vanilla (ES6 Modules)
- **Ambientación:** Temporada 1976 — la cúspide de la F1 clásica. Motores V8,
  V12 y flat-12 atmosféricos, sin asistencias electrónicas ni DRS, telemetría
  escasa o nula. No hay comunicaciones por radio: las órdenes del equipo se
  transmiten al piloto mediante carteles en la línea de meta y los datos de
  carrera solo se conocen al completar cada vuelta.

## 2. Pilares de Diseño

- **Presión en el Muro de Boxes:** Decisiones estratégicas basadas en datos
  limitados — la información solo llega cuando el piloto cruza la meta.
- **Gestión de Recursos Críticos:** Controlar el ritmo para equilibrar velocidad,
  degradación de neumáticos y consumo de combustible.
- **Estética de Ingeniería:** Interfaz de alto contraste y modo oscuro que emula
  las pantallas de cronometraje y datos de la F1 de los 70.

## 3. Estructura del Proyecto

```
pitwall-manager-f1-1976/
├── docs/gdd/                    # Documentación de diseño
│   ├── index.md                 # Este documento
│   ├── fiabilidad-mecanica.md   # Fiabilidad de los 70 y variable Empuje
│   ├── sin-radio.md             # Ausencia de comunicaciones por radio
│   ├── pizarra-pit-board.md     # Lógica del cartel en meta
│   ├── combustible.md           # Sistema de combustible
│   ├── neumaticos.md            # Compuestos, degradación y pit stop
│   ├── mecanicas.md             # Game loop y variables del piloto
│   ├── ia.md                    # Inteligencia artificial rival
│   ├── clima.md                 # Clima dinámico
│   ├── ui-ux.md                 # Interfaz de usuario y wireframes
│   └── progresion.md            # Condiciones de victoria y progresión
├── src/
│   ├── index.html
│   ├── css/style.css
│   └── js/
│       ├── app.js               # Inicializador y bucle principal
│       ├── track.js             # Canvas 2D del circuito
│       └── physics.js           # Fórmulas de simulación
├── AGENTS.md
└── package.json
```

## 4. Documentación Relacionada

- [Visión general de la saga](../../../docs/GDD_Saga.md) — contexto de la franquicia.
