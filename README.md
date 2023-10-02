## consultas_1_sql
# Introducción a las consultas a una BD usando el lenguaje SQL

## Base de datos. Ventas
## Tabla : Cliente

![Tabla Cliente](tabla-cliente.png "Tabla Cliente")


## Instruccion SELECT 
- permite seleccionar datos de una tabla.!
` SELECT campos_tabla FROM nombre_tabla`

### consulta NO. 1
1. para visualizar toda la informacion que contiene la tabla ciente se puede incluir con la intruccion SELEC el caracter **\*** o cada uno de los campos de la tabla.

- `SELEC * FROM Cliente`

![Tabla Cliente](tabla cliente.png "Tabla Cliente")

- `SELECT identificacion, nombre, apellidos, dirrecion, telefono, ciudad_nac, fecha_nac FROM Cliente`
![Consulta2](consulta2.png "Consulta 2")

![Tabla Cliente](tabla cliente.png "Tabla Cliente")



### Consulta No. 2

2. para viasualizar solamente la identificacion del cliente: `SELECT identificación FROM Cliente`
![Consulta2](consulta2.png "Consulta 2")

![Tabla Cliente](tabla cliente.png "Tabla Cliente")


### Consulta No.3

3. Si se desea obtener los registros cuya identificación sea mayor o igual a 150, se de utilizar la cláusula `WHERE` que especifica las condiciones que deben reunir los registros que se van a seleccionar: `SELEC * FROM Cliente WHERE identificacion>=150`
![Consulta3](consulta3.png "Consulta 3")


### Consulta No.4

4. Se desea obtener los registos cuyos apellidos sean Vanegas o Cetina, se debe utilizar el operador `IN` que especifica los registros que se quieren visualizar de una tabla.

`SELECT apellidos FROM Cliente WHERE apellidos IN('Vanegas', 'Cetina')`

![Consulta4_1](consulta4_1.png "Consulta 4_1")

O se puede utilizar el operador `DR`

`SELECT apellidos, nombre FROM Cliente WHERE apellidos = 'Vanegas' OR apellidos ='Cetina'`

![Consulta4_2](consulta4_2.png "Consulta 4_2")


### Consulta No.5

5. Se desea obtener los registros cuyta identificación sea menor de 110 y la ciudad sea Cali, se debe utilizar el operador  `AND`
`SELECT * FROM Cliente WHERE identificación<=110 AND ciudad_nac = 'Cali'`

![Consulta5](consulta5.png "Consulta 5")


### Consulta No.6

6. Cómo se crea una relación uno o muchos en phpMyAdmin