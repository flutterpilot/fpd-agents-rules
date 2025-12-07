# Hug AI Orchestrated Architecture

Este documento describe una arquitectura basada en capas clásicas, influenciada por Clean Architecture, DDD, Service Layer y principios de separación estricta de responsabilidades. El objetivo es lograr una estructura de directorios que refleje con claridad la arquitectura, reduzca acoplamientos y facilite tanto el desarrollo humano como el asistido por IA.

---

## 1. Objetivos de la Arquitectura

- Estructura del proyecto que **refleja directamente la arquitectura**.
- Capas **independientes**, sin conocimiento mutuo.
- **Orquestación centralizada**: un único lugar donde se coordinan los casos de uso.
- Archivos pequeños, simples, específicos y reutilizables.
- Minimizar bugs en nuevas features.
- Maximizar claridad, mantenibilidad y escalabilidad.

---

## 2. Influencias y Fundamentos

Esta arquitectura combina elementos de:

- **Layered Architecture (n-tier)**: separación por capas técnicas.
- **Clean Architecture / Hexagonal / Onion**: dominio independiente, infraestructura como detalles.
- **Service Layer / Application Layer**: capa que orquesta casos de uso.
- **DDD (Domain-Driven Design)**: repositorios, reglas de dominio separadas.
- **Cross-cutting concerns**: logging, métricas, permisos y configuraciones transversales.

El resultado es una arquitectura **estrictamente orquestada**, donde cada capa es un "instrumento" y el orquestador es el "director" que coordina el flujo.

---

## 3. Capas de la Arquitectura

### 3.1 Domain
- Regla de negocio pura.
- Lógica independiente de UI, frameworks, datos o servicios.
- Define tipos, validaciones y comportamientos centrales.

### 3.2 State
- Maneja estado de la aplicación o de una feature.
- Exposición controlada para lectura/escritura.
- No contiene reglas de dominio.

### 3.3 Data
- Mapea y transforma datos externos.
- Repositorios que implementan interfaces usadas por Domain.
- No conoce UI, State o Navigation.

### 3.4 Services
- Acceso a infraestructura: HTTP, DB, almacenamiento, OS.
- No implementa lógica de negocio.
- Solo IO y detalle técnico.

### 3.5 Component
- Componentes de UI reutilizables.
- Sin dependencia de Domain/Data/Services.
- Render puro.

### 3.6 Style
- Tokens, temas, tipografías, espaciados.
- Estilos reutilizables.

### 3.7 Navigation
- Rutas, pantallas, flujos.
- No contiene reglas de negocio.

### 3.8 Cross-Cutting
- Logging, permisos, feature flags, métricas.
- Funcionalidades transversales.

### 3.9 Orchestration
- **La capa que hace que todo funcione junto**.
- Implementa casos de uso concretos.
- Coordina Domain, Data, Services, State, Navigation.
- Interactúa con Component solo a través de entradas/salidas.

---

## 4. Reglas de Dependencia

### 4.1 Quién importa a quién

```
component → orchestration
orchestration → domain
               → state
               → data
               → services
               → navigation
               → cross_cutting
               → style (si aplica)
```

### 4.2 Prohibiciones claves
- `domain` no importa nunca `services`, `data`, `state` o `component`.
- `services` no importa `data`.
- `state` no importa UI.
- `component` no importa `data` ni `services`.
- **Toda integración entre capas pasa por Orchestration**.

---

## 5. Estructura de Directorios

Ejemplo base:

```
lib/
  domain/
  state/
  data/
  services/
  component/
  style/
  navigation/
  cross_cutting/
  orchestration/
```

Cada carpeta contiene solo archivos especializados y pequeños.

---

## 6. Flujo de un Caso de Uso

Ejemplo: "Enviar notificación a todos los usuarios".

### Secuencia
1. Un componente UI dispara un evento.
2. Ese evento llama a un archivo en `orchestration/`.
3. El orquestador:
   - valida reglas en `domain/`,
   - obtiene o prepara datos en `data/`,
   - ejecuta IO en `services/`,
   - actualiza `state/`,
   - registra logs en `cross_cutting/`,
   - opcionalmente redirige usando `navigation/`.
4. La UI reacciona únicamente al estado o al resultado devuelto.

### Ventaja
- Las capas nunca se mezclan.
- El flujo siempre está en un solo archivo.

---

## 7. Beneficios de Esta Arquitectura

- **Claridad total**: el proyecto es autoexplicativo.
- **Menos bugs**: cada capa hace solo una cosa.
- **Testeo sencillo**: las capas son pequeñas y aisladas.
- **Refactorización limpia**: la orquestación centraliza cambios.
- **Escalabilidad real**: agregar features no rompe el core.
- **Alta compatibilidad con desarrollo asistido por IA**.

---

## 8. ¿Por Qué Funciona Bien con IA?

- La arquitectura está codificada en la estructura de carpetas.
- Patrones repetibles fáciles de entender para modelos.
- Archivos pequeños y funciones predecibles.
- Reglas de dependencia claras.
- Generación automática de nuevas features siguiendo el patrón.

---

## 9. Conclusión

Esta propuesta combina múltiples principios probados (Clean Architecture, DDD, Service Layer, Cross-Cutting, Layered Architecture) en una implementación **estricta, clara y 100% visible en la estructura del proyecto**. El resultado es una arquitectura que minimiza el acoplamiento, maximiza la claridad y permite desarrollar nuevas funcionalidades de manera consistente, segura y compatible con automatización mediante IA.

