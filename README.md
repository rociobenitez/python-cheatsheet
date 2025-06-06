<h1 align="center">🐍 Python Cheatsheet</h1>

<p align="center">
  Todo lo esencial de <strong>Python</strong> en una sola hoja. <br/>
</p>

<div align="center">
  <img src="https://img.shields.io/badge/Python-CheatSheet-yellow.svg" alt="Python Badge"/>
  <img src="https://img.shields.io/badge/Práctico-100%25-brightgreen"/>
  <img src="https://img.shields.io/badge/Formato-Markdown-lightgrey.svg"/>
</div>

<br>

<p align="center">
  <a href="#tipos-de-datos"><img src="https://img.shields.io/badge/Tipos--Datos-blue.svg" alt="Tipos de datos"/></a>
  <a href="#operadores-y-expresiones"><img src="https://img.shields.io/badge/Operadores-blue.svg" alt="Operadores"/></a>
  <a href="#control-de-flujo"><img src="https://img.shields.io/badge/Control%20Flujo-blue.svg" alt="Control de flujo"/></a>
  <a href="#funciones"><img src="https://img.shields.io/badge/Funciones-blue.svg" alt="Funciones"/></a>
  <a href="#estructuras-funcionales"><img src="https://img.shields.io/badge/Funcional-blue.svg" alt="Funcional"/></a>
  <a href="#oop"><img src="https://img.shields.io/badge/OOP-blue.svg" alt="OOP"/></a>
  <a href="#concurrencia"><img src="https://img.shields.io/badge/Concurrencia-blue.svg" alt="Concurrencia"/></a>
  <a href="#red-y-correo"><img src="https://img.shields.io/badge/Red%20%26%20Correo-blue.svg" alt="Red y correo"/></a>
  <a href="#entornos-dependencias"><img src="https://img.shields.io/badge/Entornos--Dependencias-blue.svg" alt="Entornos"/></a>
  <a href="#io-archivos"><img src="https://img.shields.io/badge/I%2FO%20%26%20Archivos-blue.svg" alt="I/O y archivos"/></a>
  <a href="#bases-de-datos"><img src="https://img.shields.io/badge/Bases%20de%20Datos-blue.svg" alt="Bases de datos"/></a>
  <a href="#testing-debugging"><img src="https://img.shields.io/badge/Testing%20%26%20Debugging-blue.svg" alt="Testing"/></a>
  <a href="#fecha-tiempo-math"><img src="https://img.shields.io/badge/Fecha%20%26%20Math-blue.svg" alt="Fecha y math"/></a>
  <a href="#data-science"><img src="https://img.shields.io/badge/Data%20Science-blue.svg" alt="Data Science"/></a>
  <a href="#otros-paquetes"><img src="https://img.shields.io/badge/Otros%20Paquetes-blue.svg" alt="Otros paquetes"/></a>
</p>

# Índice de contenido

