# BuenasPracticasAngular


Buenas Prácticas Angular
Podemos tener un código (una clase) y por  ejemplo  esta podría ser como un control universal , es decir para todos los televisores. Este mismo te va a funcionar pero no va a reemplazar las funcionalidades únicas del control principal, siguiendo un poco el concepto anterior lo ideal es que cada una de las clases únicamente ,  estén relacionadas con lo que tienen. Esto evita que tengamos clases “toderas” , es decir que hacen de todo. Ejemplo, un class con  registrar usuario, generar token y registrar productos. Es por eso que lo mejor es separar las responsabilidades, una clase para registrar usuario, una clase para generar token y otra para registrar productos,  aparte de dar orden, cumplimos una única responsabilidad.
Mantenlo simple:
-Mantener códigos simples y entendibles. 
-Mantener archivos por debajo de 400 líneas de código 
-Primero propiedades, después métodos.
-Las propiedades y métodos deberían usar el sistema de camelcase (ej: registerUser)
- 12 -15 métodos, dividir en pequeñas porciones el código y  de esas líneas  de código que tenga en esa clase es importante que esos métodos y sus funciones, no sean  métodos enormes . 
-Imports: los archivos externos van primero.
¿Cuál es el total de líneas que deben tener?
30 - 40 lines como máximo en el código si no es así  se debe refactorizar. (Refactorizar): estructurar y facilitar la comprensión del código,cambiar su estructura y diseño y eliminar código muerto, para facilitar el mantenimiento en el futuro.


Como son piezas más pequeñas se podrán leer de manera más fácil y reutilizarlas principalmente.  
Estudios de científicos dicen que si se ven más de 10 elementos al mismo tiempo, es posible que te disperses en el momento. Una de las recomendaciones en la estructura de mi proyecto con angular es mantener menos de 7 ficheros , ejemplo dentro de la carpeta auth asegurarse de tener menos de 7 carpetas . Si necesito más ficheros pues opto por Estructurarlos o organizarlos en sus respectivos folder ej: components que vayan ahi dentro los componentes es decir agruparlos , así como la carpeta services, guards y aun asi siempre me mantendría por debajo de las 7 carpetas. 
- Utilizar rutas osea path absolutas con un alias ejemplo “@angular” , en lugar de rutas relativas que empiezan con “./” . Para ello podemos crear unos alias personalizados  en  nuestro ts.config.json y dentro de la categoría "compilerOptions", creamos la propiedad de path que van a apuntar a unas rutas, esto hará que se ven más limpias y más mantenibles , que las relativas.

![image](https://user-images.githubusercontent.com/73044980/171883606-ea104ad8-12f8-4c68-bfa3-41c5bf273654.png)

y para implementarla ejemplo el path “@admin”, lo pondremos en un componente de board (que es lo que componen un tablero de tareas) 
Vamos a un componente de la carpeta de board, y como necesito agregar el component que hace parte del admin pues simplemente escribo import { NombreComponente) y puede que ya automáticamente nos coloque el path con el alias personalizado que hicimos, sino también lo podemos escribir y aparecerá en la lista del intellisense. 

![image](https://user-images.githubusercontent.com/73044980/171883682-d02b132a-1de5-4f89-902f-cafbecc1c3fd.png)
Aprender  y sumergirse en las directivas 
A lo largo de las aplicaciones , las directivas de angular como el ngfor que se usa desde el template html, para recorrer un array en clase Ts , hace que angular realice un óptimo trabajo directamente con ese tipo de funcionalidad , que podría ser un foreach en js. Pero al utilizar esas directivas que ofrece angular deja que angular sea más ágil utilizando esas funcionalidades.
Ecosistema:
Cuando tengamos aplicaciones robustas, lo ideal es que separes todo por módulos, es decir que cada componente pueda beneficiarse de uno propio esto hace que nuestro app.module.ts (el módulo principal de angular) no quede sobrecargado.
Identación:
Se considera de mayor importancia , utilizar identación siempre cuando codificamos. Es probable que aveces nos olvidamos de utilizar este “requerimiento” lo llamo así , porque es mi opinion es obligatorio utilizar esta herramienta , además esto deja ver que conoces una de las mejores buenas prácticas en general de desarrollo web.  Ya que proporciona mayor claridad de lectura y orden a nuestro código e incluso identificar algunos errorsitos de sintaxis. Una de las herramientas que recomiendo es el complemento  prettier , la podemos encontrar en nuestro VSCode en la opción extensiones:
![image](https://user-images.githubusercontent.com/73044980/171883736-dff66df0-b558-40a8-8b53-70fbd640e1ca.png)

y podemos dejarla como herramienta de formateo por default, es decir por defecto en nuestro VSCode, ya que el editor ya posee una propia pero es muy limitada ya que solo funciona en el html. Entonces, para ello vamos a settings
![image](https://user-images.githubusercontent.com/73044980/171883955-83b2dc6a-8026-4098-b505-192c876aa1e6.png)

y buscamos dentro se settings, formatter . Así mismo aparecerá el apartado Editor:Default Formatter y elegimos la opción prettier .
Nota: si no les aparece es porque no se instaló el complemento.
![image](https://user-images.githubusercontent.com/73044980/171884005-06521625-210e-44e2-acd0-2d5cf67b6ab3.png)

Ya con eso configuración, para utilizar el Prettier ,  en cualquier archivo dentro del código le damos click derecho y la opción Format Document
![image](https://user-images.githubusercontent.com/73044980/171884052-75da3017-b222-4bfe-9972-0c21a1250662.png)

o aún más facil, para ejecutar esa acción el shorcut alt + shift + f






