# StockFácil — Sistema de Control de Inventario

Sistema básico orientado a la gestión y supervisión de productos en el almacén de la empresa comercial **TecnoMarket**.

## Propósito
Centralizar y controlar de manera confiable la disponibilidad y estado de los productos en almacén, garantizando la trazabilidad de los cambios mediante control de versiones y una arquitectura modular en capas.

## Módulos Principales
- **Gestión de Productos:** Registro formal de artículos con código, nombre, precio y stock (RF-01), aplicando reglas de validación en capa de servicios (RF-02).
- **Control de Stock:** Actualización ágil de las cantidades disponibles de artículos en almacén (RF-03).
- **Consultas de Disponibilidad:** Verificación inmediata de existencias de productos para soporte operativo (RF-04).

## Estructura del Proyecto
El software aplica una arquitectura por capas con separación estricta de responsabilidades (RNF-01):

- `Controllers/` — Contiene `ProductoController.cs`, encargado de recibir las acciones del usuario y coordinar las solicitudes del módulo.
- `Models/` — Contiene `Producto.cs`, que define la entidad de dominio y los atributos de los artículos.
- `Services/` — Contiene `ProductoService.cs`, donde reside la lógica del negocio y las validaciones de datos.
- `Data/` — Contiene `ProductoRepository.cs`, responsable de gestionar el acceso y persistencia de la información.
- `Views/` — Contiene `ProductoView.cs`, interfaz que gestiona la interacción con el operador de almacén.

## Control de Versiones
El proyecto gestiona su ciclo de vida y evolución colaborativa mediante **Git** y **GitHub**, aplicando flujo de trabajo por ramas (`feature-*`), convenciones de commit semántico y revisión mediante *Pull Requests*.