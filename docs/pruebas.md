# Plan de pruebas

## Stock suficiente
Producto existente y cantidad solicitada menor o igual al stock. Esperado: pedido `Aceptado` y stock reducido exactamente.

## Stock insuficiente
Producto existente y cantidad solicitada superior al stock. Esperado: pedido `Pendiente` y stock sin cambios.

## Producto inexistente
Debe gestionarse sin descontar stock. Requiere una rama de tratamiento de consulta vacía; no se considera implementada hasta probarla.

## Pedido duplicado
Debe evitarse que una misma orden descuente inventario dos veces. Requiere idempotencia adicional.

Registrar fecha, datos de entrada, resultado y capturas reales. No marcar pruebas como superadas hasta ejecutarlas.
