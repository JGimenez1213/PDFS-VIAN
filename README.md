Inicialmente, se planteó extraer los datos del PDF utilizando coordenadas específicas, asumiendo que las posiciones de los datos eran fijas en todos los documentos. Sin embargo, esta aproximación no resultó eficiente debido a la variabilidad en el formato y disposición del contenido en los PDFs. Esto nos llevó a buscar una solución más flexible basada en el análisis de texto mediante patrones.

Posteriormente, decidimos trabajar con expresiones regulares (regex), que nos permitieron identificar y extraer los datos clave directamente del texto del PDF. Durante el proceso, realizamos varios ajustes importantes:

Cambio del símbolo del euro al formato "EUR": Inicialmente, se esperaba que el importe incluyera el símbolo €. Sin embargo, al analizar los PDFs, se observó que los importes estaban acompañados de las letras "EUR". Este cambio se incorporó al patrón de búsqueda.

Identificación del bastidor con guion: El bastidor en los PDFs estaba precedido por un guion (-), lo que requería ajustar la expresión regular para capturar únicamente la parte relevante (los 8 caracteres después del guion).

Incorporación de la fecha en formato DD/MM/AAAA: Añadimos la extracción de fechas al patrón de búsqueda, identificando correctamente los valores con este formato dentro del texto.
