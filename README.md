# Proyecto análisis de métricas en Marketing

**Descripción del proyecto**  
El objetivo de este proyecto es encontrar patrones o tendencias que contribuyan a optimizar los costos de marketing de Shows; empresa que se dedica a la venta de entradas para eventos. Para ello, se cuenta con: 
- Registros del servidor con datos sobre las visitas a Shows desde Enero de 217 hasta Dicimebre de 2018,
- Un archivo con los pedidos de este período;
- Estadísticas de los gastos de marketing.

Lo que se investigó es:
- Cómo los clientes utilizan el servicio
- CUándo comienzan a comprar
- Cuánto dinero aporta cada cliente a la compañía
- Cuándo los ingresos cubren el costo de adquisición de los clientes

**Motivación**  
Dado que en el área de marketing de una empresa suelen existir diferentes canales, se busca identificar cuáles de ellos podrían reultar ser más rentables; analizando los costos de estos, los ingresos que provienen de clientes que llegaron por estos canales, y cuál es el finalmente el retorno de la inversión, con la finalidad de poder redirigir los recursos de una manera óptima; que permita aumentar los ingresos y adecuar los costos.  

**Características de los Datasets**  
*Visits*:  
Contiene datos sobre las visitas al sitio web de Shows
- Uid: identificador único del usuario
- Device: dispositivo del usuario
- Start Ts: fecha y hora de inicio de la sesión
- End Ts: fecha y hora de término de la sesión
- Source Id: identificador de la fuente de anuncios de la que proviene el usuario. Todas las fechas de esta tabla están en formato AAAA-MM-DD

*Orders*:  
Contiene información sobre los pedidos  
- Uid: identificador único del usuario
- Buy Ts: fecha y hora del pedido
- Revenue: ingreso monetario de Shows por el pedido que se realizó

*Costs*:  
Contiene los datos sobre los costos de marketing  
- Source Id: identificador del canal de anuncios
- Dt: fecha
- Costs: gastos del canal en el día

**Herramientas utilizadas:**  
- Lenguaje: Python 3
- Librerías:
    - Pandas para la manipulación de datos
    - Numpy para cálculos numéricos
    - Matplotlib y Seaborn para visualizaciones de los datos

**Proceso del proyecto**  
**1. Carga y Exploración de Datos**  

- Análisis inicial de los 3 datasets y revisión de la información de los mismos; tamaño de la data, tipos de datos, valores faltantes.
- EDA (análisis exploratorio de datos) para entender la relación entre las variables y los ingresos de venta

**2. Limpieza y Preprocesamiento**  

- No se hayaron valores nulos ni duplicados.
- Se modificaron los nombres de las columnas para cumplir con el formato PEP8.

**3. Análisis de los Datos**  

- Se analizó las cantidad de visitas diarias, semanales y mensuales de los usuarios al sitio web de Shows, así como la duración de una sesión.
- Se analizaron métricas de usuario como DAU, WAU, MAU y Sticky Factor.
- Se analizó el LTV (valor del ciclo de vida).
- Se analizaron los diferentes canales de marketing y se evaluaron las métricas CAC (costo de adquisición de clientes) y ROMI (retorno de la inverrsión en marketing).

**4. Resultados**  

- Shows no ha logrado recuperar la inversión mediante sus canales de marketing; se contempla 1 año de datos, y se observa que la inversión comienza a recuperarse al 9°-10° mes.
- El canal 3 y 4 resultaron mostrar la mayor conversión al primer día, sin embargo el costo de la adquisición de clientes para el canal 3 duplica al canal 4, por lo que en términos de rentabilidad, sería óptimo potenciar el canal 3 de marketing.
