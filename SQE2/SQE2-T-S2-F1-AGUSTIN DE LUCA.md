---
tags:
  - Testing
  - SQE2
  - Universidad
Creado: 2025-05-06
Relacionado:
  - SQE2
  - Programacion
completado:
---
# TAREA - FASE  1

Escribe High level test cases (Test Case Title, Description, Expected result) en un documento Word, para la funcionalidad de la imagen.  

Escribe título y descripción para todas las pruebas que se te ocurran.
# Casos de Prueba de Alto Nivel - Funcionalidad de Inicio de Sesión

Este documento presenta casos de prueba de alto nivel para verificar la funcionalidad de inicio de sesión en la aplicación web.

| **Título del Caso de Prueba**                             | **Descripción del Caso de Prueba**                                                                                                                                  | **Resultado Esperado**                                                                                                      |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **Login_001: Inicio de Sesión Exitoso**                   | Verificar que un usuario registrado puede iniciar sesión correctamente con credenciales válidas.                                                                    | El usuario debe ser redirigido a la página principal o al panel de control después de un inicio de sesión exitoso.          |
| **Login_002: Inicio de Sesión con Email Inválido**        | Verificar que el sistema muestre un mensaje de error apropiado cuando se intenta iniciar sesión con un formato de correo electrónico inválido.                      | El sistema debe mostrar un mensaje de error indicando que el formato del correo electrónico es inválido.                    |
| **Login_003: Inicio de Sesión con Contraseña Incorrecta** | Verificar que el sistema muestre un mensaje de error apropiado cuando se intenta iniciar sesión con un correo electrónico válido pero una contraseña incorrecta.    | El sistema debe mostrar un mensaje de error indicando que la contraseña es incorrecta o que las credenciales son inválidas. |
| **Login_004: Inicio de Sesión con Usuario No Registrado** | Verificar que el sistema muestre un mensaje de error apropiado cuando se intenta iniciar sesión con un correo electrónico y contraseña de un usuario no registrado. | El sistema debe mostrar un mensaje de error indicando que el usuario no existe o que las credenciales son inválidas.        |
| **Login_005: Sensibilidad a Mayúsculas/Minúsculas**       | Verificar si el campo de contraseña es sensible a mayúsculas/minúsculas.                                                                                            | El inicio de sesión sólo debería ser exitoso si la contraseña coincide exactamente, respetando mayúsculas/minúsculas.       |
| **Login_006: Mostrar Contraseña**                         | Verificar si el usuario puede visualizar la contraseña cuando se activa el botón de "mostrar contraseña".                                                           | Al hacer clic en el ícono de "mostrar contraseña", el campo debe cambiar de tipo "password" a texto visible.                |
| **Login_007: Recuperación de Contraseña**                 | Verificar que el enlace de recuperación de contraseña redirige correctamente y permite restablecer la contraseña.                                                   | El usuario debe recibir instrucciones o una interfaz para cambiar la contraseña después de hacer clic en el enlace.         |
| **Login_008: Registro de Usuario Nuevo**                  | Verificar que el sistema permite registrar un nuevo usuario correctamente desde el enlace de registro.                                                              | El sistema debe permitir la creación de una cuenta nueva y redirigir al usuario a la página correspondiente.                |
| **Login_009: Validación de Registro**                     | Verificar que el formulario de registro valida correctamente los campos obligatorios y formatos (email, contraseña, etc.).                                          | El sistema debe mostrar mensajes de error si faltan campos requeridos o si los formatos no son válidos.                     |
| **Login_010: Funcionalidad de "Remember Me"**             | Verificar si la opción "Remember Me" mantiene al usuario conectado después de cerrar y reabrir el navegador.                                                        | El sistema debe recordar la sesión del usuario si esta opción está activada, dentro del tiempo configurado.                 |
Feedback de Mateo Escobar:

High level test cases: 

Casos de test planteados: Todos los test que estas proponiendo me parece que estan muy bien, todos tienen un titulo especifico, una descripción detallada de como hacer el test y un caso de resultado esperado bien especifico para cada test, lo que si te podria señalar es que faltan mas casos que se pueden realizar desde esta pagina como por ejemplo:

Se puede ver la contraseña si se apreta el boton para verla?

Se puede cambiar la contraseña con el link que te lleva a eso?

Se puede crear una cuenta?

El register no tiene ningun problema?

El boton "Remember Me”  funciona correctamente?

---

Compañero Guido Mamani
![[Pasted image 20250508142752.png]]
![[Pasted image 20250508142809.png]]
![[Pasted image 20250508143032.png]]
