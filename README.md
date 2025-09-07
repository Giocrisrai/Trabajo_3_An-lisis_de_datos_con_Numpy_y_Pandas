# Trabajo 3: Análisis de datos con Numpy y Pandas

## 📋 Descripción del Proyecto

Este proyecto consiste en el análisis de datos de una cadena de tiendas minoristas ficticia llamada **RetailNow**. El objetivo es analizar los datos de ventas, inventarios y satisfacción del cliente utilizando las librerías **Pandas** y **NumPy** para optimizar el rendimiento de las tiendas.

## 🎯 Objetivos

- Cargar y limpiar datos de archivos CSV utilizando Pandas
- Realizar análisis estadísticos de ventas, inventarios y satisfacción del cliente
- Utilizar NumPy para cálculos estadísticos y simulaciones
- Generar visualizaciones adaptativas y reportes exportables
- Identificar tiendas con problemas de inventario y satisfacción

## 📊 Datos del Proyecto

El proyecto incluye tres archivos CSV principales:

### 1. **sales.csv** - Datos de Ventas
- **ID_Tienda**: Identificador único de la tienda
- **Producto**: Nombre del producto vendido
- **Cantidad_Vendida**: Cantidad de unidades vendidas
- **Precio_Unitario**: Precio por unidad del producto
- **Fecha_Venta**: Fecha de la venta

### 2. **inventories.csv** - Datos de Inventarios
- **ID_Tienda**: Identificador único de la tienda
- **Producto**: Nombre del producto
- **Stock_Disponible**: Cantidad disponible en inventario
- **Fecha_Actualización**: Fecha de actualización del inventario

### 3. **satisfaction.csv** - Datos de Satisfacción
- **ID_Tienda**: Identificador único de la tienda
- **Satisfacción_Promedio**: Puntuación de satisfacción (0-100)
- **Fecha_Evaluación**: Fecha de evaluación de satisfacción

## 🛠️ Tecnologías Utilizadas

- **Python 3.x**
- **Pandas 2.3.2** - Manipulación y análisis de datos
- **NumPy 2.3.2** - Cálculos numéricos y simulaciones
- **Matplotlib** - Visualizaciones
- **Jupyter Notebook** - Entorno de desarrollo

## 📁 Estructura del Proyecto

```
Trabajo_3_An-lisis_de_datos_con_Numpy_y_Pandas/
├── analisis_red_tiendas.ipynb          # Notebook principal con el análisis
├── README.md                           # Este archivo
└── workspace/                          # Directorio con datos
    ├── sales.csv                       # Datos de ventas
    ├── inventories.csv                 # Datos de inventarios
    ├── satisfaction.csv                # Datos de satisfacción
    ├── ventas_totales_por_tienda.csv   # Resultado: ventas por tienda
    ├── inventario_criticos_por_tienda.csv # Resultado: inventarios críticos
    └── tiendas_satisfaccion_baja.csv   # Resultado: tiendas con baja satisfacción
```

## 🚀 Instalación y Configuración

### Requisitos Previos
- Python 3.7 o superior
- Visual Studio Code con extensión de Jupyter
- Git (opcional)

### Instalación de Dependencias

```bash
pip install pandas numpy matplotlib jupyter
```

### Configuración del Entorno
1. Clona o descarga este repositorio
2. Abre Visual Studio Code
3. Instala la extensión de Jupyter si no la tienes
4. Abre el archivo `analisis_red_tiendas.ipynb`

## 📈 Análisis Realizados

### 1. **Carga y Limpieza de Datos (30%)**
- ✅ Carga de archivos CSV con rutas absolutas
- ✅ Limpieza de datos eliminando filas con valores nulos
- ✅ Validación de estructura de DataFrames
- ✅ Mapeo de columnas a nombres estándar

### 2. **Análisis de Datos con Pandas (30%)**
- ✅ **Ventas totales por tienda**: Cálculo de ingresos totales
- ✅ **Rotación de inventarios**: Análisis de productos vendidos vs. stock
- ✅ **Inventarios críticos**: Identificación de productos con <10% vendido
- ✅ **Satisfacción del cliente**: Filtrado de tiendas con <60% satisfacción
- ✅ **Análisis exploratorio**: Estadísticas descriptivas con `describe()`

