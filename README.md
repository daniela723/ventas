# Cartera y Cobros

Herramienta para hacer seguimiento a las facturas pendientes y generar el correo mensual de cobro a cada cliente.

Es un solo archivo, `index.html`: se abre con doble clic en cualquier navegador, no hay que instalar nada. Solo para leer PDFs necesita internet.

## Cómo se usa cada mes

1. **Cargar mes**: sube el PDF de facturas del mes. Se lee de cada factura el cliente, el número, el total bruto, el IVA, las retenciones y el total a pagar. Si el medio de pago incluye *Desembolso Crédito plus*, solo ese valor queda pendiente. Las notas crédito anulan la factura que referencian. Revisas la tabla, ajustas si hace falta y guardas. (También se pueden agregar a mano o pegar desde Excel.) Las facturas de meses anteriores quedan guardadas.
2. **Facturas**: marca como **Pagada** lo que ya te pagaron, o registra un **Abono** si pagaron una parte.
3. **Correos del mes**: aparece un correo por cliente con todas sus facturas pendientes, el total y los días de mora. Usa **Abrir en mi correo** o **Copiar correo**. El tono sube solo (amable → firme → último aviso) según la factura más vencida.
4. **Ajustes y respaldo**: descarga el respaldo (`.json`) al terminar. Guárdalo en Drive.

## Memoria

Todo se guarda en el navegador donde abres el archivo. Si cambias de computador o de navegador, usa **Restaurar respaldo** con el último archivo descargado.
