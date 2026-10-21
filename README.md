# Cartera y Cobros

Herramienta para hacer seguimiento a las facturas pendientes y generar el correo mensual de cobro a cada cliente.

Funciona en tu computador, sin internet y sin instalar nada.

## Abrirla desde cualquier lado

Está publicada en GitHub Pages: **https://daniela723.github.io/ventas/**

Tus datos se sincronizan con Google Drive (**Ajustes y respaldo → Google Drive → Conectar**). Se guardan en el archivo "Cartera y Cobros - datos.json" de tu Drive, y cada equipo donde abras el link y conectes Drive ve la misma cartera. Si cambias algo en dos equipos al mismo tiempo, se juntan los cambios; si se toca la misma factura, gana el cambio más reciente.

La sincronización solo funciona desde el link de GitHub Pages (no al abrir `index.html` con doble clic).

### Configuración única de Google (ID de cliente)

1. Entra a https://console.cloud.google.com/ con tu cuenta de Google y crea un proyecto (por ejemplo "Cartera").
2. **APIs y servicios → Biblioteca**: busca **Google Drive API** y dale **Habilitar**.
3. **APIs y servicios → Pantalla de consentimiento de OAuth**: tipo **Externo**, nombre "Cartera y Cobros", tu correo. En **Usuarios de prueba** agrega tu correo. (Puedes dejarla en modo de prueba.)
4. **APIs y servicios → Credenciales → Crear credenciales → ID de cliente de OAuth**: tipo **Aplicación web**. En **Orígenes de JavaScript autorizados** agrega `https://daniela723.github.io`. Guarda.
5. Copia el **ID de cliente** (termina en `.apps.googleusercontent.com`) y ponlo en la constante `GOOGLE_CLIENT_ID` de `index.html` (o pégalo en **Ajustes → Google Drive** de cada equipo).

## Cómo tenerla en tu computador (sin internet)

1. En GitHub, en esta rama, haz clic en **Code → Download ZIP**.
2. Descomprime el ZIP en una carpeta fija, por ejemplo `Documentos/Cartera`.
3. Abre `index.html` con doble clic (mejor en Chrome o Edge). Puedes crear un acceso directo o guardarlo en favoritos.

Mantén juntos `index.html` y la carpeta `lib` (ahí está el lector de PDF). No muevas la carpeta de lugar después de empezar a usarla, y ábrela siempre con el mismo navegador: ahí es donde quedan guardados tus datos.

Para actualizar a una versión nueva: descarga el ZIP otra vez y reemplaza los archivos en la misma carpeta. Tus datos no se pierden porque están en el navegador, no en los archivos.

## Cómo se usa cada mes

1. **Cargar mes**: sube el PDF de facturas del mes. Se lee de cada factura el cliente, el número, el total bruto, el IVA, las retenciones y el total a pagar. Si el medio de pago incluye *Desembolso Crédito plus*, solo ese valor queda pendiente. Las notas crédito anulan la factura que referencian. Revisas la tabla, ajustas si hace falta y guardas. (También se pueden agregar a mano o pegar desde Excel.) Las facturas de meses anteriores quedan guardadas.
2. **Facturas**: marca como **Pagada** lo que ya te pagaron, o registra un **Abono** si pagaron una parte.
3. **Correos del mes**: aparece un correo por cliente con todas sus facturas pendientes, el total y los días de mora. Usa **Abrir en mi correo** o **Copiar correo**. El tono sube solo (amable → firme → último aviso) según la factura más vencida.
4. **Ajustes y respaldo**: descarga el respaldo (`.json`) al terminar. Guárdalo en Drive.

## Memoria

Todo se guarda en el navegador donde abres el archivo. Si cambias de computador o de navegador, usa **Restaurar respaldo** con el último archivo descargado.
