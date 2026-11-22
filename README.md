# 📊 Laboratorio de Regresión

Aplicación web interactiva y autocontenida diseñada como herramienta didáctica de análisis estadístico. Permite ingresar conjuntos de datos propios (en formato CSV, separados por comas, punto y coma o tabuladores) o utilizar ejemplos precargados para ejecutar modelos de regresión completos con cálculos paso a paso, pruebas de hipótesis y visualizaciones vectoriales dinámicas.

---

## ✨ Características principales

* **100 % Autocontenido (Zero-Dependencies):** Implementado en un único archivo HTML5 con CSS3 y JavaScript puro (`Vanilla JS`). Todos los motores de álgebra lineal (inversión de matrices, productos punto), optimización numérica (Newton-Raphson / IRLS) y funciones estadísticas ($t$ de Student, $F$ de Fisher, $\chi^2$, normal estándar y funciones Beta/Gamma incompletas) están programados desde cero[cite: 1].
* **Interfaz tipo "Banco de Trabajo":** Diseño responsivo de dos paneles con barra de navegación por temas, tema claro/oscuro adaptable (`prefers-color-scheme` y selector manual) y glosarios desplegables explicando cada métrica y columna[cite: 1].
* **Visualizaciones SVG e Interactivas:** Gráficas generadas dinámicamente en SVG, incluyendo bandas de confianza y predicción, curvas sigmoides, fronteras de decisión 2D, curvas ROC, probabilidades apiladas y un **gráfico de dispersión con plano ajustado en 3D interactivo** (arrastrable con el ratón o pantalla táctil)[cite: 1].

---

## 📚 Módulos incluidos

El laboratorio está organizado en 5 módulos temáticos orientados a la enseñanza y práctica de la estadística aplicada[cite: 1]:

1. **Regresión Lineal Simple**
   * Cálculo paso a paso de medias, sumas de cuadrados ($S_{xx}, S_{xy}$), pendiente ($b_1$), intercepto ($b_0$), correlación ($r$), $R^2$ y error estándar ($s_e$)[cite: 1].
   * Tabla ANOVA completa, intervalos de confianza para parámetros, predicción puntual y despeje inverso de $X$ a partir de un valor objetivo de $Y$ (ej. análisis de SLA)[cite: 1].
   * Gráfica de ajuste con intervalos de confianza de la media y de predicción, más gráfico de residuos[cite: 1].

2. **Regresión Lineal Múltiple**
   * Estimación por Mínimos Cuadrados Ordinarios (MCO) matricial $\mathbf{b} = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{y}$[cite: 1].
   * Diagnóstico de colinealidad mediante Factor de Inflación de la Varianza (**VIF**), coeficientes estandarizados ($\beta$), apalancamiento (*leverage* $h_i$) y residuos estudentizados para detección de valores atípicos[cite: 1].
   * Visualización **3D interactiva** (para 2 predictores) junto con gráficas de valores observados vs. predichos y análisis de residuos[cite: 1].

3. **Regresión Logística Simple**
   * Ajuste por Máxima Verosimilitud mediante el algoritmo iterativo **Newton-Raphson (IRLS)** mostrando la convergencia paso a paso[cite: 1].
   * Cálculo de *log-odds*, razones de momios (**Odds Ratios** con IC al 95 %), prueba de Wald, prueba de razón de verosimilitudes ($G$) y $R^2$ de McFadden[cite: 1].
   * Curva sigmoide interactiva con umbral de decisión ajustable ($u$) y puntos críticos de probabilidad[cite: 1].

4. **Regresión Logística Binaria (Múltiple)**
   * Clasificación binaria multipredictor con detección automática de separación perfecta[cite: 1].
   * **Matriz de confusión** dinámica al variar el umbral $u$, métricas de desempeño (Exactitud, Precisión, Sensibilidad, Especificidad, $F_1$-score) y tabla comparativa de umbrales[cite: 1].
   * **Curva ROC** con cálculo de **AUC** (Área Bajo la Curva), distribución de probabilidades estimadas y mapa de frontera de decisión 2D[cite: 1].

5. **Regresión Logística Multinomial**
   * Modelado para variables respuesta con 3 o más categorías mediante función *Softmax* y selección de categoría de referencia[cite: 1].
   * Cálculo de Razones de Riesgo Relativo (**RRR** $= e^b$), predicción paso a paso para nuevos casos, matriz de confusión $K \times K$ con métricas por clase y promedio macro[cite: 1].
   * Gráficas de probabilidades acumuladas, regiones de decisión 2D y barras de probabilidad para el caso nuevo[cite: 1].

---

## 🚀 Uso e instalación

No requiere servidor backend, compilación ni instalación de paquetes[cite: 1]:

1. Clona este repositorio o descarga el archivo `Laboratorio de Regresión.html`[cite: 1]:
   ```bash
   git clone [https://github.com/rod-dev2026/](https://github.com/rod-dev2026/)<nombre-del-repositorio>.git
