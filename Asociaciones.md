
Los objetos pueden colaborar (asociarse) con otros objetos para lograr un
objetivo.Asociaciones entre Clases

Asociaciones (Association), Agregaciones (Aggregation), y Composición
(Composition) representan las relaciones entre objetos
![[Pasted image 20240708185203.png]]

En términos generales, una asociación es un conexión o relación (dependencia semántica) entre dos clases separadas. 
Una asociación indica como se relacionan los objetos y como se utiliza la funcionalidad entre ellos.
![[Pasted image 20240708185238.png]]

#### Asociaciones Unarias (Unary / directed) 

Una persona conoce su dirección (tiene / has-an una dirección) En este caso, una dirección no sabe que persona vive en ella.
![[Pasted image 20240708185412.png]]
![[Pasted image 20240708185441.png]]

Las asociaciones tienen cardinalidad y multiplicidad: uno a uno (one-to-one), uno a muchos (one-to-many), muchos a muchos (many-to-one), y muchos a muchos (many-to-many). [[1.4 Base de datos]]
![[Pasted image 20240708185501.png]]
### [[La cardinalidad]]
Es el numero de objetos que participan en una asociación y si dicha participación es opcional u obligatoria.. Para determinar la cardinalidad, nos hacemos las siguientes preguntas:
- Que objetos colaboran con otros objetos?
- Cuantos objetos participan en cada colaboración ?
- La colaboración es opcional o obligatoria?
Un empleado es una persona que puede estar casado con otra persona (esposa) y/o tener hijos (personas). Un empleado trabaja en una empresa con diferentes cargos a lo
largo del tiempo.
- Que objetos colaboran con otros objetos? 
- Es una colaboración opcional u obligatoria?
- Un empleado trabaja en una empresa (obligatorio)
- Un empleado tiene un cargo (obligatorio)
- Un empleado puede tener una esposa (opcional)
- Un empleado puede tener hijos (opcional)

![[Pasted image 20240708185911.png]]
Un empleado es una persona que puede estar casado con otra persona (esposa) y/o tener hijos (personas). Un empleado trabaja en una empresa con diferentes cargos a lo largo del tiempo.
- Cuantos objetos participan en cada colaboración?
![[Pasted image 20240708185958.png]]
La cardinalidad indica el numero de instancias de una clase enlazadas a las instancias de otra.
![[Pasted image 20240708190038.png]]
### Agregación: 
Son relaciones todo-parte donde la parte hija (parte) puede existir independientemente del padre (todo).

![[Pasted image 20240708190230.png]]
Son relaciones todo-parte donde la parte hija (parte) puede existir independientemente del padre (todo). 
- Una compañía tiene varios empleados 
- Los empleados son parte de una compañía.
- Cada objeto es independiente del otro.
- Los empleados existen si no existe la compañía (tiene su propio ciclo de vida).
![[Pasted image 20240708190304.png]]
Son relaciones todo-parte donde la parte hija (parte) puede existir independientemente del padre (todo).
![[Pasted image 20240708190700.png]]

### Composición

![[Pasted image 20240708191003.png]]
![[Pasted image 20240708191138.png]]
![[Pasted image 20240708191458.png]]
![[Pasted image 20240708191716.png]]
![[Pasted image 20240708192105.png]]
![[Pasted image 20240708192244.png]]
