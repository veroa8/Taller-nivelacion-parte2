MÓDULO SOBRE REACT JS

1. Explicar brevemente el concepto de ReactJS y sus principales características.

ReactJS es una biblioteca de JavaScript desarrollada por Facebook que se utiliza para construir interfaces de usuario (UI) interactivas y eficientes. Su enfoque principal es la creación de componentes reutilizables que representan partes específicas de la interfaz. Las principales características de React incluyen:


- Componentes
- Virtual DOM
- JSX
- Unidireccionalidad de Datos
- Reactividad
- Comunidad Activa


2.  Definir qué es un componente en ReactJS y mencionar los tipos de componentes qué existen.
Los componentes son bloques de construcción de una aplicación en React, permitiendo a los desarrolladores crear interfaces de usuario. Los componentes permiten organizar el código de manera modular y facilitan la construcción de aplicaciones escalables. Hay dos tipos principales de componentes:

Componentes Funcionales:
Definidos como funciones de JavaScript, estos componentes se centran en la presentación y eran inicialmente sin estado. Con la introducción de "Hooks" en React 16.8, los componentes funcionales pueden gestionar su propio estado y utilizar otras características previamente asociadas a componentes de clase.

Componentes de Clase:
Definidos como clases de JavaScript, estos componentes pueden tener su propio estado y métodos de ciclo de vida. Aunque los Hooks han reducido su uso, los componentes de clase siguen siendo válidos y están presentes en código heredado.


3. ¿Qué es el Virtual DOM y cuál es su función en ReactJS?

El Virtual DOM (DOM Virtual) en ReactJS es una representación ligera y virtual del Document Object Model (DOM) real del navegador. Su función principal es mejorar el rendimiento optimizando las actualizaciones en la interfaz de usuario. Cuando hay cambios en los datos de la aplicación, React no actualiza directamente el DOM real. En cambio, compara el Virtual DOM con el estado anterior y determina la diferencia (diffing). Luego, actualiza solo las partes del DOM que han cambiado, minimizando las operaciones costosas de manipulación directa del DOM. Este enfoque reduce la carga en el navegador y mejora la eficiencia, permitiendo a las aplicaciones React ser más rápidas y proporcionar una experiencia de usuario más fluida.

4. ¿Qué es JSX en ReactJS y porqué es importante?

JSX (JavaScript XML) en ReactJS es una extensión de JavaScript que permite escribir código similar a HTML dentro de archivos JavaScript. Combina la lógica y la presentación en un solo lugar, facilitando la construcción de interfaces de usuario declarativas y legibles. JSX simplifica la creación de elementos de React y su estructura refleja la jerarquía del DOM, mejorando la comprensión del código. Aunque no es estrictamente necesario para trabajar con React, JSX es ampliamente adoptado debido a su claridad y concisión. Además, JSX se compila a llamadas de funciones de JavaScript para ser interpretado por el navegador, lo que lo hace eficiente y compatible con las prácticas de desarrollo modernas. En resumen, JSX es crucial en React porque mejora la legibilidad del código y facilita la creación de interfaces de usuario de manera más intuitiva y expresiva.


5. ¿Qué es un Hook en ReactJS y cuál es su propósito?

Un Hook en ReactJS es una función especial que permite a los componentes de función acceder al estado y a características de React, como el ciclo de vida y el contexto. Los Hooks fueron introducidos en React 16.8 para permitir el uso de características de los componentes de clase en componentes funcionales, facilitando la reutilización del código y la gestión del estado y efectos secundarios. Los Hooks más comunes incluyen useState para gestionar el estado, useEffect para realizar operaciones después del renderizado, y useContext para acceder al contexto de React. El propósito principal de los Hooks es mejorar la composición y la legibilidad del código en componentes funcionales, permitiendo el uso de características avanzadas sin la necesidad de clases.

6.  Mencionar al menos tres tipos de Hooks en ReactJS y explicar brevemente para qué se utilizan.

useState:
useState permite que los componentes funcionales tengan y gestionen su propio estado interno. Se utiliza para declarar variables de estado y actualizarlas, lo que provoca la actualización del componente y la interfaz de usuario cuando cambian los datos.

useEffect: se utiliza para realizar operaciones secundarias después del renderizado del componente. Puede manejar efectos como solicitudes de red, manipulación del DOM y limpieza de recursos. Es esencial para tareas asíncronas y operaciones que deben ocurrir después de que el componente se haya montado o actualizado.

