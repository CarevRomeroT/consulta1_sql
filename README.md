#CONSULTAS SQL

![tabla usuario](img/tablausuario.png "tabla usuario")

1. Para visualizar toda la informacion que contiene la tabla `usuario` se puede incluir con la inclusion SELCET el caracter "*" o cada uno de los campos de la tabla
`select * from usuario`

![](img/imagen1.png "consulta 1")

2. Visualizar solamente la identificacion del usuario.

`select Identification from usuario`

![](img/imagen2.png "consulta 2")

3. Se desea obtener los registros cuya identidad sea mayores o iguales a 150, se utiliza la clausula where que especifica los condiciones que deben reunir los registros que se vam a seleccionar.

`SELECT * FROM usuario WHERE identification>='150'`

![Consulta3](img/imagen3.png "consulta 3 ")

4. Si se desea obtener los registros cuyos sus apellido sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros que se quieren visualizar de una tabla.

`SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas', 'Cetina')`

![Consulta4](img/imagen4.png "consulta 4 ")

O se puede utilizar el operador OR

`SELECT apellidos FROM usuario WHERE apellidos ='Vanegas' OR apellidos ='Cetina'`

![Consulta4](img/imagen4.2.png "consulta 4 pero con OR")

5. Si se desea obtener los registros cuya identificacion sea menor de '150'  y la ciudad sea 'Cali', se debe utilizar el opredaor AND.

`SELECT * FROM usuario WHERE Identificación<'150' AND ciudad_nac='Cali'`

![Consulta5](img/imagen5.png "consulta 5")


6. Si se desea obtener los regitros cuyos nombres empiecen por la letra 'A', se debe utilizar el operador LIKE que utiliza los patrones '%' (Todos) y '_' (caracter)

`SELECT * FROM usuario WHERE nombre LIKE 'A%'`

![Consulta6](img/imagen6.png "consulta 6")


7. Si se desea obtener los registros cuyo nombre contenga la letra 'a'.

`SELECT * FROM usuario WHERE nombre LIKE 'a%'`

![Consulta7](img/imagen7.png "consulta 7")

8. Si se desea obtener los registros donde la cuarta letra del nombre sea una 'a'

`SELECT * FROM usuario WHERE 

![Consulta8](img/imagen8.png "consulta 8")

nombre LIKE '___a%`

9. Si se desea obtener los registros cuya identificacion este entre el intervalo 110 y15, se debe utilizar la clausula BETWEEN, que sirve para especificar un intervalo de valores.

`SELECT * FROM usuario WHERE Identificación BETWEEN '110' AND '150'`

![Consulta9](img/imagen9.png "consulta 9")


## COMANDO DELETE

10. Parra eliminar solamente los registros cuya identificación sea mayor de 130

`DELETE FROM usuario WHERE Identificación>130 `


![Consulta 10](img/img10.png "consulta 10")
![Consulta 10](img/img10.2.png "consulta 10")


11.Para actualizar la ciudad de nacimiento de Cristian Vanegas, cuya identificación es 114.

`UPDATE usuario SET ciudad_nac = 'Manizales' WHERE Identificación='114'`

![Consulta 11](img/img11.png "consulta 11")


##INNER JOIN 
Permite obtener datos de dos o mas tablas. Cuando se realiza la concatacion de las tablas, no necesariamente se debe mostrar todos los datos de las tablas 

##Tabla pedidos

![Tabla pedidos](img/imgtablapedidos.png "tabla pedidos")

12. Para visualizar los camposidentificación, nombre, apellidos dela tabla ususario y numero pedido, fecha de compra, fecha de vencimiento y observacion de la tabla de pedidos. Se debe realizar la siguiente instruccions SQL:

`SELECT usuario. identifiación, usuario.nombre, usuario.apellido, pedido.nropedido, pedido.fechacompra, pedido.fechavence, pedidos.observación, FROM usruario INNER JOIN pedidos ON usuario. Identificación = pedidos.Identificación`

![Consulta 12](img/img12.png "consulta 12")

13. Para visualizar todos los cmapos de las tablas usuarios y pedidos donde Identificacion sea mayor que 100, se debe realizar la siguiente instruccion

`SELECT usuario.* , Pedidos.* FROM usuario INNER JOIN Pedidos ON usuario.Identificación= Pedidos.Identificacion WHERE usuario.Identificación>100;`
![Consulta 13](img/img13.png "Consulta 13")
