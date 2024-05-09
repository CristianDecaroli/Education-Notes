Lista de algunas de las funciones más utilizadas en Pandas junto con ejemplos de su uso:

1. **`read_csv()`:** Para leer datos desde un archivo CSV.
   
   ```python
   import pandas as pd
   df = pd.read_csv('datos.csv')
   ```
---
2. **`head()`:** Para ver las primeras filas del DataFrame.

   ```python
   df.head()
   ```
---
3. **`tail()`:** Para ver las últimas filas del DataFrame.

   ```python
   df.tail()
   ```
---
4. **`info()`:** Para obtener información sobre el DataFrame, incluyendo tipos de datos y valores no nulos.

   ```python
   df.info()
   ```
---
5. **`describe()`:** Para obtener estadísticas descriptivas sobre el DataFrame.

   ```python
   df.describe()
   ```
---
6. **`shape`:** Para obtener el tamaño del DataFrame (número de filas y columnas).

   ```python
   df.shape
   ```
---
7. **`columns`:** Para obtener una lista de nombres de columnas.

   ```python
   df.columns
   ```
---
8. **`loc[]`:** Para acceder a filas y columnas por etiquetas.

   ```python
   df.loc[0]  # Acceder a la primera fila
   df.loc[:, 'columna']  # Acceder a una columna
   ```
---
9. **`iloc[]`:** Para acceder a filas y columnas por índices enteros.

   ```python
   df.iloc[0]  # Acceder a la primera fila
   df.iloc[:, 0]  # Acceder a la primera columna
   ```
---
10. **`drop()`:** Para eliminar filas o columnas.

    ```python
    df.drop(0)  # Eliminar la primera fila
    df.drop('columna', axis=1)  # Eliminar una columna
    ```
---
11. **`fillna()`:** Para rellenar valores nulos con un valor específico.

    ```python
    df.fillna(0)  # Rellenar valores nulos con 0
    ```
---
12. **`dropna()`:** Para eliminar filas con valores nulos.

    ```python
    df.dropna()  # Eliminar filas con valores nulos
    ```
---
13. **`groupby()`:** Para agrupar datos por una o varias columnas y aplicar una función de agregación.

    ```python
    df.groupby('columna').mean()  # Calcular la media por grupo
    ```
---
14. **`merge()`:** Para combinar dos DataFrames utilizando una columna común.

    ```python
    pd.merge(df1, df2, on='columna_comun')  # Combinar dos DataFrames por una columna común
    ```
---
15. **`pivot_table()`:** Para crear una tabla dinámica a partir de un DataFrame.

    ```python
    pd.pivot_table(df, values='valor', index='fila', columns='columna')  # Crear una tabla dinámica
    ```
---
16. **`apply()`:** Para aplicar una función a lo largo de un eje del DataFrame.

    ```python
    df.apply(lambda x: x.max() - x.min())  # Calcular la diferencia entre el máximo y el mínimo por columna
    ```
---
17. **`sort_values()`:** Para ordenar los valores de un DataFrame por una o varias columnas.

    ```python
    df.sort_values('columna')  # Ordenar los valores por una columna específica
    ```
---
18. **`value_counts()`:** Para contar el número de ocurrencias de cada valor único en una columna.

    ```python
    df['columna'].value_counts()  # Contar las ocurrencias de cada valor único en una columna
    ```
---
19. **`to_csv()`:** Para escribir datos de un DataFrame en un archivo CSV.

    ```python
    df.to_csv('datos_nuevos.csv', index=False)  # Escribir datos en un archivo CSV sin incluir el índice
    ```
---
20. **`plot()`:** Para crear gráficos a partir de los datos de un DataFrame.

        ```python
        df.plot(x='columna_x', y='columna_y', kind='scatter')  # Crear un gráfico de dispersión
        ```
---
21. **`str.replace()`:** Para reemplazar valores en columnas de tipo `str`.

    ```python
    df['columna'].str.replace('valor_antiguo', 'valor_nuevo')  # Reemplazar valores en una columna de tipo str
    ```
---
22. **`str.contains()`:** Para verificar si una cadena de texto está contenida en otra.

    ```python
    df[df['columna'].str.contains('palabra_clave')]  # Filtrar filas que contienen una palabra clave en una columna de tipo str
    ```
---
23. **`astype()`:** Para cambiar el tipo de datos de una columna.

    ```python
    df['columna'] = df['columna'].astype('int')  # Cambiar el tipo de datos de una columna a entero
    ```
---
24. **`pd.to_datetime()`:** Para convertir una columna de tipo `str` en tipo `datetime`.

    ```python
    df['fecha'] = pd.to_datetime(df['fecha'])  # Convertir una columna de tipo str en tipo datetime
    ```
---
25. **`dt.year`, `dt.month`, `dt.day`, etc.:** Para acceder a componentes específicos de fechas.

    ```python
    df['fecha'].dt.year  # Obtener el año de una columna de tipo datetime
    ```
---
26. **`pd.cut()`:** Para dividir valores numéricos en intervalos discretos.

    ```python
    pd.cut(df['columna'], bins=[0, 10, 20, 30], labels=['grupo1', 'grupo2', 'grupo3'])  # Dividir valores en intervalos discretos
    ```
---
27. **`pd.qcut()`:** Para dividir valores numéricos en cuantiles.

    ```python
    pd.qcut(df['columna'], q=4)  # Dividir valores en cuartiles
    ```
---
28. **`pd.get_dummies()`:** Para crear variables dummy a partir de una columna categórica.

    ```python
    pd.get_dummies(df['columna'])  # Crear variables dummy a partir de una columna categórica
    ```
---
29. **`corr()`:** Para calcular la correlación entre columnas.

    ```python
    df.corr()  # Calcular la correlación entre columnas del DataFrame
    ```
---
30. **`rolling()`:** Para realizar operaciones de ventana rodante en datos de series temporales.

    ```python
    df['columna'].rolling(window=3).mean()  # Calcular la media móvil de una serie temporal
    ```