useContext:permite acceder al contexto de React en componentes funcionales. Se utiliza para consumir valores proporcionados por un proveedor de contexto, eliminando la necesidad de pasar datos a través de múltiples niveles de componentes.


7.  ¿Cuáles son las reglas de uso para los Hooks en ReactJS?

Componentes Funcionales: Los Hooks deben usarse exclusivamente en componentes funcionales o en funciones definidas dentro de ellos, no en componentes de clase.

Llamada en el Nivel Superior: Las llamadas a Hooks deben realizarse siempre en el nivel superior del componente, no dentro de estructuras de control de flujo o funciones anidadas.
Orden Consistente: Las llamadas a los Hooks deben seguir un orden consistente en cada renderizado del componente para garantizar la correcta conexión entre Hooks y estados correspondientes.

Top-Level del Componente: Las llamadas a Hooks, como useState y useEffect, deben realizarse en el nivel superior del componente, no dentro de condicionales.
Nombramiento con "use": Las funciones personalizadas que implementan Hooks deben comenzar con "use" para seguir las convenciones de nombre.

Evitar en Ciclos de Vida de Clase: No se deben mezclar Hooks con métodos de ciclo de vida de clases.

8.  Explicar qué es React Router DOM versión 6, para qué se utiliza y cuáles son sus principales componentes y Hooks.


React Router DOM se presenta como una biblioteca esencial para gestionar el enrutamiento en aplicaciones de una sola página (SPA), simplificando la navegación y el control de las rutas y vistas. Sirve para facilitar una navegación declarativa, permitiendo actualizar componentes o redirigir a otras vistas sin necesidad de recargar la página. Además, ofrece un manejo eficiente del historial del navegador, garantizando un funcionamiento fluido de la navegación hacia adelante y hacia atrás en una SPA.


Elementos clave:
BrowserRouter: Un componente fundamental que posibilita el enrutamiento al aprovechar el historial del navegador.

Routes: Define las rutas y las relaciones entre las diferentes vistas de la aplicación.

Route: Asocia componentes específicos a rutas particulares, determinando qué componente se debe renderizar en función de la URL actual.

Link: Crea enlaces de navegación que facilitan la transición entre las distintas rutas sin recargar la página.

Outlet: Un componente que actúa como el punto de salida principal para mostrar el componente correspondiente según la ruta actual.

useNavigate: Un hook que permite la navegación programática, facilitando el cambio de ruta en respuesta a eventos específicos.

useParams: Un hook para acceder a los parámetros presentes en la URL, facilitando la personalización dinámica de componentes según la ruta.


9. Explicar cómo se realiza la navegación entre diferentes páginas utilizando React Router DOM.

Instalar React Router DOM:
npm install react-router-dom
o
yarn add react-router-dom
Configura el enrutador:
import { BrowserRouter as Router } from 'react-router-dom';


function App() {
  return (
    <Router>
      {/* Contenido de tu aplicación */}
    </Router>
  );
}


Definir rutas y componentes:
import { Route } from 'react-router-dom';


function HomePage() {
  return <div>¡Bienvenido a la página principal!</div>;
}


function AboutPage() {
  return <div>Acerca de nosotros</div>;
}


function App() {
  return (
    <div>
      <Route path="/" exact component={HomePage} />
      <Route path="/about" component={AboutPage} />
    </div>
  );
}


Añadir enlaces de navegación:
import { Link } from 'react-router-dom';


function Navigation() {
  return (
    <nav>
      <Link to="/">Inicio</Link>
      <Link to="/about">Acerca de</Link>
    </nav>
  );
}


10. ¿Cómo se definen rutas en React Router DOM?


En React Router DOM, las rutas se definen utilizando el componente Route. El componente Route especifica qué componente React debe ser renderizado en la interfaz de usuario en función de la ruta actual.


11. Describir cómo crear un proyecto ReactJS con Vite

Primero, abrir una terminal bash desde la carpeta del pc, luego poner el comando create-vite my-react-app --template react, cambiar al directorio del proyecto con cd my-react-app y ejecutar npm install para instalar las dependencias. Luego se inicia el servidor con npm run dev.

12.  Describir cómo desplegar un JSON server en cualquier Hosting free o servicio en la nube gratuito de su elección.

