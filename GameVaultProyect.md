Proyecto “GameVault”

Integrantes:

-	Sebastian Bustamante López (2230843)

-	Juan Bahamon (2230235)

-	Gabriela Chavez Aguilera (2230193) 

Docente:
Jonathan López Londoño

Universidad Autónoma de Occidente
Facultad de Ingeniería
2026-01

1. Introducción

GameVault es una plataforma web que creamos enfocada totalmente en el mundo del gaming. La idea es que los usuarios puedan entrar a explorar un catálogo completo de videojuegos, revisar la información detallada de cada uno, hacer compras, dejar sus calificaciones y recibir recomendaciones personalizadas según sus gustos. Además de esto, le sumamos funciones para la comunidad gamer, como la visualización de tiendas físicas, eventos y puntos de interés a través de un mapa.

Para el desarrollo del proyecto, aplicamos las diferentes estructuras de datos que vimos a lo largo del semestre. Nuestro objetivo no era solo construir una página que funcionara bien, sino también demostrar cómo se aplican estas estructuras en un entorno real y práctico.

2. Alcance del sistema

El alcance que definimos para el sistema abarca el desarrollo de una plataforma web interactiva de videojuegos, que incluye desde la autenticación de usuarios hasta la navegación dinámica y el motor de recomendaciones. Específicamente, la plataforma permite:

●	Registro e inicio de sesión de usuarios.
●	Gestión de la autenticación por medio de Firebase.
●	Visualización de un catálogo completo de videojuegos.
●	Consulta de los detalles individuales de cada juego.
●	Sistema de carrito de compras funcional.
●	Calificación y visualización de opiniones de los juegos.
●	Recomendaciones basadas en la similitud entre los videojuegos.
●	Ranking con los juegos más vendidos.
●	Navegación dinámica dentro de la aplicación.
●	Panel administrativo para gestionar todo el contenido.
●	Integración futura de mapas con lugares de interés para la comunidad gaming.

El sistema está pensado principalmente para personas interesadas en los videojuegos y busca ofrecer una experiencia fluida, similar a la de las plataformas modernas de distribución digital como Steam o Epic Games.

3. Objetivo general

Desarrollar una plataforma web de videojuegos que permita gestionar el catálogo, las compras y las recomendaciones, aplicando estructuras de datos avanzadas para optimizar el funcionamiento del sistema y mejorar la experiencia de usuario.

4. Objetivos específicos

●	Implementar un sistema de autenticación seguro utilizando Firebase.
●	Construir un catálogo dinámico de videojuegos.
●	Aplicar estructuras de datos para resolver problemas reales dentro del desarrollo del sistema.
●	Implementar recomendaciones inteligentes por medio de grafos.
●	Organizar y clasificar los videojuegos según criterios específicos.
●	Gestionar toda la información en tiempo real utilizando Firestore.
●	Desarrollar una interfaz que sea moderna e intuitiva para el usuario.

5. Tecnologías utilizadas

Frontend:

Para la parte visual y la interacción con el usuario, trabajamos con tecnologías modernas enfocadas en el desarrollo web interactivo:

●	React.js: La usamos como la librería principal para construir interfaces dinámicas a partir de componentes reutilizables.
●	React Router: Nos permitió manejar la navegación entre las diferentes páginas y vistas de la aplicación de forma fluida.
●	JavaScript: El lenguaje principal que usamos para programar toda la lógica del sistema.
●	CSS / SCSS: Los utilizamos para armar el diseño visual y darle estilos propios a la plataforma.

Backend y base de datos:

●	Firebase: Fue el servicio principal que elegimos para el manejo de los datos y la autenticación.
●	Firebase Authentication: Lo implementamos para encargarse de:

○	El inicio de sesión.
○	El registro de usuarios nuevos.
○	La persistencia de la sesión.
○	La seguridad en la autenticación.

●	Cloud Firestore: Lo usamos como nuestra base de datos NoSQL para almacenar:

○	La información de los videojuegos.
○	Los datos de los usuarios.
○	Las calificaciones pendientes y guardadas.
○	La información de las compras.
○	Los datos de administración.

●	Elegimos Firestore porque nos facilitó una sincronización de datos en tiempo real bastante rápida y eficiente.

