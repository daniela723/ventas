# Cartera y Cobros

Herramienta para hacer seguimiento a las facturas pendientes y generar el correo mensual de cobro a cada cliente.

Es un solo archivo, `index.html`: se abre con doble clic en cualquier navegador, no necesita internet ni instalar nada.

## Cómo se usa cada mes

1. **Cargar mes**: agrega las facturas nuevas del mes (una por una o pegándolas desde Excel: Cliente · N.º factura · Valor · Fecha emisión · Vencimiento opcional). Las facturas de meses anteriores quedan guardadas.
2. **Facturas**: marca como **Pagada** lo que ya te pagaron, o registra un **Abono** si pagaron una parte.
3. **Correos del mes**: aparece un correo por cliente con todas sus facturas pendientes, el total y los días de mora. Usa **Abrir en mi correo** o **Copiar correo**. El tono sube solo (amable → firme → último aviso) según la factura más vencida.
4. **Ajustes y respaldo**: descarga el respaldo (`.json`) al terminar. Guárdalo en Drive.

## Memoria

Todo se guarda en el navegador donde abres el archivo. Si cambias de computador o de navegador, usa **Restaurar respaldo** con el último archivo descargado.
