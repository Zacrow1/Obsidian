Es un patrón de diseño de comportamiento con la intención de este patrón es definir una dependencia de uno a muchos entre objetos para que cuando un objeto cambie de estado, todos sus dependientes sean notificados y actualizados automáticamente. Consta de los siguientes Componentes:

- **Observador**: define una interfaz para objetos que deben ser notificados de un cambio.
- **El sujeto**: conoce a sus observadores. Proporciona una interfaz para conectarlos y desconectarlos.
- **ConcreteSubject**: envía una notificación a sus observadores cuando su estado cambia, también es posible enviar información del subject mediante el método Notify a sus Observers.
- **ConcreteObserver** Implementan la interfaz Observer. También puede almacenar su estado el cual debe de ser consistente con el del Sujeto. EI manejo de estado es opcional.
