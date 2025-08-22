## Concepto:
Una ecuación es una igualdad matemática entre dos expresiones, denominadas miembros y separadas por el signo igual, en las que aparecen elementos conocidos y datos desconocidos o incógnitas, relacionados mediante operaciones matemáticas.

**Componentes de una ecuación**

Los componentes de una ecuación son los siguientes:

- **Miembro:** Es cada una de las dos expresiones separadas por el signo igual.
- **Términos:** Son los sumandos que forman los miembros de una ecuación.
- **Números:** Pueden ser enteros, racionales, reales, imaginarios, etc.
- **Operaciones:** Pueden ser básicas (suma, resta, división, producto, raíz) o más complejas (como derivadas e integrales).
- **Variables o incógnitas:** Son valores que se desconocen. Pueden tener un único valor o varios; se denotan por las letras generalmente, pero se puede usar cualquier otro símbolo.
- **Grado de la ecuación:** Es el mayor de los exponentes de las incógnitas, una vez realizadas todas las operaciones (reducir términos semejantes).
- **Solución:** Es el valor que debe tener la incógnita para que se cumpla la ecuación.
	
	![[Pasted image 20231219092854.png]]
**Tipos de ecuaciones**

Las ecuaciones se pueden clasificar según el grado de la variable incógnita. Las ecuaciones de primer grado son aquellas en las que el mayor exponente de la variable incógnita es 1.

**Ecuaciones lineales o de primer grado**

Una ecuación lineal es una ecuación de primer grado con una variable. Su forma general es:

 $ax+b=0$ donde $a$ y $b$ son numeros reales, $a\neq0$ y $x$ es la variable
 
Para resolver una ecuación de primer grado, se pueden seguir los siguientes pasos:

1. **Quitar denominadores:** Si la ecuación tiene denominadores, se multiplican ambas partes de la ecuación por el mínimo común múltiplo de los denominadores.
2. **Quitar paréntesis:** Si la ecuación tiene paréntesis, se aplica la propiedad distributiva de la multiplicación para quitarlos.
3. **Transposición de términos:** Se agrupan los términos con la variable incógnita en un miembro de la ecuación, y los términos independientes en el otro miembro.
4. **Despejamiento de la incógnita:** Se divide ambos miembros de la ecuación por el coeficiente de la variable incógnita.
5. **Comprobar la solución:** Se sustituye la solución obtenida en la ecuación original para comprobar que se cumple la igualdad.

![[Pasted image 20231219093245.png]]

## Ecuaciones de segundo grado o cuadraticas
Son las ecuaciones en las que la potencia más grande de la incognita es un dos.
### $$ax^2+bx+c=0$$
donde $a$, $b$ y $c$ son numeros reales y $a\neq0$

Estas ecuaciones simpre tienen 2 posibles soluciones y se pueden resolver de las siguientes maneras:

### Solucion por factorización
Esto solo funciona cuando uno de los lados de la ecuacion es 0. Y se resuelve mediante la factorizacion
- Ejemplo: 
	- ![[Pasted image 20231219094852.png]]
### Solucion mediante la formula cuadratica:
Se obtienen las 2 soluciones mediante el uso de las seguientes formulas:
### $$x_{1}=\frac{-b+\sqrt{b^2-4ac}}{2a}$$
### $$x_2=\frac{-b-\sqrt{b^2-4ac}}{2a}$$

## Ecuaciones de tercer grado: formula de Cardano Tartaglia
Supongamos que:

### $$f(X)= X3+a1X2+a2x+a3\in Q[X]$$
A todos los efectos, el resolver $f{X}=0$ equivale a hacer lo mismo para la ecuacion que resulta de sustituir. $X+\frac{a_1}{3}$ en $f{X}$. Esta sustitucion tiene la ventaja de que elimina el termino en X2, luego se puede suponer , de entrada, que 
### $$f(X)=X3+pX+q$$
La sustitucion anterior se llama de Tchirnhausen.
Las soluciones de $f(X)=X3+pX+q=0$ (1)
Podemos suponer que $p$ y $q$ son distintos de 0 (si $p=0$, las soluciones de (1) son las raices cubicas de $-q$; si $q = 0$ las soluciones son 0 y las raices cuadradas de $-p$)
Supongamos que $a$ es una solucion de (1). Hagamos la sustitucion de $a=u+v$
Obtenemos:
- $u^3+v^3+(3uv+p)(u+v)+q=0$
Si tomamos $u$ $v$ de manera que $3uv+p=0$, $i$.$e$. $u$,$v$ serian las raices de la ecuacion cuadratica $X^2-aX-\frac{p}{3}=0$ obtenemos: $u^3+v^3=-q$

Puesto que $u^3v^3=-\frac{p^3}{27}=0$ (2)

Asi pues para encontrar una solucion de (1) tomamos una solucion de $\beta$ de (2), tomamos $u^3$ una raiz ubicada de \$beta$ y ponemos $v=-\frac{p}{3u}$
Entonces $v^3$ es la otra solucionde (2) y $a=u+v$ es solucion de (1).
Simbolicamente, una solucion de (1) es:
$$a=\sqrt[3]{-\frac{q}{2}{+\sqrt{\frac{q^2}{4}+\frac{p^3}{27}}}}+\sqrt[3]{-\frac{q}{2}-{\sqrt{\frac{q^2}{4}+\frac{p^3}{27}}}}$$
debido a que las soluciones de (2) son:
$$-\frac{q}{2}\pm\sqrt{\frac{q^2}{4}+\frac{p^3}{27}}$$
Si $w\neq1$ es una raiz cubica de 1, $u_1=u$,$u_2 = wu$,$u_3 = w^2$ son las tres raices cubicas de $s_0$. Pongamos $v_i=-\frac{p}{3u_i}$ de manera que $v _1= v,v_2=w^2v,v_3=wv$ Entonces las raices de (1) son: 
$a_i=v_i$, $i$ = 1, 2, 3.

## La ecuacion de cuarto grado: metodo de Ferrari
Mediante una transformacion se realiza mediante una sustitución de la variable x por una nueva variable u, de la forma:
![[Pasted image 20231219114613.png]]
**Explicación del caso en que r = 0**

En el caso en que r = 0, la ecuación de cuarto grado se reduce a la siguiente ecuación de tercer grado. En el caso en que q = 0, la ecuación de cuarto grado se reduce a la siguiente ecuación cuadrática. Podemos suponer $r,q\neq0$

Consideremos una variable auxiliar $u$ y escribamos
![[Pasted image 20231219114628.png]]
Para que el polinomio entre corchetes, que notaremos g(X), sea un cuadrado ha de verificarse que
![[Pasted image 20231219114636.png]]
Ahora bien, (4) es una ecuación de tercer grado, por lo que sabemos resolverla mediante radicales. Sea $u_8$ una raíz de (4). Entonces, $\frac{q}{4u_0}$ es una raíz doble de g(X) y se tiene
![[Pasted image 20231219114643.png]]
de donde las raices de f(X)son las raices de los siguientes polinomios de grado2
![[Pasted image 20231219114652.png]]


# Ecuaciones de Calculo 1 

Es importante hacer la verificación cuando hay ecuaciones con fracción

## Problemas con ecuaciones

![[Pasted image 20240429104453.png]]

![[Pasted image 20240429104747.png]]

## Ecuaciones de orden n

![[Pasted image 20240429110701.png]]