El hosting gratuito que empleo es Render, y la configuración implica la creación de un archivo index.js en la raíz del proyecto, que detalla la configuración de Render, la ubicación del archivo JSON y el puerto de la API. Estos cambios se cargan en un repositorio en GitHub que almacena todos los archivos del proyecto. Posteriormente, en la plataforma Render, creamos una cuenta, una base de datos y la conectamos a GitHub. Al seleccionar el repositorio, Render identifica automáticamente el archivo JSON, utilizando la información especificada en index.js. Al completar el proceso, Render proporciona un enlace que representa la base de datos alojada y disponible en línea para su uso en otros proyectos.

13.  Describir cómo desplegar una aplicación en cualquier Hosting de su elección.
Hosting elegido GitHub Pages:

Se va a la sección de "Settings" (Configuración) del repositorio en GitHub. En la sección de GitHub Pages, elegir el branch main como fuente y guardar los cambios.


MÓDULO SOBRE GESTION DE ESTADOS Y DATOS CON REACT CONTEXT Y USEREDUCER 


1.  ¿Qué es React Context y para qué se utiliza en el desarrollo web con React?

React Context es una característica de React que permite pasar datos a través de la jerarquía de componentes sin necesidad de pasar props manualmente entre cada nivel. Se utiliza para compartir estados o valores globales de manera eficiente en aplicaciones React.


Cuando varios componentes necesitan acceder a la misma información, como temas, autenticación o configuraciones, Context proporciona una solución centralizada. Permite crear un proveedor de contexto que envuelve los componentes que necesitan acceder a esos datos y un consumidor que los lee sin importar cuán profundo estén en la jerarquía de componentes. Esto evita la "prop drilling" o el paso repetitivo de datos a través de componentes intermedios, mejorando la claridad y mantenibilidad del código en aplicaciones más grandes.

2.  Describir cómo se crea un contexto en React y cómo se proporciona y consume información a través de él.

Para crear un contexto en React, utiliza createContext:
import React, { createContext, useContext } from 'react';


const MiContexto = createContext();


// Proveedor: envuelve componentes que necesitan acceder al contexto
function MiProveedor({ children }) {
  const valorCompartido = 'Información compartida';
  return <MiContexto.Provider value={valorCompartido}>{children}</MiContexto.Provider>;
}


// Consumidor: accede a la información del contexto
function MiComponenteConsumidor() {
  const valor = useContext(MiContexto);
  return <div>{valor}</div>;
}


Para usar el contexto, envuelve tus componentes con el proveedor:
function App() {
  return (
    <MiProveedor>
      <MiComponenteConsumidor />
    </MiProveedor>
  );
}


Ahora, MiComponenteConsumidor puede acceder a valorCompartido sin necesidad de pasar props a través de componentes intermedios. 

3.  ¿Cuál es la ventaja de utilizar React Context en lugar de pasar props a través de múltiples componentes?

React Context ofrece una ventaja significativa al evitar la tediosa propagación manual de props a través de múltiples componentes. Facilita la compartición de datos globalmente, mejorando la legibilidad del código al eliminar la necesidad de pasar props a componentes intermedios. Esto simplifica la gestión del estado global, permitiendo almacenar datos en un contexto accesible desde cualquier nivel del árbol de componentes. Además, Context facilita el mantenimiento al separar la lógica de gestión de estado de la estructura de componentes, lo que puede mejorar el rendimiento en casos de anidamiento profundo. Aunque Context es poderoso, su implementación debe considerarse cuidadosamente según las necesidades específicas de la aplicación. En situaciones simples, pasar props puede ser más directo y apropiado.

4. Explicar el propósito de useReducer en React y cómo se diferencia de useState.

useReducer en React es un hook diseñado para gestionar estados complejos y lógica de actualización más avanzada en aplicaciones. A diferencia de useState, que maneja estados simples de manera individual, useReducer gestiona estados más elaborados mediante una función reductora. Esta función recibe el estado actual y una acción que describe cómo debe cambiar el estado, devolviendo el nuevo estado.

La principal diferencia radica en la complejidad de la lógica de actualización. useReducer es preferible cuando el estado depende del estado anterior o cuando la actualización del estado implica lógica más avanzada. Es especialmente útil para manejar múltiples transiciones de estado de manera más clara y predecible.

En resumen, mientras useState es adecuado para estados simples, useReducer proporciona una solución más robusta y estructurada para la gestión de estados complejos en React.


5.  Describe los argumentos que toma la función useReducer.

La función useReducer en React toma dos argumentos principales: el primer argumento es la función reductora (reducer function) y el segundo argumento es el estado inicial.

