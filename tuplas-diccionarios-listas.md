Introducción a cada uno de estos tipos de datos en Python:

### Listas:

Una lista en Python es una colección ordenada y mutable de elementos. Puedes almacenar diferentes tipos de datos en una lista y modificarla según sea necesario. Las listas se definen utilizando corchetes `[]` y los elementos se separan por comas `,`.

#### Ejemplo:

```python
# Crear una lista
mi_lista = [1, 2, 3, 'a', 'b', 'c']

# Acceder a elementos de la lista
print(mi_lista[0])  # Output: 1
print(mi_lista[3])  # Output: 'a'

# Modificar elementos de la lista
mi_lista[0] = 10
print(mi_lista)  # Output: [10, 2, 3, 'a', 'b', 'c']

# Agregar elementos a la lista
mi_lista.append('d')
print(mi_lista)  # Output: [10, 2, 3, 'a', 'b', 'c', 'd']
```

### Tuplas:

Una tupla en Python es similar a una lista, pero es inmutable, lo que significa que no se puede modificar después de su creación. Las tuplas se definen utilizando paréntesis `()` y los elementos se separan por comas `,`.

#### Ejemplo:

```python
# Crear una tupla
mi_tupla = (1, 2, 3, 'a', 'b', 'c')

# Acceder a elementos de la tupla
print(mi_tupla[0])  # Output: 1
print(mi_tupla[3])  # Output: 'a'

# Intentar modificar una tupla generará un error
# mi_tupla[0] = 10  # Generará un TypeError
```

### Diccionarios:

Un diccionario en Python es una colección desordenada y mutable de pares clave-valor. Cada elemento en un diccionario se representa como un par `clave: valor`. Los diccionarios se definen utilizando llaves `{}` y los pares clave-valor se separan por comas `,`.

#### Ejemplo:

```python
# Crear un diccionario
mi_diccionario = {'nombre': 'Juan', 'edad': 30, 'ciudad': 'Buenos Aires'}

# Acceder a elementos del diccionario por clave
print(mi_diccionario['nombre'])  # Output: 'Juan'
print(mi_diccionario['edad'])    # Output: 30

# Modificar elementos del diccionario
mi_diccionario['edad'] = 35
print(mi_diccionario)  # Output: {'nombre': 'Juan', 'edad': 35, 'ciudad': 'Buenos Aires'}

# Agregar nuevos elementos al diccionario
mi_diccionario['profesion'] = 'Ingeniero'
print(mi_diccionario)  # Output: {'nombre': 'Juan', 'edad': 35, 'ciudad': 'Buenos Aires', 'profesion': 'Ingeniero'}
```

