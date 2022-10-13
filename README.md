
| Alejandro Jimenez | UCSD |
|---------------------|------------------------|
|![](https://avatars.githubusercontent.com/u/7384546?v=4)|![](https://pbs.twimg.com/profile_images/901546652091252736/6Clcdv1L_400x400.jpg)|

# Base-de-Datos-I

## 1 - [Unidad I](#UnidadI)
#### 1.1 - [¿Que es SQL?](#Queessql)
#### 1.2 - [¿Qué es T-SQL?](#QuéesT-SQL)
#### 1.3 - [Microsoft SQL Server](#MicrosoftSQLServer)
#### 1.4 - [UNIDADES DE MEDIDA EN INFORMATICA](#UNIDADESDEMEDIDAENINFORMATICA)
#### 1.5 - [TIPOS DE DATO SQL SERVER](#TIPOSDEDATOSQLSERVER)
#### 1.6 - [Integridad de la Base de Datos](#IntegridaddelaBasedeDatos)
#### 1.7 - [Creacion de nuestra primera Base de datos](#CreaciondenuestraprimeraBasededatos)
#### 1.8 - [**Ejercicio** Crear las Tablas de nuestra Base de datos.](#EjercicioCrearlasTablasdenuestraBasededatos)

#### 2 - [ Comandos SQL para manipulación de registros](#manipulacion)
#### 3 - [ SQL JOIN](#join)

#### 3.1 -[  Practicas](#practicaJoin)


# Unidad I <a name="UnidadI"></a>
## Fudamentos de Estructuras de Datos
#
### **¿Que es SQL?** <a name="Queessql"></a>
#### SQL Structured Query Language en español Lenguaje de consulta Estructurado, es un lenguaje específico utilizado en programación, diseñado para administrar, y recuperar información de sistemas de gestión de bases de datos relacionales.
#### Una de sus principales características es el manejo de álgebra y el cálculo relacional para realizar consultas y obtener información de forma sencilla, y además para realizar cambios en ella.

### **¿Qué es T-SQL?**<a name="QuéesT-SQL"></a>
#### T-SQL (Transact-SQL) es la manera en que se comunican las instrucciones de manipulación de datos que gestiona el usuario con el Servidor; las cuales permiten realizar operaciones claves en SQL Server, como creación y modificación de esquemas de base de datos, inserción y modificación de datos y además la administración del propio Servidor de Base de Datos.

#### Esto se realiza mediante el envío de sentencias e instrucciones en T-SQL que son procesadas por el servidor y los resultados regresan a la aplicación cliente.

#### Transact-SQL incluye características propias de cualquier lenguaje de programación que nos permiten definir:
    Tipos de datos.
    Definición de variables.
    Estructuras de control de flujo.
    Gestión de excepciones.
    Funciones predefinidas.

### Sin embargo no nos permite:
    Crear interfaces de usuario.
    Crear aplicaciones ejecutables.

## **Microsoft SQL Server**<a name="MicrosoftSQLServer"></a>
####  Es un sistema de manejo de bases de datos del modelo relacional, desarrollado por la empresa Microsoft.

#### El lenguaje utilizado (que puede ser ejecutado por línea de comandos o mediante la interfaz gráfica de Management Studio) es Transact-SQL T-SQ


## **UNIDADES DE MEDIDA EN INFORMATICA** <a name="UNIDADESDEMEDIDAENINFORMATICA"></a>

#### La información, al igual que ocurre con el peso o con el volumen, se puede medir. Dependiendo de si tenemos más o menos cantidad de información usaremos unas u otras de las siguientes unidades de medida:

#### **bit (b):** Es la unidad más pequeña de información. La palabra bit proviene de Binary digIT , es decir dígito binario en castellano.Los únicos valores de información que puede contener son 0 y 1.Como vimos en la sección anterior un bit de información almacenado por ejemplo en la memoria RAM equivaldría a un transistor con voltaje bajo si tiene almacenado un 0 o con voltaje normal si tiene almacenado un 1:

![](https://iesalandalus.es/tyc/t1/bitsmemoria.jpg)

#### **Byte (B):**Equivale a 8 bits, y es la cantidad necesaria de bits para almacenar un carácter. Por ejemplo un archivo de texto con 10 caracteres, ocuparía en memoria 10 bytes o lo que es lo mismo 80 bits.
    1 B = 8 bits

#### **Kilobyte (KB):**Un Kilobyte es igual a 1024 Bytes. Esta unidad de medida se usa para expresar la cantidades pequeñas de información.
    1 KB=1024 Bytes= 210 Bytes

#### **Megabyte(MB):**Un Megabytes es igual a 1024 Kilobytes. Se usa para cantidades medianamente grandes de información, por ejemplo para expresar lo que ocupa un archivo de música.
    1 MB= 1024 KB=  220 Bytes

#### **Gigabyte (GB):** Un Gigabye son 1024 Megabytes. Esta unidad se usa para cantidades grandes de información como por ejemplo para expresar la capacidad de un disco duro.
    1 GB= 1024 MB= 230 Bytes

#### **Terabyte (TB):** El Terabyte equivale a 1024 GB. Se utiliza para cantidades enormes de información como para medir la capacidad de almacenamiento de una supercomputadora o de algunos discos duros actuales.
    1 TB= 1024 GB= 240 Bytes


#### En el siguiente esquema vemos un resumen en forma de escalera de cómo hacer las conversiones entre las diferentes unidades de medida de la información, para pasar de una unidad más grande a otra más pequeña,es decir bajar escalones, multiplicaremos y para pasar de una más pequeña a otra mayor, es decir subir escalones, dividiremos:
![](https://iesalandalus.es/tyc/t1/escaleraconversion.jpg)


## TIPOS DE DATO SQL SERVER <a name="TIPOSDEDATOSQLSERVER"></a>

### TIPOS DE DATOS STANDARD (Más utilizados)
#### Numéricos
##### Enteros BIT, TINYINT, SMALLINT, INT, BIGINT
##### Decimales MONEY, DECIMAL
#### Texto y Binarios
##### CHAR, VARCHAR, NCHAR, NVARCHAR
##### BINARY, VARBINARY
#### Fecha y Hora
##### DATE, TIME, DATETIME, SMALLDATETIME

### Descripción de Tipos de Dato y sus tamaños posibles
#### BIT 1 byte
    0 ó 1
    True o False
#### TINYINT 1 byte
    0 a 255
#### SMALLINT 2 bytes
    -2^15 (-32,768) HASTA 2^15-1 (32,767)
#### INT 4 bytes
    -2^31 (-2,147,483,648) HASTA 2^31-1 (2,147,483,647)
#### BIGINT 8 bytes
    -2^63 (-9,223,372,036,854,775,808) HASTA 2^63-1 (9,223,372,036,854,775,807)
#### MONEY 8 bytes
    -922,337,203,685,477.5808 HASTA 922,337,203,685,477.5807

# 
## Integridad de la Base de Datos <a name="IntegridaddelaBasedeDatos"></a>
### PRIMARY KEY
#### Definiciones y reglas generales
##### 1. La clave primaria o primary key, identifica de manera unívoca (única) a cada registro de una tabla.
##### 2. El valor que contiene la columna definida como primary key, debe ser único.
##### 3. El valor debe ser NOT NULL (no permitirá valores nulos)
##### 4. Una tabla puede tener más de un campo PK, a la que llamaremos CLAVE COMPUESTA
##### 5. Sea SIMPLE o COMPUESTA, cada tabla solo podrá tener una clave primaria (PRIMARY KEY)

|IdPaciente|Nombre|Apellido|Email|idPais|
|----------|------|--------|-----|------|
|i|Jorge|Rodriguez|a@a.com|MEX|
|2|Marcelo|Lope Llano|a@a.com|MEX|
|3|Kari|Lopreta|a@a.com|COL|
|4|Juan Manuel|Loerfano|a@a.com|ARG|
|5|Juan Manuel|Perez Lozano|a@a.com|ESP|
|6|Karim|Berragas|a@a.com|PER|
|7|Saul|Lpez Gomez|a@a.com|CHI|



### Definiciones y reglas generales
##### 1. La clave foránea o foreign key, debe ser del mismo tipo de dato que su campo relacionado.
##### 2. El valor del campo definido como FK puede ser NULL
##### 3. Una tabla puede tener más de un campo FK

![](./images/foreingkey.png)


## Restricciones y propiedades de campos


### Usar Transact-SQL
##### Creación de una clave principal en una tabla existente En el ejemplo siguiente se crea una clave principal en la columna TransactionID de la base de datos de AdventureWorks.

Codigo:
~~~sql
ALTER TABLE Production.TransactionHistoryArchive
   ADD CONSTRAINT PK_TransactionHistoryArchive_TransactionID PRIMARY KEY CLUSTERED (TransactionID);
~~~

### Creación de una clave principal en una tabla nueva
##### En el ejemplo siguiente se crea una tabla y se define una clave principal en la columna TransactionID de la base de datos de AdventureWorks.
~~~sql
CREATE TABLE Production.TransactionHistoryArchive1
   (
      TransactionID int IDENTITY (1,1) NOT NULL
      , CONSTRAINT PK_TransactionHistoryArchive1_TransactionID PRIMARY KEY CLUSTERED (TransactionID)
   );
~~~


## Creando Nuestra Primera Base de datos.
#### Se adjunta un video tutorial que le muestra cómo crear una base de datos en Sql Server.

#### Haz el ejercicio paso a paso.
#### **Recuerda que el secreto del éxito está en la perseverancia.**
## [Link Video Creacion de nuestra primera Base de datos](https://www.youtube.com/watch?v=SZprT1ebLcU) <a name="CreaciondenuestraprimeraBasededatos"></a>
![](https://i.ytimg.com/vi/YOaC_TyOrdk/maxresdefault.jpg)

#

## **Ejercicio** Crear las Tablas de nuestra Base de datos. <a name="EjercicioCrearlasTablasdenuestraBasededatos"></a>

### Tabla de pacientes.

~~~sql
CREATE TABLE [dbo].[Paciente](
	[idPaciente] [int] Primary key Identity,
	[nombre] [varchar](50) NULL,
	[apellido] [varchar](50) NULL,
	[fNacimiento] [date] NULL,
	[domicilio] [varchar](50) NULL,
	[idPais] [char](3) NULL,
	[telefono] [varchar](20) NULL,
	[email] [varchar](30) NULL,
	[observacion] [varchar](1000) NULL,
	[fechaAlta] [datetime] NULL
)
GO
~~~


### Dado este ejemplo
#### Se procederá a la creación de las siguientes tablas de nuestra base de datos.


## [Historia]

        [idHistoria] [int] 
        [fechaHistoria] [datetime]
        [observacion] [varchar](2000)
        [fechaAlta] [datetime] 

~~~sql

CREATE TABLE [dbo].[Historia](
	[idHistoria] [int] NOT NULL,
	[fechaHistoria] [datetime] NOT NULL,
	[observacion] [varchar](2000) NULL,
	[fechaAlta] [datetime] NULL,
 CONSTRAINT [PK_PacienteHistoria_1] PRIMARY KEY CLUSTERED 
(
	[idHistoria] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
~~~
# 
## [HistoriaPaciente]
        [idHistoria] [int]
        [idPaciente] [int]
        [idMedico] [int] 

~~~sql
CREATE TABLE [dbo].[HistoriaPaciente](
	[idHistoria] [int] NOT NULL,
	[idPaciente] [int] NOT NULL,
	[idMedico] [int] NOT NULL,
 CONSTRAINT [PK_HistoriaPaciente] PRIMARY KEY CLUSTERED 
(
	[idHistoria] ASC,
	[idPaciente] ASC,
	[idMedico] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
~~~
#


## [TurnoPaciente]
        [idTurno] [int] 
        [idPaciente] [int] 
        [idMedico] [smallint]
    CONSTRAINT [PK_PacienteTurno] PRIMARY KEY CLUSTERED

~~~sql
CREATE TABLE [dbo].[TurnoPaciente](
	[idTurno] [int] NOT NULL,
	[idPaciente] [int] NOT NULL,
	[idMedico] [smallint] NOT NULL,
 CONSTRAINT [PK_PacienteTurno] PRIMARY KEY CLUSTERED 
(
	[idTurno] ASC,
	[idPaciente] ASC,
	[idMedico] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
~~~

# 

## [Turno]
        [idTurno] [int]
        [fechaTurno] [datetime]
        [fechaAlta] [datetime]
        [estado] [nchar](10)
    CONSTRAINT [PK_Turno] PRIMARY KEY CLUSTERED 

~~~sql
CREATE TABLE [dbo].[Turno](
	[idTurno] [int] NOT NULL,
	[fechaTurno] [datetime] NULL,
	[fechaAlta] [datetime] NULL,
	[estado] [nchar](10) NULL,
 CONSTRAINT [PK_Turno] PRIMARY KEY CLUSTERED 
(
	[idTurno] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
~~~
# 

## [Pais]
        [idPais] [char](3)
        [pais] [varchar](30)
    CONSTRAINT [PK_Pais] PRIMARY KEY CLUSTERED 

~~~sql
CREATE TABLE [dbo].[Pais](
	[idPais] [char](3) NOT NULL,
	[pais] [varchar](30) NULL,
 CONSTRAINT [PK_Pais] PRIMARY KEY CLUSTERED 
(
	[idPais] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
~~~
# 




## [Especialidad]
        [idEspecialidad] [int] IDENTITY(1,1)
        [especialidad] [varchar](30) 
    CONSTRAINT [PK_Especialidad] PRIMARY KEY CLUSTERED 

~~~sql
CREATE TABLE [dbo].[Especialidad](
	[idEspecialidad] [int] IDENTITY(1,1) NOT NULL,
	[especialidad] [varchar](30) NULL,
 CONSTRAINT [PK_Especialidad] PRIMARY KEY CLUSTERED 
(
	[idEspecialidad] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
~~~
# 


## [Medico]
        [idMedico] [dbo].[medico] IDENTITY(1,1)
        [nombre] [varchar](50)
        [apellido] [varchar](50)
    CONSTRAINT [PK_Medico] PRIMARY KEY CLUSTERED 

~~~sql
CREATE TABLE [dbo].[Medico](
	[idMedico] [dbo].[medico] IDENTITY(1,1) NOT NULL,
	[nombre] [varchar](50) NULL,
	[apellido] [varchar](50) NULL,
 CONSTRAINT [PK_Medico] PRIMARY KEY CLUSTERED 
(
	[idMedico] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO

~~~
# 
## [MedicoEspecialidad]
        [idMedico] [int] 
        [idEspecialidad] [int]
        [descripcion] [varchar](50)
    CONSTRAINT [PK_MedicoEspecialidad] PRIMARY KEY CLUSTERED 
~~~sql
CREATE TABLE [dbo].[MedicoEspecialidad](
	[idMedico] [int] NOT NULL,
	[idEspecialidad] [int] NOT NULL,
	[descripcion] [varchar](50) NULL,
 CONSTRAINT [PK_MedicoEspecialidad] PRIMARY KEY CLUSTERED 
(
	[idMedico] ASC,
	[idEspecialidad] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
~~~


#### Cree las tablas que se muestran en el ejercicio.
#### Preste mucha atención al tipo de datos y su tamaño.

#### Debe enviar estos códigos en formato TXT o SQL. Te lo explicaremos en el aula.
#### **Recuerda que el secreto del éxito está en la perseverancia.**
#



## Comandos SQL para manipulación de registros<a name="manipulacion"></a>
## ***Comando Select***
#### La instrucción SELECT en SQL se usa para recuperar datos de una base de datos relacional. Sintaxis SQL: SELECT * FROM "table_name"; "table_name" es el nombre de la tabla donde se almacenan los datos, y "column_name" es el nombre de la columna que contiene los datos que se recuperarán.
# 
## ***Comando INSERT ***
#### es una sentencia SQL que añade datos a una tabla. La sentencia INSERT tiene el formato siguiente: INSERT INTO nombtabla VALUES ( valor1, valor2 , ...) En esta sintaxis, nombtabla es el nombre de la tabla o vista en la que se desea insertar datos y valor1, valor2 (etc.), son los valores que va a insertar.
#
## ***Comando UPDATE***
#### La declaración UPDATE puede utilizarse para actualizar una sola columna, un conjunto más amplio de registros (mediante el uso de condiciones), y/o toda la tabla en una base de datos. La(s) condición(es) puede(n) ser un booleano, una verificación de cadena de texto o una secuencia matemática que se resuelve en un booleano (mayor que, menos que, etc.).
# 
## ***comando DELETE***
#### El comando DELETE permitirá eliminar una o varias filas de una tabla. La sintaxis del comando DELETE es simple si no limitamos las filas. Si no se indica la cláusula WHERE, se borrarán todas las filas de la tabla.
#

Ejemplos:
Select

~~~sql
  SELET * FROM [dbo].[Paciente] 
~~~
    En este caso, estoy extrayendo todos los campos de la tabla.

Ejemmplo 
~~~sql
 SELET 
 	[idPaciente]
	[nombre]
	[apellido]
	[fNacimiento] 
	[domicilio]
	[idPais]
	[telefono]
	[email]
	[observacion] 
	[fechaAlta]
  FROM [dbo].[Paciente] 
~~~
    En este caso, también estoy seleccionando todos los campos de la tabla; pero en este caso estoy especificando sql uno por uno los campos que necesito
    Esto 


## Aprende a utilizar las condiciones con la cláusula WHERE de SQL
#### La cláusula WHERE de SQL se utiliza para especificar una condición al recuperar un conjunto de datos de una tabla o de un conjunto de tablas. Si se cumple la condición dada, la consulta devuelve los valores relacionados con la condición que se especifique en la cláusula WHERE. Debe usar la cláusula WHERE para filtrar los registros y obtener solo los registros necesarios.
# 
#### La cláusula WHERE no solo se usa en la instrucción SELECT, sino que también se usa en la instrucción UPDATE y DELETE., que examinaríamos en las siguientes Clases.
# 
#### Resumiendo:

    La cláusula WHERE se utiliza para obtener datos filtrados de un conjunto de resultados.

- Se utiliza para obtener datos de acuerdo con un criterio particular.
- La palabra clave WHERE también se puede utilizar para filtrar datos al hacer coincidir patrones.
- La cláusula WHERE se puede utilizar con los siguientes tipos de sentencias de SQL:
    - SELECT
    - UPDATE
    - DELETE

##### Sintaxis La sintaxis básica de la cláusula WHERE con **la instrucción SELECT** es la que se muestra a continuación.

~~~SQL
SELECT column1, column2, columnN FROM table_name WHERE [condición] 
~~~
# 
#### La sintaxis para usar WHERE en la instrucción UPDATE es la siguiente:
~~~sql
UPDATE "table_name" SET "column_1" = nuevo valor WHERE "condición" 
~~~

#### La sintaxis para usar WHERE en la instrucción DELETE es la siguiente:
~~~sql
DELETE FROM "table_name" WHERE "condición";
~~~
#
#### "Condición" puede incluir una única cláusula de comparación (llamada condición simple) o múltiples cláusulas de comparación combinadas utilizando los operadores AND u OR (condición compuesta).

#### Además, la cláusula WHERE puede especificar una condición utilizando la comparación o los operadores lógicos como >, <, =, LIKE, NOT, etc. Los siguientes ejemplos te aclararan estos conceptos.

    Ejemplos
~~~sql
select EmployeeID, 
    LastName, 
    FirstName, 
    Title, 
    Address 
from Employees 
    where Title= 'Sales Representative'
~~~

#### Es importante tener en cuenta que todas las cadenas deben estar entre comillas simples (''). Considerando que, los valores numéricos deben darse sin ninguna cita.


## La cláusula WHERE con el operador OR
#### Para ver todos los datos de los Representantes de Ventas y de los administradores de ventas usamos la siguiente consulta SQL.
#
~~~sql
select EmployeeID, 
        LastName, 
        FirstName, 
        Title, 
        Address 
    from Employees 
    where Title= 'Sales Representative' or Title= 'Sales Manager'
~~~

## Usando WHERE con UPDATE y DELETE
#### Como se mencionó anteriormente, la cláusula WHERE se puede usar con las instrucciones UPDATE y DELETE además de la instrucción SELECT. Los ejemplos de cómo usar la cláusula WHERE con estos dos comandos los veremos en los artículos de UPDATE y DELETE.


    Ejercicios
#### Para estos ejercicios, trabajermos con la tabla Employees de la base de datos Northwind


#### 1.- ¿Cuál de las siguientes sentencias de SQL es correcta? (Puede haber más de una respuesta)
    1 SELECT * FROM Employees WHERE FirstName = 'Nancy';
    2 SELECT * WHERE FirstName = 'Nancy' FROM Employees;
    3 SELECT FirstName= 'CARLOS' FROM Employees;
    4 SELECT FirstName FROM Employees WHERE FirstName = 'Nancy';

#### 2.- ¿Cuál es el resultado de la siguiente consulta?
~~~sql
    SELECT EmployeeID, 
            LastName, 
            FirstName, 
            Title, 
            Address 
    FROM Employees 
        WHERE Address LIKE '4%';
~~~
#### _______________________________________________________________________

#### 3.- (Verdadero o Falso) La condición utilizada en la cláusula WHERE debe incluir una columna que sea parte de la cláusula SELECT.________



# SQL JOIN<a name="join"></a>

#### La sentencia del “SQL JOIN” es uno de los componentes principales de la sentencia Select, que se utiliza para extraer datos del “SQL Server”.

#### La palabra “Select” inicia la sentencia. A menudo es seguido por un asterisco (*) “AKA splat” como algunos lo llaman DBA.
# 
###### Nota: para expandir automáticamente los comodines a las columnas explícitas, consulte How to prevent performance problems and errors due to wildcards in SELECT statements
#
#### Esto solo significa retornar a todas las columnas. Si tenemos varias tablas, un Select asterisco capturará todas las columnas de todas las tablas, por ejemplo, unir varias tablas usando la sentencia de “SQL JOIN”, que es el tema principal de este artículo.
#
#### Empezaremos con la definición. Join es el proceso de tomar datos de varias tablas y colocarlos en una vista generada. Por tanto, una instrucción de “SQL JOIN” en un comando Select combina las columnas entre una o más tablas en una base de datos relacional y retorna a un conjunto de datos.
#
#### “El FROM” también es parte esencial de la instrucción Select y es aquí donde se especifica de qué tabla estamos extrayendo los datos. La parte de join es donde queremos unir datos de varias tablas y tenemos tres tipos diferentes de combinaciones:
# 
#### Inner join – esta es la opción predeterminada. Si no se especifica el tipo de unión, se establecerá de manera predeterminada como la unión interna. Esto implica que si estamos uniendo dos tablas en una columna común, solo retornaran los datos que coincidan en ambas tablas
![](https://www.sqlshack.com/wp-content/uploads/2018/10/word-image-150.png)


#


#### Left join – este tipo de unión significa que solo retornan todos los datos de la tabla de la mano izquierda, solo si los datos coinciden con la tabla de la mano derecha
![](https://www.sqlshack.com/wp-content/uploads/2018/10/word-image-151.png)
#

#### Right join – este tipo de unión es el caso opuesto al anterior. Implica que solo retornaran los datos de la tabla de la mano derecha, solo si los datos coinciden con la tabla de la mano izquierda
![](https://www.sqlshack.com/wp-content/uploads/2018/10/word-image-152.png)
#


## Select usando Inner Join

#### Vayamos hasta SQL Server Management Studio (SSMS) y verifiquemos cómo se puede trabajar con la instrucción de “SQL JOIN” utilizando ejemplos del mundo real. A continuación, mostramos un ejemplo de cómo unir tablas en una columna común. En nuestra base de datos de ejemplo AdventureWorks2012, tenemos la tabla “Producto” que tiene una columna “ProductID” y en la tabla “SalesOrderDetail”, también se tiene una columna “ProductID”. Entonces, si deseamos averiguar las ventas totales y los descuentos para cada producto y sacar el nombre, debemos unir estos dos en esta columna común:
#
~~~sql
USE AdventureWorks2012;
GO

SELECT 
    p.Name AS ProductName, 
    NonDiscountSales = (OrderQty * UnitPrice),
    Discounts = ((OrderQty * UnitPrice) * UnitPriceDiscount)
FROM Production.Product AS p 
JOIN Sales.SalesOrderDetail AS sod
    ON p.ProductID = sod.ProductID 
ORDER BY ProductName DESC;
GO
~~~
#### ome en cuenta que, si solo se especifica JOIN por sí mismo, sin una palabra clave interna en la sentencia de “SQL JOIN”, seguirá siendo un INNER JOIN. Por supuesto, puede poner la palabra clave “inner” para mayor claridad, pero si no hay una combinación de etiqueta izquierda / derecha, se establecerá por defecto una combinación interna:
#
![](https://www.sqlshack.com/wp-content/uploads/2018/10/word-image-153.png)
#

## Select usando LEFT JOIN

#### Ahora, démosle un vistazo al LEFT OURTER JOIN que nos ofrece todo desde la tabla de la izquierda y solo los registros que coinciden en la tabla de la derecha. En nuestro ejemplo, la siguiente consulta nos dará algunas personas que no han realizado ninguna compra:
#

~~~sql

SELECT *
FROM Person.Person p
LEFT JOIN Sales.PersonCreditCard pcc ON p.BusinessEntityID = pcc.BusinessEntityID
~~~


![](https://www.sqlshack.com/wp-content/uploads/2018/10/word-image-154a.png)
#
#### El conjunto de resultados indica que retornaron 19972 registros, y se tiene un grupo de valores nulos en la columna “BusinessEntityID”. Las filas que tienen nulos son personas que no realizaron ninguna compra.
#
#### Se puede extender de la consulta anterior y agregar otra sentencia de “SQL JOIN” para poder incluir a las personas con la información de la tarjeta de crédito. Tome en cuenta que se acaba de especificar la palabra clave Join, que es una combinación interna de forma predeterminada y eliminará todos los valores nulos porque esas personas no tienen información de la tarjeta de crédito:
#

## Select usando Right Join
#### Ahora, la cláusula RIGHT JOIN es exactamente lo opuesto a LEFT JOIN. Básicamente hacen lo mismo. La izquierda es derecha y la derecha es izquierda y se puede obtener el mismo efecto simplemente cambiando las tablas. Los RIGHT JOIN no están en omitidas, simplemente no son tan comunes. Por razones de consistencia, es una práctica común utilizar LEFT JOIN en lugar de uniones derechas.
#


## Practicas<a name="practicaJoin"></a>

- 1  para obtener en Northwind los clientes que tengan algún pedido, bastaría con escribir
~~~sql
SELECT OrderID, C.CustomerID, CompanyName, OrderDate
FROM Customers C INNER JOIN Orders O ON C.CustomerID = O.CustomerID 
~~~

- 2 todos los clientes y sus pedidos, incluso aunque no tengan pedido alguno.
~~~sql
SELECT OrderID, C.CustomerID, CompanyName, OrderDate
FROM Customers C LEFT JOIN Orders O ON C.CustomerID = O.CustomerID 
~~~

 - 3 odos los pedidos aunque no tengan cliente asociado
 ~~~sql
SELECT OrderID, C.CustomerID, CompanyName, OrderDateFROM Customers C RIGHT JOIN Orders O ON C.CustomerID = O.CustomerID
 ~~~


- los clientes y sus pedidos, los clientes sin pedido (hay 2) y los pedidos sin cliente (que en este caso son 0).
~~~sql
SELECT OrderID, C.CustomerID, CompanyName, OrderDate
FROM Customers C FULL JOIN Orders O ON C.CustomerID = O.CustomerID
~~~


#




<!-- 
# 
## Comandos SQL para manipulación de registros

## Cláusulas SQL -->

<!-- 
# UNIDAD II

## Tipos de datos Sql

##  Diseñando nuestra primer Base de Datos

## Funciones de Agregado

## Operadores Lógicos

## Stored Procedures

## Estructuras de Control

## Operadores Aritméticos y de Comparación


# UNIDAD III

## Programando Store Procedures

## Funciones de Conversion y Texto


# UNIDAD IV

## Join y Unions en SQL

## Programando Stored Procedures de SELECT UPDATE y DELETE

#  -->