Reducer Function:
La función reductora es responsable de especificar cómo el estado debe cambiar en respuesta a una acción. Esta función toma dos argumentos: el estado actual y una acción. La acción describe la intención de la actualización del estado y contiene información adicional si es necesario. La función reductora devuelve el nuevo estado.

Estado Inicial:
El segundo argumento de useReducer es el estado inicial. Este argumento establece el valor inicial del estado antes de que cualquier acción lo modifique.


6.  ¿Por qué es útil utilizar useReducer para gestionar el estado en aplicaciones más complejas?

useReducer en React es útil para gestionar el estado en aplicaciones complejas debido a su capacidad para manejar lógica de actualización avanzada y estados complejos. Permite centralizar la lógica de actualización en una función reductora, facilitando la comprensión y el mantenimiento del código en entornos complejos. La separación de acciones detalladas en la función reductora mejora la claridad y flexibilidad, especialmente cuando hay múltiples formas de actualizar el estado. Además, useReducer simplifica las pruebas unitarias al aislar la lógica de actualización. A medida que la complejidad de la aplicación aumenta, useReducer escala mejor que useState, proporcionando una solución más estructurada y controlada para gestionar estados avanzados y transiciones complejas de estado.


7.  ¿Cómo se puede utilizar React Context junto con useReducer para gestionar el estado global en una aplicación de React?

Para gestionar el estado global en una aplicación de React, puedes combinar React Context y useReducer. Primero, defines el contexto con createContext y proporcionas un estado inicial y la función reductora a través de useReducer. Luego, envuelves tu aplicación o componentes específicos con el proveedor del contexto, pasándoles el estado y la función de despacho. Así, los componentes descendientes pueden suscribirse al contexto y acceder al estado global. Esto elimina la necesidad de pasar props manualmente. Este enfoque es beneficioso para aplicaciones grandes o con múltiples componentes que comparten un estado global, ya que centraliza la gestión del estado y mejora la escalabilidad y mantenimiento del código.


8.  ¿Por qué es importante tener un sistema de gestión de estado global en aplicaciones React más grandes?

En aplicaciones React más grandes, un sistema de gestión de estado global es crucial por varias razones. Facilita la compartición eficiente de datos entre componentes distantes sin pasar props en cascada, mejorando la legibilidad y mantenimiento del código. Un estado global centralizado evita la redundancia y garantiza coherencia en la aplicación. Además, simplifica la gestión de estados compartidos, como la autenticación o configuración, y proporciona un punto único de control para la lógica de estado. Esto resulta en un código más modular, escalable y fácil de mantener, permitiendo un desarrollo más eficiente y sostenible a medida que la aplicación crece en complejidad y tamaño.


9.  Menciona al menos tres ventajas de utilizar una combinación de React Context y useReducer en comparación con el manejo de estado local en componentes.


Gestión de Estado Global:
Utilizar React Context junto con useReducer permite gestionar el estado global de manera centralizada. Esto elimina la necesidad de pasar props manualmente entre componentes y facilita el acceso a datos compartidos desde cualquier parte de la aplicación.


Reducción de Prop Drilling:
Evita el "prop drilling", que es el proceso de pasar props a través de múltiples niveles de componentes. React Context y useReducer eliminan la necesidad de pasar props a componentes intermedios que no necesitan la información, mejorando la legibilidad del código y reduciendo la complejidad.


Centralización de la Lógica de Actualización:
La combinación de React Context y useReducer permite centralizar la lógica de actualización del estado en la función reductora. Esto hace que la gestión del estado sea más predecible, escalable y facilita el mantenimiento del código al separar la lógica de actualización del componente en sí.


10. ¿En qué situaciones podría ser beneficioso migrar de un enfoque de manejo de estado local a un enfoque de estado global utilizando React Context y useReducer?

Migrar de un enfoque de manejo de estado local a un enfoque de estado global con React Context y useReducer puede ser beneficioso en situaciones donde la complejidad de la aplicación aumenta. Si encuentras que la propagación de props se vuelve engorrosa, o si varios componentes necesitan acceder o modificar el mismo estado, la migración a un estado global simplifica la comunicación entre componentes. Además, si la lógica de actualización del estado se vuelve más compleja y requiere una estructura más organizada, useReducer ofrece una solución más clara y escalable. Este enfoque es particularmente beneficioso en aplicaciones grandes o en crecimiento, donde la gestión centralizada del estado mejora la legibilidad, mantenimiento y escalabilidad del código.
