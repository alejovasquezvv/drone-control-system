# CyberLogistics X-2026

Prototipo de un sistema de monitoreo y gestión de drones autónomos para distribución urbana (caso académico, Ingeniería de Requisitos y Calidad de Software).

## Funcionalidades del prototipo
- RF-01: alerta cuando la batería de un dron baja del 20 %.
- RF-02: registro de pérdida de telemetría superior a 8 s.
- RF-03 / RF-06: PIN dinámico y registro de confirmación de entrega.
- RF-04: porcentaje de batería visible en el mapa de seguimiento.
- RF-08: bloqueo de autorización de despegue con alerta crítica abierta.

## Tecnologías
HTML5, CSS3 y JavaScript (sin dependencias).

## Cómo ejecutarlo
1. Clonar: `git clone https://github.com/alejovasquezvv/cyberlogistics-x2026.git`
2. Abrir `index.html` en un navegador moderno (Chrome, Edge o Firefox).
3. Pulsar «Simular batería baja» para ver la alerta del RF-01.

## Ramas
`main` (estable), `develop` (integración), `feature/alertas-bateria` (RF-01).

## Autor
Alejandro Vásquez Valencia · Ingeniería Informática
