El álgebra relacional provee operaciones para combinar datos de múltiples tablas en una consulta [[MySql]]. Las más usadas son:

Los Join:
	Los Productos cartesianos combinan todas las tuplas de una tabla con todas las de otra.
	La Selección filtra las tuplas del producto cartesiano que cumplen una condición.
	 La proyección selecciona las columnas deseadas del resultado de la selección.
La unión: Combina las tuplas de dos tablas, eliminando duplicados.
La Intersección: Obtiene las tuplas que se encuentran en ambas tablas.
La Diferencia: Obtiene las tuplas que están en una tabla pero no en la otra.

Supongamos que queremos obtener una lista de clientes que han comprado un producto específico

Clientes: (clienteID, nombre, apellido, email).
Pedidos: (pedidoID, clienteID, fecha, producto).

SELECT c.Nombre, c.Apellido, p.Fecha
FROM Clientes c JOIN Pedidos p ON Clientes.clienteID = pedidos.clienteID
WHERE Pedidos.producto = 'Lavarropa';

Los **JOINs** en **SQL** sirven para **combinar filas de dos o más tablas** basándose en un campo común entre ellas, devolviendo por tanto datos de diferentes tablas. Un JOIN se produce cuando dos o más tablas se juntan en una sentencia SQL.

![[Pasted image 20240427203855.png]]


