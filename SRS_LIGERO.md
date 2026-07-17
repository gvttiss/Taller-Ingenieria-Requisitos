# Especificación de Requisitos de Software (SRS)
## Sistema Web de Control de Inventario

---

## 1. Alcance y Fronteras del Software

### 1.1 Propósito del sistema

El sistema tendrá como propósito permitir a una tienda local registrar y controlar sus productos mediante una plataforma web. La solución permitirá consultar las existencias y recibir alertas cuando la cantidad disponible de un producto sea baja.

El sistema estará orientado principalmente al control interno del inventario de la tienda.

### 1.2 Funcionalidades incluidas

El sistema deberá permitir:

- Registrar productos en el inventario.
- Consultar la información de los productos registrados.
- Controlar las existencias disponibles.
- Actualizar las cantidades de los productos.
- Validar los códigos de barras de los productos.
- Generar alertas cuando la cantidad de un producto sea igual o inferior al límite establecido como bajo inventario.

### 1.3 Fronteras del sistema

El sistema se limitará a la gestión del inventario de la tienda.

No formarán parte del alcance inicial:

- La gestión de pagos.
- La venta directa de productos al cliente.
- La administración de proveedores.
- La gestión de empleados.
- La generación de facturas electrónicas.

Estas funcionalidades podrían incorporarse posteriormente como ampliaciones del sistema.

---

## 2. Restricciones Técnicas Obligatorias

El desarrollo del sistema deberá cumplir con las siguientes restricciones técnicas:

### RT-01: Plataforma

El sistema deberá implementarse como una plataforma web accesible mediante un navegador.

### RT-02: Base de datos

El sistema deberá utilizar PostgreSQL como sistema gestor de base de datos, debido a que el servidor ya se encuentra configurado para esta tecnología.

### RT-03: Validación de códigos de barras

El sistema deberá validar los códigos de barras utilizados por los productos, verificando que cumplan con el formato correspondiente a los códigos de barras utilizados en El Salvador.

### RT-04: Control de existencias

El sistema deberá mantener actualizada la cantidad disponible de cada producto para evitar inconsistencias en el inventario.

---

## 3. Historias de Usuario

### HU-01: Registrar productos

**Como** encargado de la tienda,

**Quiero** registrar productos con su información y código de barras,

**Para** incorporarlos al sistema de inventario y poder controlar sus existencias.

#### Criterios de aceptación

**Escenario:** Registrar un producto con un código de barras válido.

**Dado** que el encargado se encuentra en el formulario de registro de productos,

**Cuando** ingrese la información requerida y un código de barras válido,

**Entonces** el sistema deberá registrar el producto en el inventario.

---

### HU-02: Controlar existencias

**Como** encargado de la tienda,

**Quiero** consultar y actualizar la cantidad disponible de cada producto,

**Para** mantener un control preciso de las existencias del inventario.

#### Criterios de aceptación

**Escenario:** Consultar las existencias de un producto.

**Dado** que el producto se encuentra registrado en el sistema,

**Cuando** el encargado consulte su información,

**Entonces** el sistema deberá mostrar la cantidad disponible del producto.

---

### HU-03: Recibir alertas de bajo inventario

**Como** encargado de la tienda,

**Quiero** recibir una alerta cuando queden pocas unidades de un producto,

**Para** identificar oportunamente los productos que necesitan ser reabastecidos.

#### Criterios de aceptación

**Escenario:** Detectar un producto con pocas unidades disponibles.

**Dado** que un producto se encuentra registrado en el inventario,

**Cuando** su cantidad disponible sea igual o inferior al límite mínimo establecido,

**Entonces** el sistema deberá mostrar una alerta de bajo inventario.

---

## 4. Matriz de Trazabilidad

La matriz de trazabilidad permite relacionar los requisitos del sistema con las historias de usuario y sus criterios de aceptación.

| ID del requisito | Requisito | Historia de usuario relacionada | Criterio de aceptación |
|---|---|---|---|
| RF-01 | El sistema deberá permitir registrar productos con información y código de barras válido. | HU-01 | El sistema registra el producto cuando la información y el código de barras son válidos. |

---

## 5. Conclusión

La construcción de este documento permite organizar las necesidades del cliente en una especificación técnica más clara. El alcance define qué funciones forman parte del sistema y cuáles quedan fuera, mientras que las restricciones técnicas establecen las tecnologías y condiciones obligatorias para su desarrollo.

Las historias de usuario permiten expresar las necesidades desde la perspectiva del usuario y los criterios de aceptación ayudan a comprobar cuándo una funcionalidad cumple con lo solicitado. Finalmente, la matriz de trazabilidad relaciona los requisitos con las funcionalidades del sistema, facilitando el seguimiento de cada necesidad durante el desarrollo.