6. Arquitectura del proyecto

Organizamos el proyecto siguiendo una estructura modular basada en componentes y separando bien las responsabilidades de cada carpeta.

Organización general:

●	Components: Guarda los componentes reutilizables que necesitamos en diferentes partes de la aplicación.
●	Pages: Contiene las vistas o pantallas principales del sistema.
●	Routes: Se encarga de administrar cuáles rutas son públicas y cuáles son privadas.
●	Hooks: Incluye los hooks personalizados que creamos para reutilizar la lógica de estado.
●	Context: Nos permite manejar los estados globales en toda la aplicación (como el carrito o el usuario).
●	Helpers: Contiene funciones auxiliares que usamos repetidamente.

Esta forma de organizarnos nos ayuda a mejorar:

●	La escalabilidad del proyecto.
●	El mantenimiento del código.
●	La reutilización de lo que ya programamos.
●	La separación clara de responsabilidades.

7. Estructuras de datos implementadas

Uno de los pilares del proyecto fue aplicar estructuras de datos reales en las funciones clave de la plataforma. Aquí explicamos cuáles implementamos y por qué:

7.1 Pila 

●	Uso dentro del proyecto: La usamos para manejar el historial de navegación del usuario en la plataforma. Cada vez que alguien pasa de una página a otra, las rutas visitadas se van guardando en una pila. Cuando el usuario le da al botón de regresar, el sistema saca la última página visitada.

●	¿Por qué se utilizó una pila?: Porque funciona bajo el principio LIFO (Last In, First Out), lo que encaja perfectamente con cómo funciona la navegación hacia atrás: la última página que viste es la primera que debe aparecer al regresar.

●	Beneficios:

○	Logramos una navegación eficiente.
○	Simulamos perfectamente el comportamiento del botón “volver atrás”.
○	Mantenemos una organización cronológica de la navegación.

7.2 Lista

●	Uso dentro del proyecto: Las listas las usamos para guardar los videojuegos del catálogo, gestionar los productos que el usuario mete al carrito de compras y manejar los bloques de recomendaciones.

●	¿Por qué se utilizó una lista?: Porque nos permiten almacenar elementos de forma secuencial y nos facilitan recorrer los datos dinámicamente en la pantalla.

●	Beneficios:

○	Hace que recorrer la información sea muy sencillo.
○	Permite la inserción dinámica de nuevos videojuegos.
○	Nos da flexibilidad al momento de mostrar el catálogo.

7.3 Árbol Binario de Búsqueda 

●	Uso dentro del proyecto: Implementamos un árbol binario de búsqueda para organizar los videojuegos según su precio. Esto nos sirve para buscar juegos rápido, filtrarlos por rangos de precio y ordenarlos de forma eficiente.

●	¿Por qué se utilizó un árbol binario?: El árbol nos permite hacer búsquedas optimizadas gracias a su estructura jerárquica. Cada nodo sigue un orden estricto: los valores menores se van a la izquierda y los mayores a la derecha.

●	Beneficios:
○	Búsquedas mucho más rápidas.
○	Filtrado eficiente de los datos.
○	Una mejor organización interna de la información.

7.4 Max-Heap

●	Uso dentro del proyecto: Lo implementamos para armar el ranking de los videojuegos más vendidos en la plataforma. Así, los juegos con más ventas se acomodan solos en la parte más alta.

●	¿Por qué se utilizó un Max-Heap?: Es la estructura ideal cuando se necesita gestionar prioridades. En nuestro caso, la prioridad la define la cantidad de ventas de cada juego.

●	Beneficios:

○	Acceso directo y rápido al juego más vendido.
○	Organización automática del ranking.
○	Eficiencia al hacer consultas sobre la popularidad de los títulos.

7.5 Grafo

●	Uso dentro del proyecto: Lo usamos para darle vida al sistema de recomendaciones. Cada videojuego funciona como un nodo y las relaciones de similitud entre ellos son las conexiones (aristas). Cuando el usuario entra a ver un juego, el sistema revisa sus conexiones y le recomienda los títulos más cercanos.
●	¿Por qué se utilizó un grafo? Los grafos son perfectos para representar relaciones complejas entre distintos elementos. Nos permitieron modelar qué tan parecidos son los videojuegos basándonos en su género, categoría, popularidad y etiquetas.
●	Beneficios:

○	Recomendaciones que cambian de forma dinámica.
○	Mapeo claro de las relaciones entre videojuegos.
○	Una experiencia mucho más personalizada para el usuario.

8. Funcionalidades principales

●	Sistema de autenticación: Permite registrarse e iniciar sesión de forma segura con Firebase Authentication.
●	Catálogo de videojuegos: Muestra de forma ordenada los títulos disponibles en la plataforma.
●	Carrito de compras: Permite ir agregando juegos para comprarlos después.
●	Detalles del juego: Despliega la información específica e individual de cada videojuego.
●	Sistema de recomendaciones: Sugiere títulos similares utilizando la estructura de grafos.
●	Ranking de ventas: Muestra los videojuegos más vendidos apoyándose en el Max-Heap.
●	Navegación dinámica: Controlada internamente a través de una estructura de pila.
●	Panel administrativo: Una sección pensada para gestionar los videojuegos y los contenidos del sistema.
●	Integración de mapas: Diseñada para visualizar en el futuro:

○	Tiendas de gaming.
○	Eventos del medio.
○	Lugares de interés general.

9. Base de datos

Para la base de datos nos decidimos por Cloud Firestore. El sistema se encarga de centralizar y manejar datos como los usuarios, los juegos, las compras, el carrito, las calificaciones y las recomendaciones.

Elegimos Firestore principalmente por estas razones:

●	Es muy fácil de integrar con React.
●	Ofrece sincronización en tiempo real.
●	Es altamente escalable.
●	Nos da la flexibilidad propia de un modelo NoSQL.

10. Conclusiones

●	El desarrollo de GameVault nos sirvió muchísimo para bajar a la realidad los conceptos teóricos de estructuras de datos que vimos en clase, aplicándolos en un entorno real y funcional.
●	Cada estructura de datos la elegimos basándonos en las necesidades puntuales del sistema, lo que nos permitió optimizar los procesos de navegación, las búsquedas, la organización interna y el motor de recomendaciones.
●	Además, el proyecto nos ayudó a reforzar habilidades clave como el desarrollo frontend, el diseño de arquitecturas web, el manejo de bases de datos, los flujos de autenticación, el diseño de interfaces interactivas y la organización modular del código en un proyecto real.
●	Trabajar con la combinación de Firebase y React demostró ser una excelente opción para construir una plataforma moderna, que sea escalable y quede lista para recibir mejoras en el futuro.

11. Recomendaciones futuras

●	Implementar una pasarela para un sistema completo de pagos reales.
●	Terminar de integrar los mapas con geolocalización en tiempo real.
●	Añadir un chat interactivo para conectar a los usuarios entre sí.
●	Meter filtros de búsqueda mucho más avanzados en el catálogo.
●	Seguir puliendo el algoritmo del grafo de recomendaciones para hacerlo más preciso.
●	Añadir una sección de "favoritos" o lista de deseos para los usuarios.
●	Optimizar el rendimiento de la carga del catálogo cuando la base de datos crezca.

12. Referencias

React Documentation. (s.f.). React Official Documentation. Recuperado de https://react.dev/
Firebase Documentation. (s.f.). Firebase Official Documentation. Recuperado de https://firebase.google.com/docs
Cloud Firestore Documentation. (s.f.). Firestore Documentation. Recuperado de https://firebase.google.com/docs/firestore
Firebase API Reference. (s.f.). Firebase API Reference. Recuperado de https://firebase.google.com/docs/reference
MDN Web Docs. (s.f.). JavaScript Documentation. Recuperado de https://developer.mozilla.org/es/docs/Web/JavaScript
React Router Documentation. (s.f.). React Router Official Documentation. Recuperado de https://reactrouter.com/
Goodrich, M. T., Tamassia, R., & Goldwasser, M. H. (2014). Estructuras de datos y algoritmos en Java. Wiley.
Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). Introduction to Algorithms (3rd ed.). MIT Press.
Material de clase de la asignatura Estructuras de Datos 2 – Universidad Autónoma de Occidente. 


