[[1.1 Logica]]
### Introducción a la sintaxis

- Los símbolos que se utilizan y su orden correcto de secuenciación
- Los símbolos que se utilizan en lógica proposicional son:
	- constantes: Verdadero o Falso
	- Variables proposicionales: p, q, r ...
	- Operadores: ¬ (neq), ^(&), v (or) ,→ (si/condicional),↔(si solo si)
#### Reglas de sintaxis
No todas las secuencias de símbolos son válidas. Las reglas para construir una
fórmula válida, llamada fórmula bien formada (wff), son las siguientes:

1. El operador de negacion debe estar antes de la variable
2. los otros operadores deben estar entre dos variblaes
3. las variables no pueden estar juntas (unidas)

1. Una constante es una wff
2. Una variable proposicional es una wff
3. Si P es una wff, entonces -'P es una wff (negación)
4. Si Py Q son wff, entonces PA Q es una wff (conjunción)
5. Si Py Q son wff, entonces P v Q es una wff (disyunción)
6. Si Py Q son wff, entonces P Q es una wff (implicación)
7. Si Py Q son wff, entonces P 9 Q es una wff (si y solo si)


### Uso de ( ) para eliminar ambigüedad
A veces, las secuencias con operadores pueden ser ambiguas. Para eliminar la ambigüedad, utilizamos paréntesis ( )
a. p^(qv¬r)
b. p^((q↔r)v¬r)
Las reglas mencionadas anteriormente se describen a veces de la
siguiente manera:

- si Py Q son wff, entonces (P v Q) es una wff

### Define precedencia para eliminar ambigüedad
Alternativamente, se utilizan convenciones de precedencia:
Los operadores de mayor a menor precedencia son:
1. ¬ 
2. ^
3. v
4. →
5. ↔
### Arboles sintácticos
Utilizando las reglas para construir/reconocer una fórmula bien formada (wff), es posible construir lo que se llama un árbol sintáctico, debemos ser minuciosos al construir la wff

Ejemplo de construcción de un árbol sintáctico 
Utilizando las reglas para construir/reconocer una fórmula bien formada (wff), es posible construir lo que se llama un árbol sintáctico. Debemos ser minuciosos al construir la wff. 

Construyamos un árbol de formación para la wff (𝑝 𝖠 𝑞) 𝖠 (¬ 𝑞 ∨ 𝑟): 

wff => wff 𝖠 wff => (wff 𝖠 wff) 𝖠 wff => (p 𝖠 wff) 𝖠 wff 
wff => (p 𝖠 q) 𝖠 (wff ∨ wff) => (p 𝖠 q) 𝖠 (¬wff ∨ wff) 
wff => (p 𝖠 q) 𝖠 (¬q ∨ wff) => (𝑝 𝖠 𝑞) 𝖠 (¬ 𝑞 ∨ 𝑟 )

![[Pasted image 20240115155850.png]]




