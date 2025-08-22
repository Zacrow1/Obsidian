---
sticker: emoji//2622-fe0f
banner: Areas/Programacion/attachment/image-62.webp
---
# `rir:Reactjs`  REACT
> [!info] ¿Que es?
> Es una biblioteca para construir interfaces de usuario web y nativas

Para poder trabajar en React tenemos que usar un empaquetador llamado Vite o Refine

### Instalar react en el proyecto:

```Bash
npm init -y
```

#### Elegir si queres usar vite o refine

> [!tldr] Vite
>```bash
npm create vite@latest```

> [!tldr] Refine
> ```bash
npm create refine-app@latest```

Seleccionar [[JavaScript]]/[[TypeScript]] +SWC

En la carpeta del proyecto

```Bash
npm install
```

###  Múltiples elementos en una variable

> [!info] Uso del React.Fragment
> Asignación de múltiples elementos a una variable. Al igual que cualquier otro elemento, puede asignar elementos de fragmentos a las variables, pasarlos como accesorios, etc.

```javascript
<React.Fragment>
	<button>
		Hola button
	</button>
	<button>
		Hola button
	</button>
	<button>
		Hola button
	</button>
</React.Fragment>

%% Se puede escribir como  %%
<>
	code
</>
```

### Componentes

son como las funciones de JavaScript. Aceptan entradas arbitrarias (llamadas “props”) y retornan elementos de React que describen lo que debe aparecer en la pantalla.

> [!warning] PascalCase
> Los componentes se escriben **OBLIGATORIAMENTE** en PascalCase MayuculaEnCadaCambioDePalabra

¿como funciona? creamos una constante **Button** si queremos que se le ingresen parametros  tenemos que poner **({text})** y luego llamamos el componente para ser renderizado

```javascript
const Button = ({text}) =>{
	return{
		<button>
			<svg> svg text </svg>
			{text}
		</button>
	}
}

root.render({
	<React.Fragment>
		<Button text="Boton 1" />
		<Button text="Boton 2" />
		<Button text="Boton 3" />		
	</React.Fragment>
})
```


### Importar y exportar un componente

```javascript
	export function Button
	import (Button) from './Button.jsx'
```

### Agregar estilo a un componente

- Nativo
```javascript
	import './Component.css'
	
	export function TwitterFollowCard(){
	return(
		<article className='tw-followCard'>
			<header className='tw-followCard-header'>
				<img 
					alt="Salta" 
					src="EmpanadaSaltenia.jpg"
					className='tw-followCard-avatar'
				/>
				<div className='tw-followCard-info'>
					<strong className='tw-followCard-info-username'> La mejor empanada </strong>
					<span>@Lasaltenia</span>
				</div>
			</header>
			<aside>
				<button className='tw-followCard-button'>
					Seguir
				</button>
			</aside>
		</article>
	)}
```

### parámetros

> [!info] ¿Qué son los parámetros?
>  Los parametros


```javascript
export function TwitterFollowCard({userName, name, avatar, isFollowing}){
	
	return(
		<article className='tw-followCard'>
			<header className='tw-followCard-header'>
				<img 
					alt="Salta" 
					src={'https://unavatar.io/${username}'}
					className='tw-followCard-avatar'
				/>
				<div className='tw-followCard-info'>
					<strong className='tw-followCard-info-username'>{name}</strong>
					<span>{userName}</span>
				</div>
			</header>
			<aside>
				<button className='tw-followCard-button'>
					seguir
				</button>
			</aside>
		</article>
	)}
}
```

```javascript
import './App.css'
import {TwitterFollowCard} from './ubicaciondelarchivo.jsx'

export funtion App (){
	return(
		<section className="App">
			<TwitterFollowCard isFollowing={true} userName="midudev" name="Miguel Angel"
			<TwitterFollowCard isFollowing={false} userName="midudev" name="Miguel Angel" 
		</section>
		
	)
}
```