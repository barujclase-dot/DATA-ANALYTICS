PROYECTO FINAL DE DATA SCIENCE - INSTRUCCIONES DE ENTREGA
========================================================

PROYECTO
Análisis del gasto de capital del Gobierno peruano y su relación con indicadores macroeconómicos.

Curso: Data Science
Docente: Daniel Elías Gavidia Pucllas
Integrantes: Jhan Mercado García y Abraham Huamaní Aliaga
Archivo principal para la entrega: 03_codigo/proyecto.ipynb
Fuente principal: Banco Central de Reserva del Perú (BCRP)

1. ORGANIZACIÓN DE LAS CARPETAS
------------------------------
01_documentacion/
    Acta del proyecto, informe de cierre, manual técnico y de usuario,
    anexos A, B y C, y documentación complementaria solicitada por el docente.

02_datos/
    Series del BCRP, base mensual utilizada, información de entrenamiento
    2015-2025, meses observados de 2026, diccionario de variables y fuentes.
    Conservar únicamente datos realmente descargados; identificar cualquier
    variable o mes aún no publicado.

03_codigo/
    proyecto.ipynb: notebook definitivo de Python para Google Colab.
    IMPORTANTE: debe ser la versión simplificada de 10 secciones, sin botón,
    sin exportación de ZIP y sin descargas automáticas de CSV.

04_resultados/
    PDF visual de tres páginas y un solo archivo Excel con diez hojas.
    Los dos archivos deben proceder de la misma ejecución del notebook.

05_presentacion/
    Presentación usada para la exposición. Revisar sus cifras y gráficos
    frente a los resultados más recientes del notebook antes de entregarla.

2. CÓMO EJECUTAR EL PROYECTO
---------------------------
1) Abrir Google Colab: https://colab.research.google.com/
2) Cargar el archivo 03_codigo/proyecto.ipynb.
3) Revisar la sección inicial: fechas, curso, integrantes y parámetros.
4) Seleccionar "Entorno de ejecución" > "Ejecutar todo".
5) Comprobar los controles de calidad, los gráficos y los errores de modelos.
6) Al finalizar, Colab descarga AUTOMÁTICAMENTE DOS ARCHIVOS POR SEPARADO:
   - Un PDF breve con los hallazgos, la selección del modelo y el pronóstico.
   - Un Excel con diez hojas de datos y resultados, sin Resumen ni Objetivos.
7) Guardar ambos archivos en 04_resultados/.
8) Guardar proyecto.ipynb con sus salidas ejecutadas y conservar una copia.
9) Si el navegador bloquea descargas múltiples, autorizar las dos descargas.


3. ALCANCE Y MÉTODO FINAL
------------------------
- Cobertura geográfica: Perú.
- Periodo de entrenamiento y análisis histórico: enero de 2015 a diciembre de 2025.
- Datos de 2026: los meses efectivamente publicados se usan para contrastar
  el pronóstico original, sin mezclarlos con el entrenamiento.
- Variable fiscal central: formación bruta de capital del Gobierno General
  (serie BCRP PN02210FM). No equivale a todas las partidas del gasto de capital.
- Indicadores: PBI, inflación, tipo de cambio e IPC de Lima Metropolitana.
- El IPC de Lima aproxima montos en términos reales; no es un deflactor
  específico de inversión pública de todo el país.
- Los gráficos incluyen composición del gasto, estacionalidad, correlaciones,
  errores de validación y pronóstico para 2026.
- Cuatro modelos: promedio estacional de tres años, Holt-Winters (ETS),
  SARIMA y ensamble simple de ETS y SARIMA.
- Validación temporal expansiva para 2022, 2023, 2024 y 2025, con MAE,
  RMSE, sMAPE y error porcentual anual.
- Pronóstico de 2026 con rangos aproximados del 80 % y 90 %.
- Las correlaciones indican asociación estadística, no causalidad.
- No se incluyen escenarios de estrés ni recortes hipotéticos.

4. CAMBIOS RESPECTO AL PRIMER AVANCE
-----------------------------------
- El alcance inicial incluía un análisis nacional e internacional. La
  comparación internacional se retiró por dificultades para reunir variables
  completas y comparables, incluidas consultas a fuentes como el Banco Mundial.
  El proyecto final se concentra en las series nacionales del BCRP.
- Se incorporaron modelos predictivos y ajustes por inflación, que no
  formaban parte del alcance inicial desarrollado.
- Los gráficos del primer script se revisaron, mejoraron y redujeron para
  facilitar la interpretación del problema y de los resultados principales.
- El código se simplificó: menos salidas innecesarias y cuatro modelos
  que pueden explicarse en una exposición universitaria.
- La entrega automática se redujo a un PDF de tres páginas y un Excel de
  diez hojas, separados; se eliminó el botón de exportación anterior.
- Un tablero interactivo, planteado como posible trabajo futuro en el
  primer avance, no forma parte de los entregables actuales.

5. USO DE INTELIGENCIA ARTIFICIAL Y TRANSPARENCIA
--------------------------------
Se utilizó IA como apoyo para buscar y organizar información, aclarar dudas,
identificar errores de programación, simplificar funciones y mejorar algunas
partes del script, gráficos y documentación. La IA no sustituye las fuentes
oficiales. Los integrantes deben revisar el código, comprobar los datos y
asumir la responsabilidad por las conclusiones presentadas.

