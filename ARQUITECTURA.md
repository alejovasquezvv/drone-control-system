# Arquitectura de CyberLogistics X-2026

Diagrama de componentes del prototipo v0.1.0 (implementado) y del sistema objetivo (diseño).

```mermaid
flowchart LR
  subgraph P["Prototipo v0.1.0 (implementado)"]
    OP["Operador del centro de control"] --> UI["index.html: panel de flota, mapa y registro de eventos"]
    UI --> SIM["Simulación en JavaScript: batería, telemetría y PIN"]
    SIM --> AL["Alerta crítica y bloqueo de despegue (RF-01, RF-08)"]
  end
  subgraph S["Sistema objetivo (diseño)"]
    D["Drones autónomos"] -->|"Telemetría (MQTT sobre TLS)"| T["Telemetry-Ingestion Engine"]
    T --> M["Fleet-Monitoring & Alerting Service"]
    M --> C["Centro de control"]
    C --> X["Drone-Control Command Dispatcher"]
    X -->|"Comandos cifrados TLS 1.2 o superior"| D
  end
```

## Componentes

| Componente | Estado | Requisito |
|---|---|---|
| Panel de flota y mapa | Implementado | RF-01, RF-04 |
| Registro de eventos de telemetría | Implementado (simulado) | RF-02 |
| PIN dinámico de entrega | Implementado (simulado) | RF-03, RF-06 |
| Bloqueo de despegue | Implementado | RF-08 |
| Telemetry-Ingestion Engine | Diseño | RNF-01 |
| Drone-Control Command Dispatcher | Diseño | RNF-02 |
| Fleet-Monitoring & Alerting Service | Diseño | RNF-04 |