### 3. **Cálculos Estadísticos con NumPy (20%)**
- ✅ **Mediana de ventas**: Cálculo usando `np.median()`
- ✅ **Desviación estándar**: Cálculo usando `np.std()`
- ✅ **Conversión de DataFrames**: Uso de `.to_numpy()`

### 4. **Simulación de Datos (20%)**
- ✅ **Proyecciones futuras**: Simulación de 12 meses usando `np.random.lognormal()`
- ✅ **Estadísticas de simulación**: Media, mediana y desviación estándar
- ✅ **Semilla reproducible**: `np.random.seed(42)` para resultados consistentes

## 📊 Visualizaciones

El proyecto incluye visualizaciones adaptativas:

1. **Gráfico de barras**: Ventas totales por tienda
2. **Histograma**: Distribución de ingresos
3. **Gráfico adaptativo**: 
   - Si hay productos críticos: % de productos críticos por tienda
   - Si no hay productos críticos: Bottom-10 por % vendido y boxplot

## 📋 Resultados Generados

### Archivos de Salida
- `ventas_totales_por_tienda.csv`: Ventas totales por cada tienda
- `inventario_criticos_por_tienda.csv`: Análisis de inventarios críticos
- `tiendas_satisfaccion_baja.csv`: Tiendas con satisfacción <60%

### Métricas Clave
- **Mediana de ventas**: $10,500.00
- **Desviación estándar**: $2,973.21
- **Tiendas analizadas**: 5 tiendas
- **Productos analizados**: 3 productos (A, B, C)

## 🔍 Hallazgos del Análisis

### Inventarios
- **No se detectaron productos críticos** (<10% vendido)
- Todos los productos muestran buena rotación
- Se generaron visualizaciones alternativas para mostrar el rendimiento

### Satisfacción del Cliente
- **1 tienda** presenta satisfacción baja (<60%): Tienda ID 5 (55%)
- **Recomendaciones** generadas para mejorar el rendimiento

### Ventas
- **Tienda 2** lidera en ventas totales
- **Distribución equilibrada** entre las tiendas
- **Proyecciones futuras** simuladas para 12 meses

## 🎓 Cumplimiento de la Rúbrica

| Criterio                | Peso | Estado | Descripción                                                        |
| ----------------------- | ---- | ------ | ------------------------------------------------------------------ |
| Carga y manejo de datos | 30%  | ✅      | Rutas absolutas, limpieza con `dropna()`, validación de estructura |
| Análisis de datos       | 30%  | ✅      | Ventas totales, rotación, críticos <10%, satisfacción <60%         |
| Cálculos estadísticos   | 20%  | ✅      | Mediana y desviación estándar con NumPy                            |
| Simulación de datos     | 20%  | ✅      | Proyecciones futuras con arrays aleatorios de NumPy                |

## 🚀 Cómo Ejecutar el Proyecto

1. **Abrir el Notebook**:
   ```bash
   jupyter notebook analisis_red_tiendas.ipynb
   ```

2. **Ejecutar todas las celdas**:
   - Usar "Run All" en Jupyter
   - O ejecutar celda por celda con Shift+Enter

3. **Verificar resultados**:
   - Los archivos CSV se generarán en la carpeta `workspace/`
   - Las visualizaciones se mostrarán en el notebook

## 📝 Notas Técnicas

### Rutas Absolutas
El proyecto utiliza una función `resolve_workspace_file()` que busca archivos en múltiples ubicaciones:
- Variable de entorno `WORKSPACE_DIR`
- `/workspace/`
- `<cwd>/workspace/` (hasta 3 niveles padre)
- `/mnt/data/` (entornos cloud)

### Reproducibilidad
- Semilla fija: `np.random.seed(42)`
- Resultados consistentes en cada ejecución
- Validaciones automáticas con `assert`

### Adaptabilidad
- Visualizaciones que se adaptan según los datos disponibles
- Manejo de casos edge (sin productos críticos)
- Exportación automática de resultados

## 👨‍💻 Autor

**Giocrisrai Godoy**  
Curso de Python UNIR - Trabajo 3

## 📄 Licencia

Este proyecto es parte de un trabajo académico para el Curso de Python UNIR.

---

*Última actualización: Septiembre 2025*
