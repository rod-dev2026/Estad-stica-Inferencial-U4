# 📊 Laboratorio de Regresión

Aplicación web interactiva y autocontenida diseñada como herramienta didáctica de análisis estadístico. Permite ingresar conjuntos de datos propios (en formato CSV, separados por comas, punto y coma o tabuladores) o utilizar ejemplos precargados para ejecutar modelos de regresión completos con cálculos paso a paso, pruebas de hipótesis, diagnósticos de supuestos y visualizaciones vectoriales dinámicas.

## ✨ Características principales

* **100 % Autocontenido (Zero-Dependencies):** Implementado en un único archivo HTML5 con CSS3 y JavaScript puro (Vanilla JS). Todos los motores de álgebra lineal (inversión de matrices, productos punto), optimización numérica (Newton-Raphson / IRLS) y funciones estadísticas ($t$ de Student, $F$ de Fisher, $\chi^2$, normal estándar y funciones Beta/Gamma incompletas) están programados desde cero (con soporte de exportación a `.xlsx` vía SheetJS en las versiones que incluyen exportación a Excel).
* **Interfaz tipo "Banco de Trabajo":** Diseño responsivo de dos paneles con barra de navegación por temas, tema claro/oscuro adaptable (`prefers-color-scheme` y selector manual) y glosarios desplegables explicando cada métrica y columna.
* **Visualizaciones SVG e Interactivas:** Gráficas generadas dinámicamente en SVG, incluyendo bandas de confianza y predicción, curvas sigmoides, fronteras de decisión 2D, curvas ROC, probabilidades apiladas y un gráfico de dispersión con plano ajustado en 3D interactivo (arrastrable con el ratón o pantalla táctil).

## 📚 Módulos incluidos

El laboratorio está organizado en 5 módulos temáticos orientados a la enseñanza y práctica de la estadística aplicada:

* **Regresión Lineal Simple**
  * Cálculo paso a paso de medias, sumas de cuadrados ($S_{xx}, S_{xy}$), pendiente ($b_1$), intercepto ($b_0$), correlación ($r$), $R^2$ y error estándar ($s_e$).
  * Tabla ANOVA completa (con $F$ crítica), intervalos de confianza para parámetros, predicción puntual y despeje inverso de $X$ a partir de un valor objetivo de $Y$ (ej. análisis de SLA).
  * Gráfica de ajuste con intervalos de confianza de la media y de predicción, más gráfico de residuos.
* **Regresión Lineal Múltiple**
  * Estimación por Mínimos Cuadrados Ordinarios (MCO) matricial $\mathbf{b} = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{y}$.
  * Diagnóstico de colinealidad mediante Factor de Inflación de la Varianza (VIF), tolerancia ($1/\text{VIF}$), número de condición (en 2 predictores), matriz de correlaciones, coeficientes estandarizados ($\beta$), apalancamiento (leverage $h_i$) y residuos estudentizados para detección de valores atípicos.
  * Visualización 3D interactiva (para 2 predictores) junto con gráficas de valores observados vs. predichos y análisis de residuos.
* **Regresión Logística Simple**
  * Ajuste por Máxima Verosimilitud mediante el algoritmo iterativo Newton-Raphson (IRLS) mostrando la convergencia paso a paso.
  * Cálculo de log-odds, razones de momios (Odds Ratios con IC al 95 %), prueba de razón de verosimilitudes ($G$), AIC y $R^2$ de McFadden.
  * Curva sigmoide interactiva con umbral de decisión ajustable ($u$).
* **Regresión Logística Binaria (Múltiple)**
  * Clasificación binaria multipredictor con detección automática de separación perfecta.
  * Matriz de confusión dinámica al variar el umbral $u$, métricas de desempeño (Exactitud, Precisión, Sensibilidad, Especificidad, $F_1$-score) y tabla comparativa de umbrales.
  * Curva ROC con cálculo de AUC (Área Bajo la Curva), distribución de probabilidades estimadas y mapa de frontera de decisión 2D.
* **Regresión Logística Multinomial**
  * Modelado para variables respuesta con 3 o más categorías mediante función Softmax y selección de categoría de referencia.
  * Cálculo de Razones de Riesgo Relativo (RRR $= e^b$), predicción paso a paso para nuevos casos, matriz de confusión $K \times K$ con métricas por clase y promedio macro.
  * Gráficas de probabilidades acumuladas y regiones de decisión 2D.

## 🗂️ Historial de versiones y mejoras

* **v1.0 (`Laboratorio de Regresión 1.0.txt`):** Primera versión del banco de trabajo interactivo con los 5 modelos de regresión (lineal simple, lineal múltiple, logística simple, logística binaria y multinomial), editor de texto CSV/TSV, cálculos paso a paso, gráficas vectoriales SVG y visor 3D interactivo arrastrable.
* **v1.1 (`Laboratoio de regresión 1.1.html`):** Amplía la versión inicial con editor de celdas de datos y rotación automática en el visor 3D.
* **v1.2 (`Laboratoio de regresión 1.2.html`):** Refina el banco de trabajo con un editor de datos tipo hoja de cálculo (navegación mediante teclas y panel de edición ampliado), manteniendo los modelos y visualizaciones de la versión anterior.
* **v1.3 (`Laboratoio de regresión 1.3.html`):** Incorpora exportación de reportes imprimibles con formato estilo APA (PDF), descarga de datos en CSV, exportación a Excel (`.xlsx` mediante SheetJS) y descarga individual de gráficas en PNG.
* **v1.4 (`Laboratoio de regresión 1.4.txt`):** Añade contexto editable por ejercicio con glosario de conceptos, sección de conclusiones automáticas, prueba gráfica de hipótesis con región crítica ($F$ y $F$ crítica), comprobación formal de supuestos (linealidad, independencia vía Durbin–Watson, homocedasticidad vía Breusch–Pagan, normalidad vía Jarque–Bera con gráficos Q–Q, EPV, VIF e IIA), diagnóstico de colinealidad y comparación de predictores ($\beta$ estandarizado), además de mostrar tanto la forma normal como la ecuación ajustada con las variables del ejercicio.

## 🚀 Uso e instalación

No requiere servidor backend, compilación ni instalación de paquetes:

1. Clona este repositorio o descarga el archivo `Laboratorio de Regresión.html` (o la versión correspondiente):
   ```bash
   git clone [https://github.com/rod-dev2026/](https://github.com/rod-dev2026/)<nombre-del-repositorio>.git