**Tipos de datos:** [`Números`](#numeros) | [`Strings`](#strings) | [`Booleanos`](#booleanos) | [`None`](#none) | [`Lists`](#lists) | [`Tuples`](#tuples) | [`Sets`](#sets) | [`Dictionaries`](#dictionaries) | [`Conversión de tipos`](#conversión-de-tipos)

**Operadores y expresiones:** [`Aritméticos & Lógicos`](#operadores) | [`Ternario`](#operador-ternario) | [`Any`/`All`](#any-all) | [`Desempaquetado`](#desempaquetado)

**Control de flujo:** [`if`](#if) | [`for`](#for) | [`while`](#while) | [`try/except`](#try-except) | [`Context managers`](#context-managers) | [`with`](#with)

**Funciones:** [`Funciones`](#funciones) | [`args`/`kwargs`](#args-y-kwargs) | [`lambda`](#lambda) | [`closures`](#closure) | [`decoradores`](#decoradores) | [`scope`](#scope)

**Funcional:** [`Comprehension`](#comprehension) | [`Map`/`Filter`/`Reduce`](#map-filter-reduce) | [`Iteradores`](#iteradores) | [`Generators`](#generators)

**OOP:** [`Clases`](#clases) | [`Propiedades`](#propiedades) | [`Encapsulación`](#encapsulación) | [`Métodos`](#métodos) | [`Herencia`](#herencia) | [`Polimorfismo`](#polimorfismo) | [`Abstracción`](#abstracción) | [`Duck Typing`](#ducktypes)

**Concurrencia:** [`threading`](#threading) | [`multiprocessing`](#multiprocessing) | [`asyncio`](#asyncio)

**Red y correo:** [`webbrowser`](#webbrowser) | [`smtplib`](#smtplib) | [`MIMEText`](#mime-text) | [`socket`](#socket) | [`requests`](#requests) | [`ftp`](#ftp)

**Módulos, entornos y dependencias:** [`Módulos`](#modulos) | [`venv`](#env) | [`pip`/`requirements`](#pip) | [`pipenv`](#pipenv) | [`poetry`](#poetry)

**I/O y archivos:**

- [`Lectura y escritura de archivos`](#lectura-escritura-archivos) | [`Rutas y directorios`](#rutas-y-directorios)
- Formatos: [`open`](#open) | [`csv`](#csv) | [`json`](#json) | [`html`/`xml`](#html-xml)
- Binario: [`zipfile`](#zipfile) | [`tarfile`](#tarfile)
- Sistema: [`pathlib`](#pathlib) | [`os, sys`](#files) | [`subprocess`](#subprocess)

**Bases de datos:** [`sqlite3`](#sqlite3) | [`MySQL`/`PostgreSQL`](#mysql-postgresql) | [`ORM`](#orm)

**Testing y debugging:** [`assert`](#assert) | [`logging`](#logging) | [`unittest`](#unittest) | [`pytest`](#pytest)

**Fechas, números y texto:** [`time`](#time) | [`datetime`](#datetime) | [`math`](#math) | [`random`](#random) | [`re (regex)`](#re)

**Data science:** [`numpy`](#numpy) | [`pandas`](#pandas) | [`matplotlib`](#matplotlib) | [`seaborn`](#seaborn) | [`beautifulsoup4`](#beautifulsoup4) | [`selenium`](#selenium) | [`scipy`](#scipy) | [`scikit-learn`](#scikit-learn) | [`tensorflow`](#tensorflow) | [`keras`](#keras)

**Otros paquetes:** [`gdown`](#gdown) | [`ydata-profiling`](#ydata-profiling)

<br>

# Tipos de datos

<a name="numeros"></a>

## Números

Los principales tipos de Python para los números son `int` (entero), `float` (decimal) y `complex` (complejo).

```python
type(1)          # int
type(-3)         # int
type(0)          # int
type(2.5)        # float
type(0.0)        # float
type(-3.6)       # float
type(1e-003)     # float (0.001)
type(1E6)        # float (1000000.0)
type(1j)         # complex (1+0j)
type(-1.23+4.5j) # complex
```

```python
# Funciones básicas
abs(-20)        # 20 --> valor absoluto
bin(512)        # '0b1000000000' --> formato binario
hex(512)        # '0x200' --> formato hexadecimal
pow(5, 2)       # 25 --> como hacer 5**2
round(5.46)     # 5
round(5.468, 2) # 5.47 --> round to nth digit
```

<a name="strings"></a>

## Strings

En Python, las cadenas de texto (strings o `str`) se almacenan como secuencias de caracteres en la memoria y son inmutables, no se puedes modificar.

```python
type("Rocío") # str
type('Rocío') # str
type("123")   # str
type("12.3")  # str
type("1e3")   # str

'I\'m a string'
"I'm a string"
"\n" # salto de línea
"\t" # tabulador

"Rocío"[2] # "c"
name = "Rocío Benítez"
name[0] # "R"
name[1] # "o"
name[-1] # "z"
name[-2] # "e"
name[0:3] # "Roc"
name[0:] # "Rocío Benítez"
name[:3] # "Roc"
name[3:] # "ío Benítez"
name[::1] # "Rocío Benítez"
name[::2] # "RcioBtz"
name[::-1] # "zéTneB iócR"
name[0:10:2] # "RcioB" --> slicing con formato [start:stop:step]

# Concatenar Strings
first_name = "Rocío"
last_name = "Benítez"
full_name = first_name + " " + last_name # "Rocío Benítez"

'Vivo en ' + 'Madrid' # 'Vivo en Madrid'
'*' * 10 # '**********' --> multiplicar una cadena de texto por un número

# Formatear Strings
name = "Rocío"
age = 30
f"Mi nombre es {name} y tengo {age} años" # "Mi nombre es Rocío y tengo 30 años"
"Mi nombre es {} y tengo {} años".format(name, age) # "Mi nombre es Rocío y tengo 30 años"
"Mi nombre es %s y tengo %d años" % (name, age) # %d para integer, %f para float, %s para string

frase = "{0:d} {1:s} actualmente son {2:.2f} dólares ($)"
print(frase.format(20, "euros (€)", 20*1.12)) # "20 euros (€) actualmente son 22,42 dólares ($)"
```

```python
# Funciones básicas
len("Rocío") # 5

# Métodos básicos
"Rocío".upper() # "ROCIO"
"Rocío".lower() # "rocío"
"vivo en madrid".capitalize() # "Vivo en madrid"
"vivo en madrid".title() # "Vivo En Madrid"

"Rocío".count("o") # 2
"Rocío".find("o")  # 2 --> devuelve el índice del primer caracter encontrado
"Rocío".find("z")  # -1 --> devuelve -1 si no encuentra el caracter
"Rocío".index("o") # 2 --> devuelve el índice del primer caracter encontrado
"Rocío".index("z") # ValueError --> devuelve un error si no encuentra el caracter

" Vivo en Madrid ".strip()  # "Vivo en Madrid" --> elimina espacios al principio y al final
" Vivo en Madrid ".lstrip() # "Vivo en Madrid " --> elimina espacios al principio
" Vivo en Madrid ".rstrip() # " Vivo en Madrid" --> elimina espacios al final
"Vivo en Madrid".split()    # ["Vivo", "en", "Madrid"] --> divide una cadena de texto en una lista de palabras

"Mi perra se llama Noa".replace("Mi", "Nuestra") # "Nuestra perra se llama Noa"
"Mi perra se llama Noa".replace("a", "o", 1) # "Mi perro se llama Noa" --> reemplaza la 1ª coincidencia
"Mi perra se llama Noa".startswith("Mi") # True
"Mi perra se llama Noa".endswith("Noa")  # True
"Mi perra se llama Noa".startswith("mi") # False
"Mi perra se llama Noa".endswith("noa")  # False
```

```python
# Comprobación palíndromo (palabra que se lee igual de izquierda a derecha que de derecha a izquierda)
word = 'reconocer'
palindrome = bool(word.find(word[::-1]) + 1)
print(palindrome) # True
print(word == word[::-1]) # True
```

<a name="booleanos"></a>

## Booleanos

Los **booleanos** son valores que pueden ser `True` o `False`.

```python
type(True)     # bool
type(False)    # bool

print(bool(1))        # True
print(bool(0))        # False
print(bool("1"))      # True
print(bool("0"))      # True
print(bool(0.0))      # False
print(bool(""))       # False
print(bool(" "))      # True
print(bool("a"))      # True
print(bool("A"))      # True
print(bool("True"))   # True
print(bool("False"))  # True
print(bool("None"))   # True
print(bool([]))       # False
print(bool([1]))      # True
print(bool({}))       # False
print(bool({1:1}))    # True
print(bool(()))       # False
print(bool(set()))    # False
print(bool(range(0))) # False
```

<a name="none"></a>

## None

`None` es usado para representar el **valor nulo** o **ausencia** de un valor.

```python
type(None) # NoneType
a = None
```

<a name="lists"></a>

## Lists

A diferencia de los strings, las **listas** son secuencias **mutables**, es decir, se pueden modificar.

```python
my_list = [1, 2, '3', True]

len(my_list)        # 4
my_list.index('3')  # 2
my_list.count(2)    # 1 --> cuantas veces aparece el 2

my_list[3]      # True
my_list[1:]     # [2, '3', True]
my_list[:1]     # [1]
my_list[-1]     # True
my_list[::1]    # [1, 2, '3', True]
my_list[::-1]   # [True, '3', 2, 1]
my_list[0:3:2]  # [1, '3']

# : se llama 'slicing' y tiene el formato [ start : end : step ]
```

```python
# Añadir elementos a una lista
my_list * 2          # [1, 2, '3', True, 1, 2, '3', True]
my_list + [100, 5]   # [1, 2, '3', True, 100, 5] - No modifica la lista original, crea una nueva

my_list.append(100)        # [1, 2, '3', True, 100]
my_list.extend([100, 200]) # [1, 2, '3', True, 100, 200] - Añade varios elementos
my_list.insert(2, '!!!')   # [1, 2, '!!!', '3', True] - Inserta el elemento en la posición 2 y mueve el resto a la derecha

' '.join(['Rocío','Benítez']) # 'Rocío Benítez' - Une los elementos con un separador (espacio en blanco)
```

Los métodos `append`, `extend` e `insert` mutan la lista original.

```python
# Copiar una lista
basket = ['apples', 'pears', 'oranges']
new_basket = basket.copy()
new_basket2 = basket[:]
```

```python
# Eliminar elementos de una lista
[1,2,3].pop()    # 3 --> modifica lista original, índice por defecto -1
[1,2,3].pop(1)   # 2 --> modifica lista original
[1,2,3].remove(2)# None --> [1,3] Elimina primera coincidencia o lanza ValueError.
[1,2,3].clear()  # None --> modifica lista original y elimina todos los items: []
del [1,2,3][0]   # None --> elimina item en índice 0 o lanza IndexError
```

```python
# Ordenar una lista
[1,2,5,3].sort()                # None --> Modifica la lista a [1, 2, 3, 5]
[1,2,5,3].sort(reverse=True)    # None --> Modifica la lista a [5, 3, 2, 1]
[1,2,5,3].reverse()             # None --> Modifica la lista a [3, 5, 2, 1]
sorted([1,2,5,3])               # [1, 2, 3, 5] --> crea una nueva lista ordenada
sorted([1,2,5,3], reverse=True) # [5, 3, 2, 1] --> nueva lista ordenada en orden descendente
```

```python
my_list = [(4,1),(2,4),(2,5),(1,6),(8,9)]

sorted(my_list,key=lambda x: int(x[0]))
# [(1, 6), (2, 4), (2, 5), (4, 1), (8, 9)] --> ordena por el primer elemento de la tupla (índice 0)

list(reversed([1,2,5,3]))
# [3, 5, 2, 1] --> reversed() devuelve un iterador, se convierte a lista con list()
```

```python
# Operaciones útiles
1 in [1,2,5,3]    # True
min([1,2,3,4,5])  # 1
max([1,2,3,4,5])  # 5
sum([1,2,3,4,5])  # 15

# Obtener el primer y último elemento de una lista
mList = [63, 21, 30, 14, 35, 26, 77, 18, 49, 10]
first, *x, last = mList
print(first) # 63
print(last)  # 10
```

```python
# Matrix
matrix = [[1,2,3], [4,5,6], [7,8,9]]
matrix[2][0] # 7 --> Grab first first of the third item in the matrix object
```

```python
# Looping through a matrix by rows:
mx = [[1,2,3],[4,5,6]]
for row in range(len(mx)):
	for col in range(len(mx[0])):
		print(mx[row][col]) # 1 2 3 4 5 6
# Transform into a list:
[mx[row][col] for row in range(len(mx)) for col in range(len(mx[0]))] # [1,2,3,4,5,6]

# Combine columns with zip and *:
[x for x in zip(*mx)] # [(1, 3), (2, 4)]
```

```python
# Funciones avanzadas
list_of_chars = list('Helloooo')  # ['H', 'e', 'l', 'l', 'o', 'o', 'o', 'o']
sum_of_elements = sum([1,2,3,4,5])  # 15
element_sum = [sum(pair) for pair in zip([1,2,3],[4,5,6])]  # [5, 7, 9]
sorted_by_second = sorted(['hi','you','man'], key=lambda el: el[1])  # ['man', 'hi', 'you']
sorted_by_key = sorted([
                       {'name': 'Elena', 'age': 30},
                       {'name': 'Ana', 'age': 18},
                       {'name': 'Ángel', 'age': 55}],
                       key=lambda el: (el['name']))
# [{'name': 'Ana', 'age': 18}, {'name': 'Elena', 'age': 30}, {'name': 'Ángel', 'age': 55}]
```

ℹ️ **Consultar [_'List Comprehension'_](#comprehensions) de la sección _'Estructuras funcionales'_**

```python
# Leer linea de un archivo en una lista
with open("myfile.txt") as f:
  lines = [line.strip() for line in f]
```

ℹ️ **Consultar [_'Lectura y escritura de archivos'_](#lectura-escritura-archivos) de la sección _'Sistema de archivos'_**

<a name="tuples"></a>

## Tuples

Como las listas, las **tuplas** son secuencias **inmutables**, no se pueden modificar.

```python
my_tuple = ('mandarina','fresas','mango', 'fresas')
mandarina, fresas, mango, fresas = my_tuple  # Tupla

len(my_tuple)   # 4
my_tuple[2]     # 'mango'
my_tuple[-1]    # 'fresas'
```

```python
# Inmutabilidad
my_tuple[1] = 'donuts'   # TypeError
my_tuple.append('vino')  # AttributeError
```

```python
# Métodos
my_tuple.index('fresas') # 1 - primera coincidencia
my_tuple.count('fresas') # 2 - cuantas veces aparece el elemento
```

```python
# Zip - Comprime dos listas en una tupla
list(zip([1,2,3], [4,5,6])) # [(1, 4), (2, 5), (3, 6)]
```

```python
# Unzip - Descomprime una tupla en dos listas
z = [(1, 2), (3, 4), (5, 6), (7, 8)] # Resultados de una función zip
unzip = lambda z: list(zip(*z))
unzip(z) # [(1, 3, 5, 7), (2, 4, 6, 8)]
```

<a name="sets"></a>

## Sets

Colección **desordenada** de elementos **únicos**.

```python
my_set = set()
my_set.add(1)   # {1}
my_set.add(100) # {1, 100}
my_set.add(100) # {1, 100} --> no duplicados!
```

```python
new_list = [1,2,3,3,3,4,4,5,6,1]
set(new_list)            # {1, 2, 3, 4, 5, 6}

my_set.remove(100)       # {1} --> KeyError si no encuentra el elemento
my_set.discard(100)      # {1} --> No da error si no encuentra el elemento
my_set.clear()           # {}
new_set = {1,2,3}.copy() # {1,2,3}
```

```python
set1 = {1,2,3}
set2 = {3,4,5}
set3 = set1.union(set2)                # {1,2,3,4,5}
set4 = set1.intersection(set2)         # {3}
set5 = set1.difference(set2)           # {1, 2}
set6 = set1.symmetric_difference(set2) # {1, 2, 4, 5}
set1.issubset(set2)                    # False
set1.issuperset(set2)                  # False
set1.isdisjoint(set2)                  # False --> devuelve True si no hay elementos en común
```

```python
# Frozenset
# hashable --> puede utilizarse como clave en un diccionario o como elemento en un conjunto
<frozenset> = frozenset(<collection>)
```

<a name="dictionaries"></a>

## Dictionaries

También conocidas como _mappings_ (mapeos) o _tablas hash_. Son **pares clave-valor** que se garantiza que conservan el orden de inserción a partir de Python 3.7

```python
my_dict = {'name': 'Rocío', 'age': 30}

my_dict['name']         # Rocío
len(my_dict)            # 3

list(my_dict.keys())    # ['name', 'age']
list(my_dict.values())  # ['Rocío', 30]
list(my_dict.items())   # [('name', 'Rocío'), ('age', 30)]

my_dict['favourite_snack'] = 'Anacardos' # {'name': 'Rocío', 'age': 30, 'favourite_snack': 'Anacardos'}

my_dict.get('age')      # 30 - Devuelve None si no encuentra la clave
my_dict.get('ages', 0)  # 0 -  Devuelve el valor por defecto si no encuentra la clave
```

```python
# Eliminar elementos de un diccionario
del my_dict['name']
my_dict.pop('name', None)
```

```python
# Modificar elementos de un diccionario
my_dict.update({'has_car': True})
# {'name': 'Rocío', 'age': 30, 'favourite_snack': 'Anacardos', 'has_car': True}

{**my_dict, **{'has_car': True} }
# {'name': 'Rocío', 'age': 30, 'favourite_snack': 'Anacardos', 'has_car': True}
```

```python
# Crear diccionarios a partir de otras colecciones
new_dict = dict([['name', 'Ro'],['age', 32],['has_car', False]])
new_dict = dict(zip(['name', 'age', 'has_car'],['Ro', 32, False]))
new_dict = my_dict.pop('favourite_snack') # Elimina el elemento del diccionario
```

```python
# Dictionary Comprehension (Comprensión de diccionarios)
{key: value for key, value in new_dict.items() if key == 'age' or key == 'name'}
# {'name': 'Ro', 'age': 32} --> Filtrar dict por keys (claves)
```

<a name="conversion-de-tipos"></a>

## Conversión de tipos _(type conversion)_

```python
# Convertir Strings a Números
age = input("¿Cuál es tu edad?")
age = int(age)
pi = input("¿Cuál es el valor de pi?")
pi = float(pi)

# Convertir Números a Strings
str(123)  # "123"
str(12.3) # "12.3"
str(1e3)  # "1000.0"

# Convertir int a float
float(123)  # 123.0
float(12.3) # 12.3
float(1e3)  # 1000.0

# Convertir float a int
int(123.0) # 123
int(12.3)  # 12

# Convertir booleanos a int
int(True)  # 1
int(False) # 0

# Convertir int a booleano
bool(1)  # True
bool(0)  # False

# Convertir float a booleano
bool(123.0)  # True
bool(0.0)    # False

# Convertir str a booleano
bool("True")  # True
bool("False") # True
bool("None")  # True
bool("")      # False
bool(" ")     # True

# Convertir tuple a list
list((1,2,3)) # [1, 2, 3]

# Convertir set a list
list({1,2,3}) # [1, 2, 3]

# Convertir set a list
list({1,2,3}) # [1, 2, 3]

# Convertir list a tuple
tuple([1,2,3]) # (1, 2, 3)

# Convertir set a tuple
tuple({1,2,3}) # (1, 2, 3)

# Convertir list a set
set([1,2,3]) # {1, 2, 3}

# Convertir tuple a set
set((1,2,3)) # {1, 2, 3}
```

<br>

# Operadores y expresiones

<a name="operadores"></a>

## Operadores aritméticos y lógicos

```python
# Operaciones aritméticas
10 + 3  # 13
10 - 3  # 7
10 * 3  # 30
10 ** 3 # 1000
10 / 3  # 3.3333333333333335
10 // 3 # 3 --> cociente de la división sin decimales - devuelve un entero
10 % 3  # 1 --> operador modulo - resto de la división. Útil para hallar números pares e impares
```

```python
# Operadores lógicos
True and True  # True
True and False # False
True or True   # True
True or False  # True
not True       # False
not False      # True
```

```python
1 < 2 and 4 > 1  # True
1 > 3 or 4 > 1   # True
1 is not 4       # True
not True         # False
1 not in [2,3,4] # True

if <condición evaluada como booleana>:
  # realizar acción 1
elif <condición evaluada como booleana>:
  # realizar acción 2
else:
  # realizar acción 3
```

```python
# Operadores de comparación - Devuelven True o False
==  # igual
!=  # no igual
>   # mayor que
<   # menor que
>=  # mayor o igual que
<=  # menor o igual que

<element> is <element>     # verifica si son el mismo objeto
<element> is not <element> # verifica si no son el mismo objeto
```

```python
10 == 10 # True
10 != 10 # False
10 > 10  # False
10 < 10  # False
10 >= 10 # True
10 <= 10 # True
```

<a name="operador-ternario"></a>

## Operador Ternario

```python
# <expression_if_true> if <condition> else <expression_if_false>

[a if a else 'zero' for a in [0, 1, 0, 3]] # ['zero', 1, 'zero', 3]
```

<a name="any-all"></a>

## Any All

```python
any([False, True, False]) # True si al menos uno es verdadero, False si está vacío
all([True,1,3,True])      # True si todos son verdaderos
```

<a name="desempaquetado"></a>

## Desempaquetado con \* y \*\*

```python
# Desempaquetado de listas
a, b, *c = [1, 2, 3, 4, 5]
a # 1
b # 2
c # [3, 4, 5]
```

Ver más en la sección: [_Funciones: args y kwargs_](#args-y-kwargs).

<br>

# Control de flujo

<a name="if"></a>

## if

```python
if <condition>:
  # código a ejecutar si la condición es verdadera (True)
elif <condition>:
  # código a ejecutar si se cumple elif
else:
  # código a ejecutar si nada anterior se cumple
```

```python
x = 10
if x > 0:
    print("Positivo")
elif x == 0:
    print("Cero")
else:
    print("Negativo")
```

<a name="for"></a>

## for

Cuando se conoce el número de iteraciones.

```python
for <elemento> in <iterable>:
  # código a ejecutar para cada elemento del iterable
```

```python
for i in range(10): # range excluye el último número
  print(i) # 0 1 2 3 4 5 6 7 8 9
```

- `break` → termina el bucle
- `continue` → salta a la siguiente iteración
- `else` → se ejecuta si el bucle termina sin break

```python
for i in range(3):
    if i == 1:
        break
    else:
        print("Fin sin break")  # No se ejecuta
```

### enumerate

```python
for i, elemento in enumerate(lista):
  # código a ejecutar para cada elemento del iterable
```

```python
for i, elemento in enumerate(lista):
  print(i, elemento) # 0 elemento1 1 elemento2 2 elemento3
```

<a name="while"></a>

## while

Cuando no se conoce el número exacto de iteraciones.

```python
while <condition>:
  # código a ejecutar mientras la condición sea verdadera (True)
```

```python
i = 0
while i < 10:
    print(i)
    i += 1
```

- `break`, `continue`, `else` funcionan igual que con `for`.

<a name="try-except"></a>

## try/except

```python
try:
  # código a ejecutar
except <exception>: # TipoDeError
  # código a ejecutar si hay error
```

```python
try:
  # código a ejecutar (intento)
except <exception>: # ejemplo: ValueError
  # código a ejecutar si hay error (manejo del error)
except <exception>: # ejemplo: TypeError, ZeroDivisionError
  # código a ejecutar si hay error (manejo de múltiples error)
else:
  # código a ejecutar si no hay error
finally:
  # código que siempre se ejecuta
```

### Excepciones comunes

```python
print(10 / 0)  # ZeroDivisionError
```

```python
print(a + 5)  # NameError: name 'a' is not defined (si 'a' no se ha definido previamente)
```

```python
print(int("abc"))  # ValueError
```

```python
with open("nonexistent_file.txt", "r") as file:
    content = file.read()  # FileNotFoundError
```

```python
mi_lista = [1,2,3]
mi_lista[1]  # No IndexError
mi_lista[5]  # IndexError
```

```python
my_dict = {'nombre': 'Rocío', 'age': 30}
value = my_dict.get('apellido') # No KeyError, usando el método .get()
missing = my_dict['apellido']   # KeyError
```

```python
print("hello" + 5)  # TypeError
```

```python
text = "ejemplo"
length = len(text)            # No AttributeError
missing = text.some_method()  # AttributeError (si no posee ese atributo o método)
```

```python
import modulo_no_existente  # ImportError
```

**Ejemplo de manejo de la excepción:**

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Error: No se puede dividir entre cero")

# Esta línea se ejecutará independientemente de si ocurrió una excepción
print("fuera del bloque try y except")
```

> _Hay muchas más excepciones en Python (`AssertionError`, `MemoryError`, `OverflowError`, `FloatingPointError`, `OSError`, `ModuleNotFoundError`, `StopIteration`, `KeyboardInterrupt`, `SystemExit`, `IndentationError`...)_

### `raise`

Lanza una excepción manualmente.

```python
raise ValueError("Mensaje de error")
```

Puede usarse dentro de funciones para validaciones personalizadas.

<a name="with"></a>

## with

- Controla **cómo y cuando** se entra y se sale de un bloque de código.
- Sirve para **gestionar recursos** como archivos, conexiones de bases de datos, etc.
- Se basa internamiente en el protocolo de **context managers** (`__enter__` y `__exit__`).

```python
with open('file.txt', 'r') as f:
    data = f.read()
    print(data)
```

```python
with open("a.txt") as f1, open("b.txt") as f2:
    ...
```

> 🔗 [Más información sobre _Lectura y escritura de archivos_](#lectura-escritura-archivos)

```python
from threading import Lock

lock = Lock()

with lock:  # Gestiona acceso a un recurso compartido
    # sección crítica
```

<a name="context-managers"></a>

## Context managers

```python
with <context_manager> as <variable>:
  # código a ejecutar
```

```python
# Context manager para abrir y cerrar un archivo
class FileManager:
    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode
    def __enter__(self):
        self.file = open(self.filename, self.mode)
        return self.file
    def __exit__(self, type, value, traceback):
        self.file.close()
# Usar el context manager
with FileManager('file.txt', 'r') as f:
    data = f.read()
    print(data)
```

<br>

# Funciones en Python

<a name="funciones"></a>

## Funciones

```python
def function_name(parametro1, parametro2):
    # code to execute
    return value
```

```python
def function_name(parametro1, parametro2):
    pass # no hace nada
```

```python
# Función para saludar
def greet(name):
    print("Hola, " + name + " 😊")
    # Sin valor de retorno (return None)

# Llamar a la función
greet("Rocío") # "Hola, Rocío 😊"
```

<a name="args-y-kwargs"></a>

## args y kwargs

Cada función puede tener **argumentos posicionales** (`args`) y **argumentos de palabras clave** (`kwargs`).

- `args`: se pasan en el **orden** en que se definen
- `kwargs`: se pasan con el nombre de la palabra clave

```python
some_func(1, 2, x=3, y=4, z=5) # args = (1, 2), kwargs = {'x': 3, 'y': 4, 'z': 5}
```

### \*args y \*\*kwargs

El operador **splat** (\*) expande una colección en **argumentos posicionales**, mientras que el operador **splatty-splat** (\*\*) expande un diccionario en **argumentos de palabras clave**.

```python
args = (1, 2)
kwargs = {'x': 3, 'y': 4, 'z': 5}
some_func(*args, **kwargs) # igual a some_func(1, 2, x=3, y=4, z=5)
```

### \* dentro de la definición de la función

_Splat_ combina **cero o más argumentos posicionales** en una **tupla**, mientras que _splatty-splat_ combina **cero o más argumentos de palabras clave** en un **diccionario**.

```python
def add(*a):
    return sum(a)

add(1, 2, 3) # 6
```

### Parámetros vs Argumentos

Los parámetros son las variables que se definen en la definición de la función, mientras que los argumentos son los valores que se pasan a la función cuando se llama.

```python
def greet(name): # name es un parámetro
    print(f"¡Hola, {name}!")  # uso del parámetro name
greet("Rocío") # "¡Hola, Rocío!"  --> "Rocío" es un argumento
```

### Ordenación de argumentos

```python
def f(*args):                  # f(1, 2, 3)
def f(x, *args):               # f(1, 2, 3)
def f(*args, z):               # f(1, 2, z=3)
def f(x, *args, z):            # f(1, 2, z=3)

def f(**kwargs):               # f(x=1, y=2, z=3)
def f(x, **kwargs):            # f(x=1, y=2, z=3) | f(1, y=2, z=3)

def f(*args, **kwargs):        # f(x=1, y=2, z=3) | f(1, y=2, z=3) | f(1, 2, z=3) | f(1, 2, 3)
def f(x, *args, **kwargs):     # f(x=1, y=2, z=3) | f(1, y=2, z=3) | f(1, 2, z=3) | f(1, 2, 3)
def f(*args, y, **kwargs):     # f(x=1, y=2, z=3) | f(1, y=2, z=3)
def f(x, *args, z, **kwargs):  # f(x=1, y=2, z=3) | f(1, y=2, z=3) | f(1, 2, z=3)
```

### Otros usos de \*

Crear una nueva lista, conjunto (set), una tupla o un diccionario desempaquetando otras listas o diccionarios. Saca los elementos individuales y los une:

```python
[*[1,2,3], *[4]]   # [1, 2, 3, 4]
{*[1,2,3], *[4]}   # {1, 2, 3, 4}
(*[1,2,3], *[4])   # (1, 2, 3, 4)
{**{'a': 1, 'b': 2}, **{'c': 3}}  # {'a': 1, 'b': 2, 'c': 3}
```

No puede haber duplicados en los conjuntos (set).

```python
{*[1,2,3], *[3]}   # {1, 2, 3}
```

En los diccionarios, si hay claves repetidas, la última sobreescribe a las anteriores.

```python
{**{'a': 1, 'b': 2}, **{'a': 3, 'c': 4}}  # {'a': 3, 'b': 2, 'c': 4}
```

Podemos usar **desempaquetado extendido** para asignar valores de una lista:

```python
head, *body, tail = [1,2,3,4,5]
```

`head` toma el **primer** elemento de la lista, `tail` toma el **último** elemento de la lista y `body` toma el resto de elementos de la lista (todo lo que queda en medio).

<a name="lambda"></a>

## Lambda

Las funciones **lambda** son funciones anónimas que se pueden definir en una sola línea.

```python
lambda : <valor_devuelto>
lambda <argumentos> : <expresión>
lambda <arg1>, <arg2> : <valor_devuelto>
```

```python
# Factorial
from functools import reduce

n = 3
factorial = reduce(lambda x, y: x*y, range(1, n+1))
print(factorial) # 6
```

En el bloque anterior, `range(1, n+1)` genera `[1, 2, 3]` y `reduce` aplica la función `lambda` a cada elemento de la lista (en este caso, multiplica dos valores).

```python
# Fibonacci
fib = lambda n : n if n <= 1 else fib(n-1) + fib(n-2)
result = fib(10)
print(result) # 55
```

Esta función **recursiva** calcula el [número de Fibonacci](https://es.wikipedia.org/wiki/Sucesi%C3%B3n_de_Fibonacci) para `n`. Si `n <= 1`, devuelve `n`. De lo contrario, devuelve la suma de los dos números anteriores. _Aunque es poco común usar lambda para funciones recursivas (es menos legible), aquí se hace para demostrar que también puede hacerse._

<a name="closures"></a>

## Closures

Una **closure** _(clausura)_ en Python ocurre cuando:

- Hay una **función anidada** (dentro de otra).
- La función interna **usa variables de la externa.**
- La función externa **retorna** la función interna.

```python
def get_multiplier(a):
    def out(b):
        return a * b
    return out
```

```python
multiply_by_3 = get_multiplier(3)
multiply_by_3(10) # 30
```

Si varias funciones internas acceden al mismo valor externo, **comparten ese valor.**

```python
# Acceder al valor interno ("a") desde fuera
# usando <function>.__closure__[0].cell_contents
multiply_by_3.__closure__[0].cell_contents # 3
```

<a name="decoradores"></a>

## Decoradores

Un **decorador** es una función que toma como argumento otra función y la **modifica**.

```python
@decorator_name
def function_that_gets_passed_to_decorator():
    ...
```

```python
def decorator_function(function):
    def wrapper_function():
        # hacer algo antes de llamar a la función
        function()
        # function() --> también es posible volver a llamar a la función
        # hacer algo después de llamar a la función
    return wrapper_function
    ...
```

**Ejemplo de decorador: _Cronometrar el tiempo de ejecución de una función_.**

El decorador functools `@functools.wraps` se utiliza para mantener el nombre de la función y la documentación de la función dentro del decorador.

```python
from time import time
import functools

def performance(func):

    @functools.wraps()
    def wrapper(*args, **kwargs):
        t1 = time()
        result = func(*args, **kwargs)
        t2 = time()
        print(f"La función tardó {t2 - t1} segundos en ejecutarse")
        return result
    return wrapper

## Llamar a la función con el decorador
@performance
def long_time():
    print(sum(i*i for i in range(10000)))
```

Los **decoradores** son útiles para **modificar el comportamiento de una función** sin tener que modificar la función en sí. Veamos un ejemplo:

**Ejemplo de decorador: _Retrasar la ejecución de una o varias funciones_.**

```python
import functools
import time

# Decorador que retarda la ejecución de una función 2 segundos
def delay_decorator(func):
    def wrapper(*args, **kwargs):
        time.sleep(2)
        func(*args, **kwargs)
    return wrapper

@delay_decorator
def say_hello():
    print("Hello!")

@delay_decorator
def say_bye():
    print("Bye!")

say_hello() # "Hello!"
say_bye()   # "Bye!"
```

<a name="scope"></a>

## Scope

Si la variable se asigna a cualquier parte del **scope** _(alcance)_, se considera una **variable local, a menos que se declare como 'global' o 'nonlocal'.**

```python
def get_counter():
    i = 0
    def out():
        nonlocal i
        i += 1
        return i
    return out
```

```python
counter = get_counter()
counter(), counter(), counter() # (1, 2, 3)
```

```python
def saludar():
    saludo = "Hola Mundo!"

print(saludo) # NameError: name 'saludo' is not defined
```

```python
def login_message():
    message = "Sesión iniciada"
    print(message)

def logout_message():
    message = "Sesión cerrada"
    print(message)

login_message()  # "Sesión iniciada"
logout_message() # "Sesión cerrada"
logint_message() # "Sesión iniciada"
```

```python
message = "Hola Mundo!" # Global scope (contexto global)

def login_message():
    print(message)  # Genera 'UnboundLocalError'
    message = "Sesión iniciada"

login_message()  # UnboundLocalError: cannot access local variable'message'
```

```python
message = "Hola Mundo!"

def login_message():
    message = "Sesión iniciada"
    print(message)

login_message() # "Sesión iniciada"
print(message)  # "Hola Mundo!"
```

> [!NOTE]
>
> _**Usar variables globales es considerada una mala práctica.** Es preferible definir variables dentro del contexto donde van a ser utilizadas, ya que las globales pueden modificarse accidentalmente en cualquier parte del programa (por ejemplo, dentro de una función)._

<br>

# Estructuras funcionales

<a name="comprehensions"></a>

## Comprehensions

La **[comprensión de listas](https://docs.python.org/es/dev/tutorial/datastructures.html#list-comprehensions)** es una forma de crear listas en Python en una sola línea.

También existen **comprehensions para sets, diccionarios y tuplas.**

```markdown
<list> = [<acción> for <item> in <iterador> if <condición>]
```

```python
a = [i for i in 'hello']                   # ['h', 'e', 'l', 'l', '0']
b = [i*2 for i in [1,2,3]]                 # [2, 4, 6]
c = [i for i in range(0,10) if i % 2 == 0] # [0, 2, 4, 6, 8]
```

```python
<list> = [i+1 for i in range(10)]         # [1, 2, ..., 10]
<set>  = {i for i in range(10) if i > 5}  # {6, 7, 8, 9}
<iter> = (i+5 for i in range(10))         # (5, 6, ..., 14)
<dict> = {i: i*2 for i in range(10)}      # {0: 0, 1: 2, ..., 9: 18}
```

```python
output = [i+j for i in range(3) for j in range(3)] # [0, 1, 2, 1, 2, 3, 2, 3, 4]

# Es equivalente a:
output = []
for i in range(3):
  for j in range(3):
    output.append(i+j)
```

<a name="map-filter-reduce"></a>

## Map Filter Reduce

```python
from functools import reduce
list(map(lambda x: x + 1, range(10)))            # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
list(filter(lambda x: x > 5, range(10)))         # (6, 7, 8, 9)
reduce(lambda acc, x: acc + x, range(10))        # 45
```

- `map` aplica una función a cada elemento.
- `filter` filtra elementos según una condición.
- `reduce` aplica una función a cada elemento y devuelve un solo valor acumulado.

<a name="iteradores"></a>

## Iteradores

Un **iterador** es un objeto que puede iterarse (recorrerse) uno por uno, devolviendo los valores de sus elementos.

```python
<iter> = iter(<collection>)  # Convierte una colección (lista, tupla, string...) en un iterador
<iter> = iter(<function>, to_exclusive)  # Secuencia de valores devueltos hasta 'to_exclusive'
<el>   = next(<iter> [, default])  # Lanza StopIteration o devuelve 'default' si termina
```

```python
iter([1, 2, 3]) # <list_iterator object at 0x7fc190371f00>
```

```python
from random import randint

def lanzar_dado():
    return randint(1, 6)

tiradas = iter(lanzar_dado, 6)  # genera valores hasta que salga un 6

for valor in tiradas:
    print(f"Tirada: {valor}")
```

```python
users = iter(['Rocío', 'Ana', 'Alejandro'])

print(next(users))  # "Rocío"
print(next(users))  # "Ana"
print(next(users))  # "Alejandro"
print(next(users, "No hay más usuarios"))  # "No hay más usuarios" (no hay más elementos)
```

<a name="generators"></a>

## Generators

Un **generator** es una forma cómoda de crear un iterador usando la palabra clave `yield` en lugar de `return`.

```python
def count(start, step):
    while True:
        yield start
        start += step
```

En esta función no se devuelve un valor con `return`, sino que se **genera valores uno a uno** con `yield`. Cada vez que se llama a la función con `next(...)`, **se retoma la ejecución justo donde se quedó**, manteniendo el estado interno (como `start`).

```python
counter = count(10, 2)
next(counter)  # 10
next(counter)  # 12
next(counter)  # 14
```

Un **generator** es más eficiente (no guarda todos los valores en memoria, sino que genera uno a uno). Son ideales para **secuencias infinitas** o grandes.

<a name="oop"></a>

# Programación orientada a objetos

<a name="clases"></a>

## Clases

### Definición de clase e instancias

```python
class NombreClase(object): # Definir clase

    class_atribute = value # Atributo de clase (compartido por todas las instancias)

    def __init__(self, a): # Constructor (inicializa atributos de instancia)
        self.a = a         # Atributo (dato)
    def __str__(self):
        return str(self.a)
    def __repr__(self):
        class_name = self.__class__.__name__
        return f"{class_name}({self.a!r})"

    def metodo1(self, parametro1, parametro2, ...):
        # Lógica del método
        pass

    # Más métodos aquí

    @classmethod              # Decorador
    def get_class_name(cls):
        return cls.__name__
```

```python
class Perro:  # Clase
    especie = "Canis lupus" # Atributo de clase

    def __init__(self, nombre, edad): # Parámetros: self, nombre, edad
        self.__nombre = nombre        # Atributo privado (encapsulado)
        self.edad = edad              # Atributo público

    def hablar(self):                 # Método de instancia (función)
        print("¡Guau!")
```

```python
mi_perro = Perro("Noa", 6)  # Instancia de la clase (objeto basado en esa clase)
mi_perro                    # "Perro(nombre=Noa, edad=6)"
mi_perro.name               # "Noa"
mi_perro.hablar()           # "¡Guau!"
mi_perro.__nombre           # AttributeError: 'Perro' object has no attribute '__nombre'
```

### Encapsulación con `@property`

```python
class Perro:  # Clase
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    @property                 # Decorador
    def nombre(self):         # Getter
        return self.__nombre

    @nombre.setter            # Decorador
    def nombre(self, nombre): # Setter con validación
        if nombre.strip():
            self.__nombre = nombre
        return
```

```python
mi_perro.nombre           # Accede
mi_perro.nombre = "Erika" # Modifica con validación
```

### Métodos mágicos (`dunder methods`)

Son métodos que no se llaman directamente, sino automáticamente.

```python
class Perro:
    ...

    def __str__(self):
        return f"Perro(nombre={self.nombre}, edad={self.edad})"

    def __repr__(self):
        return f"Perro({self.nombre!r}, {self.edad!r})"
```

```python
print(str(mi_perro))   # Perro(nombre=Erika, edad=6)
print(repr(mi_perro))  # Perro('Erika', 6)
```

| Método        | Propósito                              |
| ------------- | -------------------------------------- |
| `__init__`    | Constructor                            |
| `__str__`     | Representación legible                 |
| `__repr__`    | Representación técnica                 |
| `__len__`     | Longitud                               |
| `__eq__`      | Comparación con `==`                   |
| `__lt__`      | Comparación con `<`                    |
| `__add__`     | Suma con `+`                           |
| `__call__`    | Permite usar la instancia como función |
| `__getitem__` | Acceso tipo lista/dict                 |

> _**No es necesario implementar todos los métodos mágicos.** Se pueden implementar solo los que sean necesarios._

> 🔗 [Más información sobre _Python's Magic Methods_](https://rszalski.github.io/magicmethods/#representations)

**Método mágico destructor:**

```python
def __del__(self):
    print(f"El perro {self.nombre} ha sido eliminado")
```

### Métodos de clase y de fábrica

```python
class Perro:
    especie = "Canis lupus" # Atributo de clase

    ...

    @classmethod # Decorador
    def especie_info(cls):
        return cls.especie

    @classmethod # Decorador
    def factory(cls, nombre):
        return cls(nombre, 1)
```

```python
Perro.especie_info() # "Canis lupus"
nuevo_perro = Perro.factory("Coco")
print(nuevo_perro) # "Perro(Coco, 1)"
print(nuevo_perro.name) # "Coco"
```

**Métodos útiles:**

```python
mi_perro.__dict__           # {'_Perro__nombre': 'Noa', 'edad': 6}
isinstance(mi_perro, Perro) # True
type(mi_perro)              # <class '__main__.Perro'>
```

```python
dir(mi_perro)
# ['_Perro__nombre', '__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'edad', 'especie', 'hablar']
```

## Herencia

```python
class Perro:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def ladrar(self):
        print("¡Guau!")

class PerroDeTrabajo(Perro):  # Hereda de Perro
    def __init__(self, nombre, edad, tarea):
        super().__init__(nombre, edad)
        self.tarea = tarea

    def trabajar(self):  # Nuevo método
        print(f"{self.nombre} está haciendo: {self.tarea}")
```

```python
gala = PerroDeTrabajo("Gala", 6, "Guiar")
gala.ladrar()     # "¡Guau!"
gala.trabajar()   # "Gala está haciendo: Guiar"
```

### **Herencia multi-nivel**

Una clase hereda de una clase que ya hereda de otra.

_No se recomienda hacerlo con más de dos niveles._

```python
class Animal():
    def comer(self):
        print("Estoy comiendo")

class Perro(Animal):  # Hereda de Animal
    def ladrar(self):
        print("¡Guau!")

class PerroDeTrabajo(Perro):  # Hereda de Perro
    def trabajar(self):
        print("Estoy trabajando")
```

```python
kira = PerroDeTrabajo()
kira.comer()    # Estoy comiendo (heredado de Animal)
kira.ladrar()   # ¡Guau!
kira.trabajar() # Estoy trabajando
```

### **Herencia múltiple**

Una clase herda de **dos o más clases**.

_Útil pero requiere cuidado con el orden de resolución (MRO: Method Resolution Order)._

```python
class Nadador:
    def nadar(self):
        print("Estoy nadando")

class Volador:
    def volar(self):
        print("Estoy volando")

class Pato(Nadador, Volador):  # Hereda de ambas
    def graznar(self):
        print("Cuac")
```

```python
lucas = Pato()
lucas.nadar()   # Estoy nadando
lucas.volar()   # Estoy volando
lucas.graznar() # Cuac
```

## Polimorfismo

```python
class Gato:
    def hablar(self):
        print("¡Miau!")

class Canario:
    def hablar(self):
        print("¡Pío!")

def hacer_hablar(animal):
    animal.hablar()
```

```python
hacer_hablar(gala)  # "¡Guau!"
hacer_hablar(Gato())  # "¡Miau!"
hacer_hablar(Canario())  # "¡Pío!"
```

<a name="abstraccion"></a>

## Abstracción

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def hablar(self):
        pass
```

```python
class Perro(Animal):
    def hablar(self):
        print("¡Guau!")

Perro().hablar()  # ¡Guau!
```

<a name="ducktypes"></a>

## Duck Types

_"Si camina como un pato y habla como un pato, entonces es un pato."_

Python no exige que heredes de interfaces, solo que tu clase implemente ciertos métodos especiales (`__eq__`, `__hash__`, `__lt__`, etc.).

### Comparable

```python
class MyComparable:
    def __init__(self, a):
        self.a = a
    def __eq__(self, other):
        if isinstance(other, type(self)):
            return self.a == other.a
        return NotImplemented
```

### Hashable

```python
class MyHashable:
    def __init__(self, a):
        self._a = a
    def __eq__(self, other):
        return isinstance(other, type(self)) and self._a == other._a
    def __hash__(self):
        return hash(self._a)
```

### Sortable (ordenable)

```python
from functools import total_ordering

@total_ordering
class MySortable:
    def __init__(self, a):
        self.a = a
    def __eq__(self, other):
        return self.a == other.a
    def __lt__(self, other):
        return self.a < other.a
```

### Iterador personalizado

```python
class Counter:
    def __init__(self):
        self.i = 0
    def __next__(self):
        self.i += 1
        return self.i
    def __iter__(self):
        return self
```

```python
counter = Counter()
next(counter), next(counter), next(counter)  # (1, 2, 3)
```

### Callable (invocable)

```python
class Counter:
    def __init__(self):
        self.i = 0
    def __call__(self):
        self.i += 1
        return self.i
```

```python
counter = Counter()
counter(), counter(), counter()  # (1, 2, 3)
```

### Context Manager personalizado

```python
class MyOpen:
    def __init__(self, filename):
        self.filename = filename
    def __enter__(self):
        self.file = open(self.filename)
        return self.file
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.file.close()
```

```python
with MyOpen('example.txt') as f:
    print(f.read())
```

<a name="concurrencia"></a>

# Concurrencia

### `threading`

```python
import threading
import time

def crawl(link, delay=3):
    print(f"crawl started for {link}")
    time.sleep(delay)  # Bloqueante I/O (simulando una petición de red)
    print(f"crawl ended for {link}")

links = [
    "https://python.org",
    "https://docs.python.org",
    "https://peps.python.org",
]

# Iniciar hilos para cada enlace
threads = []
for link in links:
    # Usando `args` para pasar argumentos posicionales y `kwargs` para pasar argumentos nombrados
    t = threading.Thread(target=crawl, args=(link,), kwargs={"delay": 2})
    threads.append(t)

# Iniciar cada hilo
for t in threads:
    t.start()

# Espera a que todos los hilos terminen
for t in threads:
    t.join()
```

> 🔗 Más información: [`threading` - Docs Python](https://docs.python.org/es/3.13/library/threading.html)

### `multiprocessing`

```python
from multiprocessing import Process
import os

def info(title):
    print(title)
    print('module name:', __name__)
    print('parent process:', os.getppid())
    print('process id:', os.getpid())

def f(name):
    info('function f') # Información de la función
    print('hello', name) # Salida de la función

if __name__ == '__main__':
    info('main line') # Información del proceso principal
    p = Process(target=f, args=('Rocío',)) # Crear proceso
    p.start() # Iniciar proceso
    p.join() # Esperar a que el proceso termine
```

> 🔗 Más información: [`multiprocessing` - Docs Python](https://docs.python.org/es/3.13/library/multiprocessing.html)

### `asyncio`

```python
import asyncio

async def main():
    print("Hola...")
    await asyncio.sleep(1)
    print("Rocío!")

asyncio.run(main()) # Iniciar proceso
```

> 🔗 Más información: [`asyncio` - Docs Python](https://docs.python.org/es/3.13/library/asyncio.html)

# Red y correo

### `webbrowser`

```python
import webbrowser

url = 'https://docs.python.org/'

# Abrir URL en una nueva pestaña, si la ventana del navegador está abierta
webbrowser.open_new_tab(url)

# Abrir URL en una nueva ventana, independientemente de si la ventana del navegador está abierta
webbrowser.open_new(url)
```

> 🔗 Más información: [`webbdrowser` - Docs Python](https://docs.python.org/es/3.13/library/webbrowser.html)

### `smtplib`

```python
import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
from email.mime.image import MIMEImage
from pathlib import Path

path = Path("ruta/a/la/imagen.jpg")
mime_image = MIMEImage(path.read_bytes()) # Convertir imagen a bytes
mensaje = MIMEMultipart()
mensaje['From'] = 'rociodev@gmail.com'
mensaje['To'] = 'rociodev@gmail.com'
mensaje['Subject'] = 'Asunto del correo'
cuerpo = 'Contenido del correo'
mensaje.attach(MIMEText(cuerpo, 'plain'))
mensaje.attach(mime_image) # Añadir imagen al correo

with smtplib.SMTP('smtp.gmail.com', 587) as smtp: # host, puerto
    smtp.ehlo() # Identificar el servidor
    smtp.starttls() # Encriptar la conexión
    smtp.login('rociodev@gmail.com', 'password') # Iniciar sesión (usuario, contraseña)
    smtp.send_message(mensaje) # Enviar correo
    smtp.quit() # Cerrar conexión
```

> 🔗 Más información: [`smtplib` - Docs Python](https://docs.python.org/es/3.13/library/smtplib.html)

#### **Uso de plantillas**

```python
from string import Template
from email.mime.text import MIMEText

plantilla = """
    <b>Hola, $nombre</b>
    <p>Este es un correo de prueba</p>
"""
template = Template(plantilla)
cuerpo = template.substitute(nombre="Rocío") # "<b>Hola, Rocío</b>"
...
mensaje.attach(MIMEText(cuerpo, 'html')) # ya no es texto plano, ahora es html
```

También podemos importar la plantilla desde un archivo (`.html`):

```python
from pathlib import Path
from string import Template

plantilla = Path("carpeta/plantilla.html").read_text()
template = Template(plantilla)
...
```

### `socket`

```python
addr = ("", 8080)  # all interfaces, port 8080
if socket.has_dualstack_ipv6():
    s = socket.create_server(addr, family=socket.AF_INET6, dualstack_ipv6=True)
else:
    s = socket.create_server(addr)
```

> 🔗 Más información: [`socket` - Docs Python](https://docs.python.org/es/3.13/library/socket.html)

### `requests`

```python
import requests

url = "https://api.github.com/users/octocat"
response = requests.get(url)
response.json()
```

### `ftp`

```python
import ftplib

ftp = ftplib.FTP("ftp.example.com")
ftp.login("username", "password")
ftp.retrlines("LIST")
```

> 🔗 Más información: [`ftplib` - Docs Python](https://docs.python.org/es/3.13/library/ftplib.html)

<a name="entornos-dependencias"></a>

# Módulos, entornos y dependencias

<a name="modulos"></a>

## Módulos

```python
import <nombre_modulo>
import <nombre_modulo> as m
from <nombre_modulo> import <nombre_funcion>
from <nombre_modulo> import <nombre_funcion>, <nombre_funcion>
from <nombre_modulo> import <nombre_funcion> as m_function
from <nombre_modulo> import *   # no recomendado
```

### Módulos vs Paquetes

- Un **módulo** es un **archivo** `.py`.
- Un **paquete** es una **carpeta** que contiene módulos y un archivo `__init__.py`.

```bash
├── app.py
├── mi_paquete
│   ├── __init__.py
│   ├── modulo1.py
│   └── modulo2.py
```

```python
# modulo1.py
def funcion1():
    print("Funcion 1")

# modulo2.py
def funcion2():
    print("Funcion 2")

# __init__.py
from .modulo1 import funcion1
from .modulo2 import funcion2
```

```python
# app.py
from mi_paquete import modulo1, modulo2
modulo1.funcion1() # "Funcion 1"
modulo2.funcion2() # "Funcion 2"
```

También se puede importar directamente desde el módulo:

```python
# app.py
from mi_paquete.modulo1 import funcion1
from mi_paquete.modulo2 import funcion2
funcion1() # "Funcion 1"
funcion2() # "Funcion 2"
```

### Subpaquetes

```bash
├── app.py
├── mi_paquete
│   ├── __init__.py
│   ├── modulo1.py
│   └── subpaquete
│       ├── __init__.py
│       └── modulo3.py
```

```python
# modulo3.py
def funcion3():
    print("Funcion 3")
```

```python
# __init__.py
from .subpaquete.modulo3 import funcion3
```

```python
# app.py
from mi_paquete.subpaquete.modulo3 import funcion3
funcion3() # "Funcion 3"
```

```python
# modulo3.py
from ..modulo1 import funcion1  # Importar módulo desde el sub-paquete
```

> 🔗 La **importación dinámica de paquetes** se explica en la sección [_"Lectura y escritura de archivos: Import dinámico de paquetes"_](#import-dinámico-de-paquetes), a continuación de `pathlib`.

### Import condicionales

```python
# modulo3.py
if __name__ != "__main__":
    from ..modulo1 import funcion1
```

### `dir()`

```python
import numpy
dir(numpy) # Lista de nombres definidos en el módulo
```

```python
# Sintaxis
print(paquete.modulo.__<atributo,función,clase,etc.>__)
```

```python
print(numpy.__doc__)     # Documentación del módulo
print(numpy.__name__)    # Nombre del módulo
print(numpy.__package__) # Nombre del paquete
print(numpy.__version__) # Versión del módulo
print(numpy.__path__)    # Ruta del paquete
print(numpy.__file__)    # Ruta del archivo del módulo
```

<a name="env"></a>

## Entornos virtuales

Entorno aislado donde puedes instalar paquetes sin afectar el entorno global.

### **Crear entorno virtual**

```bash
python3 -m venv <nombre_entorno>
```

```bash
python3 -m venv env
```

### **Activar entorno virtual**

```bash
# En macOS/Linux
source env/bin/activate

# En Windows
env\Scripts\activate
```

### **Desactivar entorno**

```bash
deactivate
```

### **Eliminar entorno**

```bash
rm -r env  # Basta con borrar la carpeta del entorno virtual
```

<a name="pip"></a>

## `pip` y `requirements.txt`

- `pip` es el gestor de paquetes oficial de Python.
- `requirements.txt` es un archivo que contiene los paquetes y versiones necesarios para el proyecto.

### **Instalar paquetes**

```bash
pip install nombre_paquete
pip install nombre_paquete==version
pip install 'nombre_paquete==2.8.*'  # Instalar la última versión de 2.8
pip install 'nombre_paquete==2.*'    # Instalar la última versión de 2
```

Para instalar una versión anterior, primero debemos desintalar el paquete con la versión actual y después instalar la versión deseada con `pip install nombre_paquete==version`.

### **Ver paquetes instalados**

```bash
pip list
```

### **Actualizar paquetes**

```bash
pip install --upgrade nombre_paquete
```

Para verificar la actualización:

```bash
nombre_paquete --version
```

### **Desinstalar paquetes**

```bash
pip uninstall nombre_paquete
```

### **Crear archivo `requirements.txt`** _(Guardar dependencias)_

```bash
pip freeze > requirements.txt
```

### **Instalar paquetes desde `requirements.txt`**

```bash
pip install -r requirements.txt
```

## `pipenv`

```bash
pipenv install nombre_paquete
```

🔗 [Documentación `pipenv`](https://pipenv-es.readthedocs.io/es/latest/)

Activar el entorno virtual:

```bash
pipenv shell
```

Desactivar el entorno virtual:

```bash
exit
```

Saber dónde está almacenado el entorno virtual:

```bash
pipenv --venv
```

<a name="poetry"></a>

## `poetry`

```bash
poetry add nombre_paquete
```

🔗 [Documentación Poetry](https://python-poetry.org/)

<br>

<a name="io-archivos"></a>

# I/O y sistema de archivos

<a name="lectura-escritura-archivos"></a>

## Lectura y escritura de archivos

Para leer y escribir archivo puedes usar [`with`y `open`](#lectura-escritura-open") o [`Path`](#lectura-escritura-path")

### Lectura y escritura con `open`

```python
from io import open

texto = "Hola mundo!"
archivo = open("directorio/archivo.txt", mode="w", encoding=None)
... # write, read, readlines...
archivo.close() # Es necesario cerrar el archivo
```

```python
# Modo escritura
archivo = open("directorio/archivo.txt", "w") # Si el archivo no existe, lo crea
archivo.write(texto)
archivo.writelines(listado_texto) # pasar listado_texto = archivo.readlines()
```

```python
# Modo lectura
archivo = open("directorio/archivo.txt", "r")
texto = archivo.read()       # lee todo el contenido del archivo como una cadena
texto = archivo.readlines()  # devuelve una lista de líneas
```

#### **Modos**

- `r` - Lectura (por defecto)
- `w` - Escritura. Si el archivo no existe, lo crea
- `x` - Escritura o falla si el archivo ya existe
- `a` - Agregar, añadir
- `w+` - Lectura y escritura
- `r+` - Lectura y escritura desde el principio
- `a+` - Lectura y escritura desde el final. Si el archivo no existe, lo crea
- `t` - Modo texto
  - `rt` - Modo lectura de texto
  - `wt` - Modo escritura de texto
  - `at` - Modo anexado de texto
- `b` - Modo binario
  - `rb` - Modo lectura binaria
  - `wb` - Modo escritura binaria
  - `ab` - Modo anexado binario

```python
archivo.seek(0) # Se desplaza al inicio del archivo
```

```python
archivo.mode      # Modo de apertura del archivo
archivo.name      # Nombre del archivo
archivo.closed    # True si el archivo está cerrado
archivo.encoding  # Codificación del archivo
archivo.newlines  # Número de nuevas líneas
archivo.softspace # True si el archivo está cerrado
```

<a name="open"></a>

### Lectura y escritura con `with`

```python
# Leer archivo completo
with open("ruta-archivo/archivo.txt", "r", encoding="utf-8") as f:
    contenido = f.read()

# Leer líneas como lista
with open("ruta-archivo/archivo.txt", "r", encoding="utf-8") as f:
    lineas = f.readlines()    # Lee todas las líneas
    next_line = f.reafline()  # Lee la siguiente línea como una cadena
    line = f.readline(10)     # Lee los primeros 10 caracteres de la primera línea

# Escribir (sobrescribe)
with open("ruta-archivo/archivo.txt", "w") as f:
    f.write("Hola mundo")

# Añadir (append)
with open("ruta-archivo/archivo.txt", "a") as f:
    f.write("\nNueva línea")

# Escritura de múltiples líneas
with open("ruta-archivo/archivo.txt", "w") as f:
    f.writelines(["Línea 1\n", "Línea 2\n"])
```

- El uso de `with` asegura que el archivo se **cierre automáticamente** _(mejor práctica)_.
- Usa `"rb"` / `"wb"` para archivos binarios.

#### **Leer texto de un archivo**

```python
def read_file(nombre_archivo):
    with open('ruta-archivo/nombre_archivo.txt', encoding='utf-8') as file:
        return file.readlines()

for line in read_file(nombre_archivo):
    print(line)
```

#### **Leer y copiar contenido de un archivo a otro**

```python
with open('ruta-archivo/nombre_archivo.txt', 'r') as source_file:
    with open('ruta-archivo/nombre_archivo_copia.txt', 'w') as destination_file:
        for line in source_file:          # Procesa cada línea
            destination_file.write(line)  # Copia línea a línea
```

#### **Escribir múltiples líneas en un archivo usando una lista**

```python
lineas = ["Esta es la línea 1", "Esta es la línea 2", "Esta es la línea 3"]

# nuevo archivo Example.txt para escribit
with open('Example.txt', 'w') as file:
    for linea in lineas:
        file.write(linea + "\n")
    # file se cierra automáticamente cuando el bloque 'with' termina
```

#### **Agregar datos a un archivo existente**

```python
new_data = "Esta es la línea R"

# Abrir un archivo existente Example2.txt para agregar datos
with open('Example2.txt', 'a') as file1:
    file1.write(new_data + "\n")  # Línea agregada al final del archivo
```

### Lectura y escritura con `Path`

```python
from pathlib import Path

archivo = Path("archivo.txt")

archivo.read_text()                 # Leer archivo completo
archivo.read_text().split("\n")     # Leer archivo y dividir el string
archivo.read_text(encoding="utf-8") # Leer archivo con codificación
archivo.write_text("Hola mundo")    # Escribir archivo
```

```python
texto = archivo.read_text("utf-8").split("\n") # Leer con codificación y dividir
text.insert(0, "Hola mundo!")                  # Añadir texto al inicio
archivo.write_text("\n".join(texto), "utf-8")  # Escribir sobre el archivo (manipular string)
```

_`Path` se explica a continuación._

> 🔗 Para el manejo de **archivo CSV y JSON**, puedes consultar las **secciones [_`CSV`_](#csv) y [_`JSON`_](#json).**

<a name="rutas-y-directorios"></a>

## Rutas y directorios

### `pathlib`

`pathlib` es más limpio, multiplataforma y expresivo. Reemplaza a `os.path` y parte de `os` para rutas.

#### **Rutas:**

```python
from pathlib import Path

ruta = Path("carpeta/archivo.txt")

ruta.exists()      # True si existe
ruta.is_file()     # True si es archivo
ruta.is_dir()      # True si es carpeta
ruta.parent        # Carpeta superior (directorio padre)
ruta.name          # Nombre del archivo
ruta.stem          # Nombre sin extensión
ruta.suffix        # Extensión (.txt)
ruta.absolute()    # Ruta absoluta

# Crear carpeta
Path("nueva_carpeta").mkdir(parents=True, exist_ok=True)

# Leer contenido
Path("archivo.txt").read_text(encoding="utf-8")

# Escribir
Path("archivo.txt").write_text("Texto nuevo")
```

```python
# En Windows
Path(r"C:\Users\Usuario\Desktop\archivo.txt") # 'r' -> raw string (evitar caracteres especiales)
```

```python
p = ruta.with_name("nuevo_nombre.txt")
print(p)  # 'carpeta/nuevo_nombre.txt'
```

```python
p = ruta.with_suffix(".bat")
print(p)  # 'carpeta/archivo.bat'
```

```python
p = ruta.with_stem("nuevo_nombre")
print(p)  # 'carpeta/nuevo_nombre.txt'
```

#### **Directorios:**

```python
from pathlib import Path

path = Path("carpeta")

path.exists()                # True si existe
path.mkdir()                 # Crear directorio
path.rmdir()                 # Eliminar directorio (debe estar vacío)
path.rename("nuevo-nombre")  # Renombrar directorio
```

```python
# Iterar sobre archivos en el directorio
for file in path.iterdir():
    print(file) # 'carpeta/archivo.txt'
```

```python
# Filtrar archivos
archivos = [p for p in path.iterdir() if not p.is_dir()]
print(archivos)  # [PosixPath('carpeta/archivo.txt'), PosixPath('carpeta/archivo2.txt')]
```

```python
archivos = [p for p in path.glob("*.py")]     # No recursivo (solo en la carpeta)
archivos = [p for p in path.glob("**/*.py")]  # Recursivo (subcarpetas)
archivos = [p for p in path.rglob("*.py")]    # Recursivo (subcarpetas)
print(archivos)  # [PosixPath('carpeta/archivo.py'), PosixPath('carpeta/archivo2.py')]

archivos = [p for p in path.glob("01-*.py")]  # Patrón de nombre
print(archivos)  # [PosixPath('carpeta/01-archivo.py')]
```

#### **Gestión de archivos:**

```python
from pathlib import Path

archivo = Path('archivos/archivo.txt')

archivo.exists() # True si existe
archivo.rename() # Renombra el archivo
archivo.unlink() # Eliminar archivo o enlace simbólico
archivo.stats()  # Muestra estadísticas
```

#### **Import dinámico de paquetes:**

```python
# archivo-inyeccion-dependencias.py
from pathlib import Path
import db
import api
import graphql

path = Path()
paths = [p for p in path.iterdir() if p.is_dir()]

dependencias = {
    "db": db,
    "api": api,
    "graphql": graphsql
}

def load(p):
    paquete = __import__(str(p).replace("/", "."))
    try:
        paquete.init(**dependecias)
    except:
        print("El paquete no tiene función init")

list(map(load,paths))
```

```python
# modulo1/__init__.py
def init(db, api, **_):
    print(f"{db},{api}")
```

```python
# modulo2/__init__.py
def init(graphql, **_):
    print(f"{graphql}")
```

<a name="csv"></a>

## `csv`

```python
import csv

# Lectura
with open('carpeta/archivo.csv', encoding='urf-8') as archivo: # Modo lectura por defecto
    return csv.reader(archivo, delimiter=';')  # Este objeto se puede iterar

with open('carpeta/archivo.csv', encoding='urf-8') as archivo: # Modo lectura por defecto
    reader = csv.reader(archivo, delimiter=';')
    return list(reader)  # O pasarlo como una lista

with open('carpeta/archivo.csv', encoding='urf-8') as archivo: # Modo lectura por defecto
    reader = csv.reader(archivo, delimiter=';')
    for linea in reader:
        print(linea)  # Mostrar línea a línea
```

```python
# Escritura
def write_to_csv_file(nombre_archivo, rows)
    with open(nombre_archivo, 'w', encoding='urf-8') as archivo:
        writer = csv.writer(archivo, delimiter=';')
        writer.writerow()
        writer.writerows(rows)
```

```python
import os

# Actualizar CSV
with open('carpeta/archivo.csv') as r, open('carpeta/archivo_temporal.csv', 'w') as w:
    reader = csv.reader(r)
    writer = csv.writer(w)
    for linea in reader:
        if linea[0] == "826": # supongamos que es el ID del usuario
            writer.whiterow([826, 'Rocío', 'texto modificado'])
        else:
            writer.writerow(linea)
    os.remove('carpeta/archivo.csv')
    os.rename('carpeta/archivo_temp.csv', 'carpeta/archivo.csv')
```

```python
# Escribe el DataFrame en un archivo CSV
df.to_csv("output.csv", index=False)
```

## `excel`

```python
# Lee datos de un archivo de Excel y crea un DataFrame
df = pd.read_excel("nombre_archivo.xlsx")
```

<a name="json"></a>

## `json`

```python
import json

# Codificación
json.dumps("\"foo\bar") # "\"foo\bar"
json.dumps({"c": 0, "b": 0, "a": 0}, sort_keys=True)) # {"a": 0, "b": 0, "c": 0}

# Mejor visualización
json.dumps({'6': 7, '4': 5}, sort_keys=True, indent=4)
# {
#     "4": 5,
#     "6": 7
# }

# Decodificación JSON
json.loads('["rocio", {"bar":["baz", null, 1.0, 2]}]') # ['rocio', {'bar': ['baz', None, 1.0, 2]}]
json.loads('"\\"foo\\bar"') # '"foo\x08ar'
```

🔗 Más información: [`json` - Docs Python](https://docs.python.org/es/3/library/json.html)

<a name="html-xml"></a>

## `html / xml`

🔗 Más información: [`html` - Docs Python](https://docs.python.org/es/3.13/library/html.parser.html)

<a name="zipfile"></a>

## Archivos comprimidos - `zipfile`

```python
from zipfile import ZipFile

# Escritura
with ZipFile("archivos/comprimidos.zip", "w") as zip:
    for path in Path().rglob("*.*"):   # Cualquier archivo (cualquier nombre, cualquier extensión)
        if str(path) != "archivos/comprimidos.zip":
            zip.write(path)

# Lectura
with ZipFile("archivos/comprimidos") as zip:
    print(zip.namelist())  # Muestra los archivos comprimidos
    info = zip.getinfo("archivos/comprimidos.py")
    print(
        info.file_size,      # Tamaño del archivo original
        info.compress_size   # Tamaño del archivo comprimido
    )
    zip.extractall("archivos/descomprimidos") # Extrae los archivos comprimidos
```

<a name="tarfile"></a>

## `tarfile`

🔗 Más información: [`tarfile` - Docs Python](https://docs.python.org/es/3/library/tarfile.html)

<a name="files"></a>

## `os, sys`

### `os` _(Operating System)_ - Interacción con el sistema operativo

```python
import os

os.name               # 'posix' (Unix) o 'nt' (Windows)
os.getenv("HOME")     # Obtener variable de entorno
os.environ["X"] = "1" # Establecer variable
os.system("ls -la")   # Ejecuta comando del sistema
```

### `sys` _(System)_ - Interacción con el intérprete de Python

```python
import sys

sys.argv     # Argumentos del script (como lista)
sys.exit()   # Finaliza el programa (salir del programa)
sys.path     # Rutas de búsqueda de módulos
sys.version  # Versión de Python
```

<a name="subprocess"></a>

## `subprocess`

Ejecuta comandos del sistema en Python.

```python
import subprocess

# Ejecutar y capturar salida
result = subprocess.run(["ls", "-la"], capture_output=True, text=True)
print(result.stdout)
```

```python
# Ejecutar con control de error
subprocess.run(["mkdir", "carpeta"], check=True)
```

```python
# Redireccionar entrada/salida
with open("salida.txt", "w") as f:
    subprocess.run(["echo", "Hola"], stdout=f)
```

> Usa `subprocess.run()` en lugar de `os.system()` para mayor control y seguridad.

<br>

<a name="bbdd"></a>

# Bases de datos

<a name="sqlite3"></a>

## `sqlite3`

```python
import sqlite3

conexion = sqlite3.connect("base_de_datos.db")
cursor = conexion.cursor() # Actúa como un intermediario entre el código y la base de datos

# Ejecutar la consulta SQL
cursor.execute(
    """
    CREATE TABLE IF NOT EXISTS usuarios (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        nombre VARCHAR(50),
        email VARCHAR(100)
    )
    """
)
conexion.commit()  # Guardar los cambios
conexion.close()   # Cerrar siempre la conexión
```

### `with`

```python
import sqlite3

with sqlite3.connect("base_de_datos.db") as conexion:
    cursor = conexion.cursor()
    cursor.execute(
        """
        CREATE TABLE IF NOT EXISTS usuarios (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            nombre VARCHAR(50),
            email VARCHAR(100)
        )
        """
    )
```

`with` asegura que la conexión se cierre y los cambios se guarden automáticamente.

### `insert`

```python
cursor.execute(
    "INSERT INTO users (name, email) VALUES (?, ?)", # Consulta SQL con placeholders
    ("Rocío", "rocio@example.com") # Tupla de valores
)
```

```python
users = [
    ("Rocío", "rocio@example.com"),
    ("Ana", "ana@example.com"),
    ("Juan", "juan@example.com")
]
cursor.executemany(  # Ejecuta la consulta SQL para cada valor de la lista (insert many)
    "INSERT INTO users (name, email) VALUES (?, ?)",
    users
)
```

No se incluyen los valores directamente en la consulta SQL para prevenir un **SQL Injection**.

### `select`

```python
cursor.execute("SELECT * FROM usuarios")
print(cursor.fetchall())    # Muestra todos los resultados
print(cursor.fetchone())    # Muestra el primer resultado
print(cursor.fetchmany(2))  # Muestra los siguientes 2 resultados
```

<a name="mysql-postgresql"></a>

## MySQL / PostgreSQL

🔗 [PostgreSQL](https://www.postgresql.org/)

<a name="orm"></a>

## ORM

🔗 [Full Stack Python - Object-relational Mappers (ORMs)](https://www.fullstackpython.com/object-relational-mappers-orms.html)

<br>

<a name="testing-debugging"></a>

# Testing y debugging

<a name="assert"></a>

## `assert`

```python
assert 1 == 1 # No hace nada
assert 1 == 2 # Lanza un AssertionError
assert False, "La condición es falsa" # Lanza un AssertionError con el mensaje


# Testing
assert(calcula_media([5, 10, 7.5]) == 7.5) # True
assert(calcula_media([4, 8]) == 6) # False

# Funciones
def suma(a, b):
    assert(type(a) == int and type(b) == int) # Comprueba que los argumentos sean enteros
    return a + b

assert(suma(1, 2))     # Ok
assert(suma(1, "2"))   # Lanza un AssertionError
assert(suma(3.0, 2.0)) # Lanza un AssertionError
```

> 🔗 Más información: [`assert` - Docs Python](https://docs.python.org/es/3.13/reference/simple_stmts.html#assert)

<a name="logging"></a>

## Logging

```python
import logging

logging.basicConfig(level=logging.DEBUG)
logging.debug("Mensaje de depuración")
logging.info("Mensaje informativo")
logging.warning("Mensaje de advertencia")
logging.error("Mensaje de error")
logging.critical("Mensaje crítico")
```

> 🔗 Más información: [`logging` - Docs Python](https://docs.python.org/es/3.13/library/logging.html)

<a name="unittest"></a>

## `unittest`

```python
import unittest

class TestStringMethods(unittest.TestCase):
    def test_upper(self):
        self.assertEqual("foo".upper(), "FOO")

    def test_isupper(self):
        self.assertTrue('FOO'.isupper())
        self.assertFalse('Foo'.isupper())

    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
        # comprobar que s.split falla cuando el separador no es una cadena
        with self.assertRaises(TypeError):
            s.split(2)

if __name__ == "__main__":
    unittest.main()
```

<a name="pytest"></a>

## `pytest`

```python
import pytest

def funcion(x):
    return x + 1

def funcion_a_testear():
    assert funcion(3) == 5 # Lanza un AssertionError
    assert funcion(4) == 5 # No lanza un AssertionError
```

🔗 [Documentación de pytest](https://docs.pytest.org/en/stable/)

<br>

<a name="fecha-tiempo-math"></a>

# Fechas, números y texto

<a name="time"></a>

## `time`

```python
import time

time.time()    # Devuelve el tiempo actual en segundos
time.sleep(1)  # Pausa el programa por 1 segundo
```

<a name="datetime"></a>

## `datetime`

```python
for datetime import datetime

# Crear fechas
datetime(2025, 1, 1)  # Devuelve la fecha 1 de enero de 2025
datetime.now()        # Devuelve la fecha y hora actual
datetime.strptime("2025-01-01", "%Y-%m-%d")  # Devuelve la fecha 1 de enero de 2025
datetime.now().strftime("%Y-%m-%d %H:%M:%S") # Devuelve la fecha y hora actual en formato string
```

**Directivas de formato:**

- `%Y`: Año con siglo
- `%m`: Mes
- `%d`: Día
- `%H`: Hora
- `%M`: Minuto
- `%S`: Segundo
- `%f`: Microsegundo
- `%z`: Desplazamiento UTC
- `%Z`: Zona horaria
- `%j`: Día del año
- `%U`: Semana del año (0-53)
- `%W`: Semana del año (0-53)
- `%a`: Nombre del día (minúsculas)
- `%A`: Nombre del día (mayúsculas)
- `%b`: Nombre del mes (minúsculas)
- `%B`: Nombre del mes (mayúsculas)
- `%c`: Fecha y hora local
- `%x`: Fecha local
- `%X`: Hora local

```python
# Comparar fechas
fecha1 = datetime.strptime("2025-01-01", "%Y-%m-%d")
fecha2 = datetime.strptime("2025-01-02", "%Y-%m-%d")

print(fecha1 < fecha2)  # True
```

```python
# Ver año, mes, día, hora, minuto, segundo de una fecha
print(
    fecha.year     # 2025
    fecha.month    # 1
    fecha.day      # 1
    fecha.hour     # 0
    fecha.minute   # 0
    fecha.second   # 0
)
```

### `timedelta`

```python
from datetime import timedelta

timedelta(days=1)  # Devuelve un intervalo de tiempo de 1 día

delta = fecha1 - fecha2      # Devuelve un intervalo de tiempo entre las dos fechas
print(delta)                 # 1 day, 0:00:00
print(delta.days)            # 1
print(delta.seconds)         # 0
print(delta.microseconds)    # 0
print(delta.total_seconds()) # 86400.0
```

```python
from datetime import datetime, timedelta

fecha1 = datetime.now()
fecha2 = fecha1 + timedelta(days=1) # Sumar un día a la fecha actual
fecha3 = fecha1 - timedelta(weeks=2) # Restar dos semanas a la fecha actual
print(fecha2)  # 2025-01-02 00:00:00
print(fecha3)  # 2024-12-18 00:00:00
```

<a name="math"></a>

## `math`

```python
import math

math.pi           # Devuelve el número pi
math.sqrt(9)      # Devuelve la raíz cuadrada de 9
math.ceil(2.1)    # Devuelve el número 3
math.floor(2.9)   # Devuelve el número 2
math.factorial(5) # Devuelve el factorial de 5
math.pow(2, 3)    # Devuelve 2 elevado a 3
math.log(10)      # Devuelve el logaritmo natural de 10
math.exp(1)       # Devuelve e elevado a 1
```

<a name="random"></a>

## `random`

```python
import random

random.random()                       # Número aleatorio entre 0 y 1
random.randint(1, 10)                 # Número aleatorio entre 1 y 10
random.choice([1, 2, 3, 4, 5])        # Elemento aleatorio de la lista
random.choices([1, 2, 3, 4, 5], k=3)  # Lista de 3 elementos aleatorios de la lista
random.shuffle([1, 2, 3, 4, 5])       # Mezcla los elementos de la lista
```

```python
import string

string.ascii_letters    # Devuelve todas las letras del alfabeto
string.ascii_lowercase  # Devuelve todas las letras minúsculas del alfabeto
string.ascii_uppercase  # Devuelve todas las letras mayúsculas del alfabeto
string.digits           # Devuelve todos los dígitos del 0 al 9
string.punctuation      # Devuelve todos los caracteres de puntuación

chars = string.ascii_letters + string.digits + string.punctuation

seleccion = random.choices(chars, k=10)  # Lista de 10 caracteres aleatorios
print(seleccion) # ['a', '1', '!', 'A', '1', '1', '!', 'a', '1', 'A']

password = "".join(seleccion)
print(password) # a1!A11!a1A
```

<a name="re"></a>

## `re (regex)`

```python
import re

re.match(r"^[a-zA-Z0-9]+$", "123456")    # Devuelve True
re.search(r"^[a-zA-Z0-9]+$", "123456")   # Devuelve True
re.findall(r"^[a-zA-Z0-9]+$", "123456")  # Devuelve ['123456']
```

<a name="webbrowser"></a>

## `webbrowser`

```python
import webbrowser

webbrowser.open("https://www.google.com")
```

<br>

<a name="data-science"></a>

# Data Science

<a name="numpy"></a>

## `numpy`

[NumPy](https://numpy.org/) es una biblioteca para cálculos numéricos en Python.

```bash
pip install numpy
```

```python
import numpy as np
```

```python
a = np.array([0,1,2,3,4])

type(a)   # numpy.ndarray
a.dtype   # dtype('int64')
a.size    # 5
a.ndim    # 1
a.shape   # (5,)
```

```python
b = np.array([20,1,2,3,4])  # array 1D

# Indexación
b[0] = 100   # [100 1 2 3 4]
c = b[1:4]   # Asignar valores de un array a otro array
```

```python
# Suma y resta de vectores
u = np.array([20,1,32,13,24])
v = np.array([10,12,10,8,14])

u + v   # [30 13 42 21 38]
u - v   # [10 -11 22 5 10]
u * v   # [200 12 320 104 336]
u / v   # [2. 0.08333333 3.2 1.625 1.71428571]

# Operaciones con un escalar
u + 10  # [30 11 42 23 34]
u * 2   # [40 2 64 26 48]

# Funciones
u.mean()             # 18.0
u.sum()              # 90
u.max()              # 32
u.min()              # 1
np.pi                # 3.141592653589793
np.linspace(-2,2,5)  # [-2. -1.  0.  1.  2.]

# Dot product (producto punto)
np.dot(u,v)  # 972 -> 20 * 10 + 1 * 12 + 32 * 10 + 13 * 8 + 24 * 14
```

````python
A = np.array([[11, 12, 13], [21, 22, 23], [31, 32, 33]]) # array 2D

A[1,2]    # 23             (acceder al elemento de la 2ª fila, 3ª columna)
A[1][2]   # 23             (acceder al elemento de la 2ª fila, 3ª columna)
A[0][0:2] # array([11,12]) (elementos de la 1ª fila y 1ª y 2ª columnas)
A[0:2][2] # array([13,23]) (elementos de la 1ª y 2ª filas y 3ª columna)


<a name="pandas"></a>

## `pandas`

[Pandas](https://pandas.pydata.org/) es una biblioteca para análisis de datos en Python.

```bash
pip install pandas
````

```python
import pandas as pd
```

### Series

```python
# Crear una Serie desde una lista
data = [10, 20, 30, 40, 50]
s = pd.Series(data)

s         # Imprime la serie
s[2])     # 30
s.iloc[3] # 40
s[1:4]    # [20, 30, 40]
s.values  # array([10, 20, 30, 40, 50])
s.dtype   # dtype('int64')
s.dtypes  # dtype('int64')
s.shape   # (5,)
s.size    # 5
s.mean()  # 30.0
s.sum()   # 150
s.min()   # 10
s.max()   # 50
s.unique()  # [10 20 30 40 50] (valores únicos)
s.nunique() # [5 (número de valores únicos)
```

```python
s = pd.Series([122, 320, 40, 250])

s.sort_index() # ordena por índice
# 0    122
# 1    320
# 2     40
# 3    250

s.sort_values() # ordena por valores
# 2    40
# 0    122
# 3    250
# 1    320

s.isnull()  # verifica si hay valores faltantes (NaN)
# 0    False
# 1    False
# 2    False
# 3    False
# 4    False

s.notnull()  # verifica si no hay valores faltantes (NaN)
# 0    True
# 1    True
# 2    True
# 3    True
# 4    True

s.apply(lambda x: x ** 2)  # Aplica una función personalizada a cada elemento
# 0     14884
# 1    102400
# 2      1600
# 3     62500
```

### DataFrames

```python
file_path = "ruta-archivo/archivo.csv"
df = pd.read_csv(file_path)  # Lee el archivo CSV y lo convierte en un DataFrame

df.shape        # Número de filas y columnas (dimensión del DataFrame)
df.head()       # Primeras 5 filas del DataFrame
df.tail()       # Últimas 5 filas del DataFrame
df.info()       # Información sobre el DataFrame
df.describe()   # Estadísticas descriptivas del DataFrame
df.duplicated() # Valores o registros duplicados o repetitivos
```

```python
songs = {
    "title": ["Song 1", "Song 2", "Song 3"],
    "artist": ["Artist 1", "Artist 2", "Artist 3"],
    "year": [2020, 2021, 2022]
}

df = pd.DataFrame(songs) # Convierte el diccionario en un DataFrame
```

```python
df.iloc[0,0]     # Accede al valor de la fila 0 y columna 0 ('Song 1')
df.iloc[1,0]     # Accede al valor de la fila 1 y columna 0 ('Song 2')
df.iloc[0,:]     # Accede a la fila 0 ('Song 1', 'Artist 1', 2020)
df.iloc[:,0]     # Accede a la columna 0 ('Song 1', 'Song 2', 'Song 3')
df.iloc[0:2,0:2] # Accede a las filas 0 y 1 y a las columnas 0 y 1

df.loc[0, "title"]  # Accede al valor de la fila 0 y columna 'title' ('Song 1')
df.loc[1, "artist"] # Accede al valor de la fila 1 y columna 'artist' ('Artist 2')
```

```python
df[['title', 'artist']] # Selecciona columnas específicas
df[1:3]                 # Selecciona filas específicas
df['year'].unique()     # Elementos únicos en la columna
df[df['year'] > 2021]   # Filtrado condicional
```

```python
# Eliminar filas o columnas del DataFrame
df.drop(["col1", "col2"], axis=1, inplace=True) # Elimina columnas
df.drop(index=[row1, row2], axis=0, inplace=True) # Elimina filas
df.dropna(axis=0, inplace=True) # Elimina filas con valores NaN faltantes
```

```python
# Combinar dos DataFrames basándose en múltiples columnas comunes
merged_df = pd.merge(df1, df2, on=["col1", "col2"])

# Reemplaza valores específicos en una columnas por nuevos valores
df["nombre_columna"].replace(old_value, new_value, inplace=True)
```

```python
# Guarda el DataFrame en un archivo CSV
df.to_csv("ruta-archivo/archivo.csv", index=False)

# Guarda el DataFrame en un archivo Excel
df.to_excel("ruta-archivo/archivo.xlsx", index=False)
```

<a name="matplotlib"></a>

## `matplotlib`

[Matplotlib](https://matplotlib.org/) es una biblioteca para visualización de datos en Python.

```bash
pip install matplotlib
```

```python
import matplotlib.pyplot as plt
```

<a name="seaborn"></a>

## `seaborn`

[Seaborn](https://seaborn.pydata.org/) es una biblioteca para visualización de datos en Python.

```bash
pip install seaborn
```

```python
import seaborn as sns
```

<a name="beatifulsoup4"></a>

## `beautifulsoup4`

[BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) es una biblioteca para analizar HTML y XML.

```bash
pip install beautifulsoup4
```

```python
from bs4 import BeautifulSoup

soup = BeautifulSoup(html_content, 'html.parser')
```

<a name="selenium"></a>

## `selenium`

[Selenium](https://www.selenium.dev/) es una biblioteca para automatización de navegadores.

```bash
pip install selenium
```

```python
from selenium import webdriver

driver = webdriver.Chrome()
driver.get("https://www.google.com")
```

<a name="scipy"></a>

## `scipy`

[SciPy](https://scipy.org/) es una biblioteca para cálculos científicos en Python.

```bash
pip install scipy
```

```python
import scipy

scipy.stats.norm.pdf(0) # Devuelve la densidad de probabilidad de la distribución normal en 0
```

<a name="scikit-learn"></a>

## `scikit-learn`

[Scikit-learn](https://scikit-learn.org/) es una biblioteca para aprendizaje automático en Python.

```bash
pip install scikit-learn
```

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X, y)
```

<a name="tensorflow"></a>

## `tensorflow`

[TensorFlow](https://www.tensorflow.org/) es una biblioteca para aprendizaje automático en Python.

```bash
pip install tensorflow
```

```python
import tensorflow as tf

model = tf.keras.models.Sequential([
    tf.keras.layers.Dense(units=1, input_shape=[1])
])
```

<a name="keras"></a>

## `keras`

[Keras](https://keras.io/) es una biblioteca para aprendizaje automático en Python.

```bash
pip install keras
```

```python
import keras

model = keras.Sequential([
    keras.layers.Dense(units=1, input_shape=[1])
])
```

<a name="otros-paquetes"></a>

# Otros paquetes

### `gdown`

[`gdown`](https://pypi.org/project/gdown/) es una biblioteca para descargar archivos de Google Drive.

```python
import gdown

file_id = "1l_5RK28JRL19wpT22B-DY9We3TVXnnQQ"  # id del archivo en Google Drive
url = f"https://drive.google.com/uc?id={file_id}"

# Descargar el archivo
output = "archivo.csv"
gdown.download(url, output, quiet=False)
```

Después podríamos leer el archivo CSV con Pandas:

```python
import pandas as pd

df = pd.read_csv(output)
df.head()
```

### `ydata-profiling`

[ydata-profiling](https://pypi.org/project/ydata-profiling/) es una biblioteca para generar informes de análisis exploratorio de datos.

```python
import pandas as pd
from ydata_profiling import ProfileReport

# Leer datos
df = pd.read_csv("data.csv")

# Generar informe
profile = ProfileReport(df, title="Profiling Report")

# Guardar el informe en un archivo HTML
profile.to_file("profiling_report.html")
```

```python
# Mostrar el informe en un notebook
profile.to_notebook_iframe()
```
