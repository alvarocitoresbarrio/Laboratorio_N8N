# Arquitectura

El prototipo separa la entrada del pedido, el registro en Google Sheets, la consulta de inventario y la decisión de disponibilidad.

## Regla de negocio

- Si `stock_disponible >= cantidad`, se acepta el pedido y se descuenta la cantidad.
- Si `stock_disponible < cantidad`, se marca como pendiente y no se modifica el inventario.

El generador aleatorio sustituye temporalmente la entrada de un comercial para facilitar pruebas repetidas. En un entorno real podría sustituirse por un formulario, CRM o webhook. Claude podría extraer campos de un mensaje libre, mientras n8n valida y aplica las reglas de negocio.
