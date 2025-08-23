La **arquitectura cebolla** (Onion Architecture), también conocida como arquitectura hexagonal, es un patrón de diseño de software que busca crear aplicaciones altamente mantenibles, testables y desacopladas. 

**Objetivo principal**

- **Aislar la lógica de negocio:** El modelo de dominio, queda completamente aislado de los detalles de implementación, como bases de datos, frameworks o interfaces de usuario.
    
- **Facilitar los tests:** Al estar desacoplada, la lógica de negocio puede ser probada de forma aislada, sin depender de componentes externos.
    
- **Mejorar la mantenibilidad:** Los cambios en la infraestructura (base de datos, frameworks) tienen un impacto mínimo en el núcleo de la aplicación.
    
- **Promover la reutilización:** Los componentes del núcleo pueden ser reutilizados en diferentes contextos.
    

**Se estructura en capas:**

1. **Núcleo (Core):** Contiene el modelo de dominio, entidades, reglas de negocio y servicios de dominio. Es la parte más importante y estable de la aplicación.
    
2. **Capa de Aplicación:** Define los casos de uso y los flujos de trabajo de la aplicación. Coordina la interacción entre los servicios de dominio y la infraestructura.
    
3. **Capa de Infraestructura:** Contiene los detalles de implementación, como:
    
    - Acceso a datos (bases de datos, repositorios)
        
    - Servicios externos (APIs, mensajes)
        
    - Interfaces de usuario (web, móvil)
        

**¿Por qué las dependencias van hacia adentro?**

La característica distintiva de esta arquitectura es que las dependencias siempre apuntan hacia el centro. Esto significa que:

- El núcleo no depende de nada externo.
    
- La capa de aplicación depende solo del núcleo.
    
- La capa de infraestructura depende de la capa de aplicación y posiblemente del núcleo.
    

**Ventajas de la Arquitectura Cebolla:**

- **Mayor testabilidad:** Al estar desacoplada, cada capa puede ser probada de forma independiente.
    
- **Mejor mantenibilidad:** Los cambios en una capa tienen un impacto mínimo en las demás.
    
- **Mayor flexibilidad:** Permite cambiar tecnologías o infraestructuras sin afectar el núcleo de la aplicación.
    

**¿Cuándo usarla?**

La arquitectura cebolla es ideal para aplicaciones de mediana a gran escala que requieren un alto nivel de mantenibilidad y testabilidad. Es especialmente útil en proyectos donde los requisitos pueden cambiar con frecuencia o donde se espera una larga vida útil de la aplicación.

**Estructura de carpetas de Account-Module**

Module

- src
    
    - main
        
        - java/org/jala/university
            
            - application
                
                - dto
                    
                    1. DTO's: Contiene las clases Data Transfer Object (DTO), utilizadas para transferir datos entre diferentes capas de la aplicación.
                        
                - mapper
                    
                    1. Mappers: Contiene las clases mappers, responsables de convertir entre DTOs y entidades de dominio.
                        
                - service
                    
                    1. Services: Define las interfaces de los servicios de la aplicación, que encapsulan la lógica de negocio.
                        
                    2. ServicesImpl: Contiene las implementaciones concretas de los servicios, que realizan las operaciones reales.
                        
            - domain
                
                - entity
                    
                    1. Entities: Contiene las clases entidad, que representan los objetos de dominio de la aplicación.
                        
                - repository
                    
                    1. {Entitie}Repository: Define las interfaces de los repositorios, responsables de acceder y persistir datos.
                        
            - infrastructure/persistance
                
                - Persistance
                    
                    1. {Entitie}Generatos: Contiene las clases generadoras de persistencia, que pueden ser utilizadas para generar código de persistencia automáticamente.
                        
                    2. {Entitie}RepositoryImpl: Contiene las implementaciones concretas de los repositorios, que realizan las operaciones de acceso a datos.
                        
                    3. {Entitie}RepositoryMock: Contiene las implementaciones de prueba (mocks) de los repositorios, utilizadas para simular el comportamiento de los repositorios en los tests.
                        
            - presentation
                
                - Controller
                    
                    1. Create{Entitie}Controller: Contiene el controlador para crear nuevas entidades.
                        
                    2. List{Entitie}Controller: Contiene el controlador para listar entidades existentes.
                        
                    3. MainViewController: Contiene el controlador principal de la aplicación.
                        
                
                1. {Entitie}View: Contiene la vista para representar una entidad específica.
                    
                2. MainView: Contiene la vista principal de la aplicación.
                    
            
            1. MainApp**:** Contiene la clase principal de la aplicación, que inicia la ejecución.
                
            2. ServiceFactory**:** Contiene la fábrica de servicios, utilizada para crear instancias de los servicios.
                
        - resources: Contiene los recursos estáticos de la aplicación, como archivos de propiedades, imágenes, etc.
            
    - POM
        
    - README
        
    - .gitignore