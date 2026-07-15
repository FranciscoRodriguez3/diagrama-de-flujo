```mermaid
flowchart TD
    Inicio([Inicio: Usuario ingresa a tienda comercial]) --> Seleccion(Selecciona equipamiento y agrega al carrito)
    Seleccion --> Checkout(Procede al pago / Checkout)
    Checkout --> Decision{¿Pago aprobado?}
    
    Decision -- No --> Error(Notificar error al cliente)
    Error --> FinError([Fin del proceso])
    
    Decision -- Sí --> Orden(Generar orden y confirmar compra)
    Orden --> StockComercial(Descontar producto del Inventario Comercial)
    StockComercial --> Calculo(Calcular el % predefinido de la venta)
    Calculo --> FondoSocial(Acreditar ese % en el Fondo de Impacto Social)
    FondoSocial --> FinExito([Fin: Preparar pedido para envío])
