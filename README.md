# Taller-Ingenieria-Requisitos
**ACTIVIDAD:** Fragmentación de un requisito caótico

## Introducción
En este taller se analiza un requisito expresado de forma informal por un cliente. A partir de este, se identifican los requisitos no funcionales, se redactan historias de usuario y se establecen criterios de aceptación utilizando el formato Gherkin, con el objetivo de transformar una necesidad del cliente en documentación técnica clara.

## 1. Requisitos No Funcionales

### RNF-01: Seguridad de la información

El sistema deberá proteger la información de los choferes y de los viajes mediante mecanismos de seguridad que eviten el acceso no autorizado a los datos.

### RNF-02: Rendimiento

El sistema deberá soportar al menos 1,000 usuarios conectados simultáneamente sin presentar bloqueos ni degradación significativa del rendimiento.

### RNF-03: Protección de datos

La información personal y la ubicación de los choferes deberán almacenarse y transmitirse de forma segura para evitar su exposición o manipulación por terceros.

## 2. Historia de Usuario 1

**ID:** HU-01

**Como** chofer,

**Quiero** visualizar los viajes cercanos en tiempo real,

**Para** seleccionar y aceptar el viaje que mejor se adapte a mi ubicación.

## 3. Criterios de aceptación (Gherkin)

**Escenario:** Visualizar viajes cercanos en tiempo real.

**Dado** que el chofer ha iniciado sesión en la aplicación,

**Cuando** existan viajes disponibles cerca de su ubicación,

**Entonces** el sistema mostrará los viajes cercanos en tiempo real para que el chofer pueda seleccionarlos.

## 4. Historia de Usuario 2

**ID:** HU-02

**Como** chofer,

**Quiero** recibir la ruta más corta cuando acepte un viaje,

**Para** reducir el tiempo de recorrido y ahorrar combustible.

## 5. Criterios de Aceptación (Gherkin)

**Escenario:** Mostrar la ruta más corta al aceptar un viaje.

**Dado** que el chofer ha aceptado un viaje,

**Cuando** el sistema confirme la aceptación,

**Entonces** mostrará automáticamente la ruta más corta hacia el destino para optimizar el tiempo de recorrido y el consumo de combustible.

## 6. Conclusión
La fragmentación de un requisito permite convertir una necesidad expresada por el cliente en especificaciones técnicas claras. Esto facilita la comunicación entre el cliente y el equipo de desarrollo, además de reducir ambigüedades durante la implementación del sistema.
