# Revisión de la Biblioteca Seaborn

## 1. Tipos de Gráficos en Seaborn

Seaborn ofrece una variedad de gráficos para explorar y presentar datos. Algunos de los más comunes son:

- **Gráficos de dispersión (`scatterplot`)**: Muestran la relación entre dos variables numéricas.
  
- **Gráficos de líneas (`lineplot`)**: Ideales para visualizar tendencias a lo largo del tiempo.

- **Histogramas (`histplot`)**: Muestran la distribución de una variable numérica.

- **Gráficos de densidad (`kdeplot`)**: Representan la estimación de la densidad de probabilidad de una variable.

- **Gráficos de cajas (`boxplot`)**: Útiles para mostrar la distribución de una variable numérica y detectar valores atípicos.

- **Gráficos de violín (`violinplot`)**: Combinan boxplots y gráficos de densidad para mostrar la distribución de datos.

- **Gráficos de barras (`barplot`)**: Muestran promedios o conteos de una categoría y son útiles para comparaciones.

- **Gráficos de pares (`pairplot`)**: Permiten visualizar relaciones entre múltiples variables al mostrar gráficos de dispersión y distribuciones.

- **Gráficos de calor (`heatmap`)**: Representan datos matriciales y son ideales para mostrar correlaciones.

## 2. Estilos para una Presentación Más Profesional

Seaborn permite personalizar el estilo de los gráficos. Aquí hay algunos consejos:

- **Estilos predefinidos**: Puedes usar estilos como `"darkgrid"`, `"whitegrid"`, `"dark"`, `"white"` y `"ticks"` con `sns.set_style()`.

- **Paletas de colores**: Usa `sns.color_palette()` para elegir entre paletas como `"deep"`, `"pastel"`, `"muted"`, etc.

- **Tamaños de figura**: Ajusta el tamaño de la figura con `plt.figure(figsize=(ancho, alto))`.

- **Etiquetas y títulos**: Añade títulos (`plt.title()`) y etiquetas a los ejes (`plt.xlabel()`, `plt.ylabel()`) para mayor claridad.

- **Estilo de fuente**: Personaliza la fuente y el tamaño del texto con `plt.rc()`.

### Ejemplo de Código

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Cargar datos de ejemplo
tips = sns.load_dataset("tips")

# Establecer estilo
sns.set_style("whitegrid")

# Crear un gráfico de barras
plt.figure(figsize=(10, 6))
sns.barplot(x='day', y='total_bill', data=tips, palette='pastel')

# Añadir títulos y etiquetas
plt.title('Promedio de la Cuenta Total por Día', fontsize=16)
plt.xlabel('Día de la Semana', fontsize=14)
plt.ylabel('Promedio de Cuenta Total', fontsize=14)

plt.show()
