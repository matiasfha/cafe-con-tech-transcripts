Matias: [00:00:00] 
Bienvenidos a este primer episodio de Café con Tech en inglés. Hoy estoy con el único e inigualable Kent C Dodds. Kent, gracias por venir.  Gracias por aceptar ser mi invitado en este particular episodio que inicia su primera temporada.



Kent: [00:00:14]
Sí, me siento honrado de ser invitado. Es realmente genial y genial de tu parte tener un podcast en español y, y agradable de tu parte invitarme a hacer uno en inglés. Porque yo, , no comprendo mucho español. 



Matías: [00:00:33]
Eso es habitual. Además, creo que todo desarrollador latinoamericano debería aprender inglés de todos modos. Si quieres tener más puertas abiertas y subir de nivel en tu carrera, pero, para empezar, Kent, ¿puedes presentarte? No sé. Si alguien más necesita una presentación tuya, pero hagámoslo.



Kent: [00:00:56]
Estoy seguro de que hay mucha gente que no me conoce, pero, sí, mi nombre es Kent C. Dodds y vivo en Utah, en los Estados Unidos. Soy padre de cuatro hermosos hijos, marido, tengo un perro y enseño a la gente a escribir software de calidad. En particular, me enfoco mucho en React, pero también hago mucho Node. Así que prácticamente todo es JavaScript para mí.  He estado haciendo eso durante poco más de dos años, antes de eso fue PayPal y luego un par de otras empresas. He trabajado en bases de código realmente grandes y por eso conozco el dolor y la lucha. Trato de tomar esa experiencia que he tenido para ayudar a otras personas a aliviar algo de ese dolor y hacer del mundo un lugar mejor con lo que están haciendo.



Matias: [00:01:44]
Me gustó mucho esa cita, "Haz del mundo un lugar mejor con código. "En general, la gente tiende a pensar que sólo escribimos código, pero en realidad resolvemos problemas. Así que eso es lo que me ha gustado. Tengo una pregunta, en algún momento fuiste conocido como el chico de las pruebas, uh ahora eres más un chico de React en términos de pruebas. Y ya que has mencionado esto, que tienes experiencia con una gran base de código, ¿cómo puedes vender las pruebas a tus jefes? El testing es una especie de área gris que nadie quiere que hagas porque lleva tiempo, pero siempre es deseable tenerlo, porque mejorará tu proceso, pero ¿cómo lo vendes? 


Kent: [00:02:26]
Sí. Así que en realidad tengo una entrada de blog titulada, "Alineación de Negocios e Ingeniería", que es donde hablo de cómo conseguir que la gente de negocios haga lo que quieras. El truco es la parte de cambiar lo que quieres, para estar en línea con lo que la gente de negocios quiere que hagas. En realidad, se trata de identificar la misión de la empresa y suponer que todo el mundo está motivado para impulsar esa misión. Y si tienes gente que no está motivada para impulsar la misión, entonces, estás en un mal lugar de todos modos. Así que tenemos que asumir que la gente está motivada para impulsar la misión.

Kent: [00:03:24]
Así que identificas la misión y luego averiguas cómo puedes explicar a la gente de negocios que lo que quieres hacer va a impulsar mejor esa misión. Va a ayudarle en sus objetivos.  Y para poder hacer eso, primero tienes que convencerte de que esto realmente va a ser un retorno valioso de tu inversión de tiempo.

Kent: [00:03:40]
Y si no puedes convencerte a ti mismo, si realmente, después de analizarlo y pensarlo, estás como, oh, no sé, sólo estamos en la etapa de prototipo y no puedo convencerme realmente de que las pruebas son realmente súper valiosas ahora mismo en esta etapa, entonces eso es fácil. Usted ni siquiera necesita tener la conversación. Pero para la mayoría de nosotros, no estamos trabajando en una situación en la que las pruebas son innecesarias. La mayoría de nosotros estamos trabajando en una situación en la que necesitamos escribir pruebas. Su trabajo es ser capaz de tener un vínculo tan fuerte como sea posible entre las pruebas y la misión de la empresa. Así que puedes decir que si no probamos o porque no probamos, estamos teniendo todos estos errores que estamos enviando y debido a esos errores, no somos capaces de impulsar la misión tanto como nos gustaría. 



Kent: [00:04:41]
Así que podemos resolver esto muy fácilmente escribiendo pruebas. Puede que no sea fácil dependiendo de dónde te encuentres, pero la respuesta es bastante simple. La respuesta es bastante sencilla: se trata de hacer pruebas, pruebas automatizadas, para no tener que probar todo manualmente. Ahí es donde se reduce, sólo hacer o comunicar efectivamente con las personas que toman estas decisiones, los gerentes o lo que sea, que esta es una parte importante de su retorno de su inversión de tiempo y no hacer esto es peor que hacerlo. 



Matias: [00:04:56] 
Sí, me gusta. Me gusta la idea de alinearse con la misión y vender la necesidad técnica de esto con más como la necesidad del producto. En realidad estamos resolviendo problemas y entregando productos. Así que debemos estar seguros de que estamos haciendo un buen trabajo allí, pero dejando de lado las pruebas, como siempre y todo el mundo, usted tiene una charla que siempre es interesante para mí. Y creo que ya la he visto como dos o más veces, en diferentes lugares. Y la que mencionaste que React es en realidad una herramienta de gestión de estados, no sólo una herramienta de UI. ¿Puedes resumir el concepto que quieres transmitirnos?



Kent: [00:05:38]
Sí, claro. Recuerdo que cuando empecé con React, una de las primeras preguntas que tuve fue ¿cuál es la diferencia entre props y state? Creo que mucha gente se lo pregunta al empezar. Y recuerdo haber encontrado este diagrama de flujo que Ryan Florence había hecho que describe esas diferencias. Desde el principio, React siempre ha sido capaz de gestionar el estado. Antes de entrar en React, pensaba que una gran parte de ello era que React te anima a no tener estado.



Kent: [00:06:37] 
Así que tienes tu estado que vive fuera de React, y luego sólo pasas eso a React y luego, renderiza tu cosa basada en el estado externo. Y mientras puedes hacer eso, puedes hacer todos tus componentes sin estado y luego simplemente pasarlo a través de, eso es posible. Y este tipo de encarna el, ya sabes, UI como una función de estado, una cosa que mucha gente habla. Eso no es en realidad lo que es Reactor, no es Reactor práctico. Uh, es realmente acerca de la falta de estado, es más acerca de darle una forma determinista para gestionar su estado y una forma declarativa para interactuar con las cosas que cambian con el tiempo para que usted no tiene que pensar en ellos.



Kent: [00:07:21] 
Y sólo piensas en ello basándote en el estado actual, aquí está mi UI actual. Y cuando esto ocurra, actualizaré el estado, pero no me voy a preocupar de lo que ocurra con mi IU en ese momento. Eso será un render completamente diferente y todo. Así que desde que React existe, siempre ha sido un gestor de estados. Desde el principio, la gente trató de añadir cosas a React para mejorar sus capacidades allí por varias razones que te encuentras cuando estás tratando de construir una aplicación a escala, como una aplicación realmente considerable, un término común es la perforación de prop. Y eso básicamente significa que estás manejando un, bueno, déjame dar un paso atrás.



Digamos que tienes este pequeño componente y es pequeño. Entonces estás construyendo esta aplicación, te das cuenta de que necesitas dividir las cosas en múltiples componentes. Entonces dos componentes hermanos necesitan acceder al mismo estado. Así que sólo tienes que mover ese estado hasta el padre menos común y eso es lo que llamamos levantar el estado.



Con el tiempo, a medida que continúas levantando lentamente al estado, eventualmente vas a tener algún estado que viene de la parte superior, como todo necesita acceder a este estado. Así que cuando lo estás haciendo tienes todas estas diferentes capas de componentes, tienes que pasar los accesorios hacia abajo a los componentes que lo necesitan.



La verdadera frustración es cuando tienes un componente que está muy abajo en el árbol de componentes de Reactor que necesita un estado que está muy arriba en el árbol de componentes, pero ninguno de los componentes entre esos dos lo necesita. Y así, todos los demás componentes entre estos son sólo pasar a lo largo de accesorios que ni siquiera necesitan a sí mismos.



Es que hay una relación entre los bisabuelos y el bisnieto. Eso puede ser frustrante. Esto es lo que llamamos "prop chilling", y no sólo tienes que pasar el estado, sino también el mecanismo para actualizar el estado. Sí, eso hace que sea un poco molesto tener que pasar esas cosas.



Creo que este fue probablemente el mayor desafío que llevó a la gente a empezar a explorar cosas fuera de react para la gestión de estado. Podemos hablar de eso un poco más, pero la, la otra cosa que creo que motivó a la gente a llegar fuera de react fue cuando Facebook salió con su idea detrás de flujo, que es una forma de gestionar el estado donde usted tiene este mecanismo para enviar un evento que usted maneja un evento que despacha, , en algún otro evento con alguna carga útil y luego que se establece en algún estado y luego que se propaga a través de toda la aplicación. Y, y hay varios beneficios a este enfoque y varias compensaciones que este enfoque hace, , que sólo descubrimos después de que todos se subieron a este, flex que la balsa, bajando el río, no nos dimos cuenta de que alguien se olvidó de la orden o algo así.



Todo el mundo decidió que esta es la única manera. Y entonces esta es la manera de reaccionar cuando realmente no lo es, la manera de reaccionar siempre ha sido, , tu, tu manejas el estado dentro de un componente. Si un hermano lo necesita, entonces usted levanta el estado y si ningún hermano lo necesita y sólo un hijo lo necesita, entonces empuja ese estado en el hijo.



No hay razón para que exista fuera de esa situación. React siempre ha sido una librería de gestión de estados. Pero debido a estos problemas, buscamos otras cosas y ahí es donde entró Redux, porque resolvió ambas cosas. Era una implementación de Flex, o una implementación parecida a la de Flux y, usaba la API de contexto no oficial.



Uh, que en los documentos de react, fue documentado, pero tenía esta gran advertencia que era aterrador que decía, ya sabes, no use esto, va a cambiar todo. Así que la gente no quería, pero literalmente todo el mundo era porque estábamos usando react router y que estaba usando. Probablemente estábamos usando un proveedor de temas CSS y JS que lo estaba usando.



Y luego Redux lo estaba usando. Y así todos estamos usando esta API para resolver el problema de la perforación previa. Y, y en realidad había algunas otras implementaciones mucho más simples de la API de contexto que utilicé. Hubo uno llamado react broadcast por Michael Jackson que realmente me gustó.



Fue increíble. Sólo para que sea más fácil para obtener su estado de uno de la parte superior del árbol hacia abajo, , Pero, sí, así que yo, yo usé Redux por un tiempo y, por el tiempo suficiente para mí para darse cuenta de que no estaba super feliz con él. Terminé abriendo como 30 archivos para hacer un solo cambio. Uh, no disfruté de eso en absoluto.

Sólo lo he utilizado para un proyecto. Tampoco lo elegí para ese proyecto. Entré en el proyecto que ya lo tenía, y luego cualquier otro proyecto después de eso, ese fue el único proyecto con el que usé Redux sólo porque vi que resolvía muchos problemas. pero si cambio mi enfoque, no tengo esos problemas.

No necesitaba preocuparme por ello. Así que de todos modos, eso es, eso es una larga manera de decir que sí, reaccionar es un gestor de estado.



Matias: [00:12:15] 
Mencionaste dos cosas que quiero como gritar, esta idea de, no necesitas resolver el problema que simplemente no tienes, o simplemente no lo declaras que tienes, y la gente tiende a, o solía pensar que la perforación de prop es un problema. Así que tenemos que resolverlo incluso antes de tenerlo y usamos redux y cualquier otro, un montón de posibilidades allí. Pero en realidad hay otro concepto que es nativo de Reactor, que es la composición. Y siento que sí, los estudiantes y los principiantes en realidad no utilizan la composición en absoluto. Es como los niños bajo los niños bajo los niños, pero no hay otra idea allí, su composición. ¿Puede usted, tipo de, , hablar de eso.



Kent: [00:12:59]
Sí, sí, absolutamente. Así que, y estoy bastante seguro de que mencioné esto en la entrada del blog. No lo hice originalmente, y lo añadí después porque era una parte evidente, que faltaba en esa entrada del blog. Así que la composición es como, digamos que usted está construyendo un poco de interfaz de usuario basada en el chat y quiere tener, no sé, usted está manejando un poco de estado en el nivel superior que dice que los usuarios están actualmente conectados. Y luego tienes esta barra lateral aquí que enumera esos usuarios y tiene que estar en el nivel superior porque también tienes otra cosa que indica el recuento total de personas que están actualmente conectadas o algo así. Así que eso tiene que estar más arriba en el árbol. Pero, pero tienes dos cosas, dos componentes que están más abajo en el árbol que necesitan acceder a estos datos. Así que una cosa bastante natural que la gente hace cuando están escribiendo reactores es que tienen un componente que hace esta cosa, y luego esos, esos componentes hacen esta cosa y, y esos componentes hacen esto, estas cosas.



Y así, cuando haces cosas así, naturalmente tienes que apuntalar el taladro. Así que tienes que pasar este valor hacia abajo a ese. Luego hacia abajo a ese y hacia abajo a ese todo el camino hasta llegar a donde estás. Sin embargo, ¿qué pasa si en lugar de, , y, y a menudo estos otros componentes son una especie de raperos y a menudo son como componentes de diseño. Uh, por lo que es como, bueno, tengo mi, mi barra lateral, pero eso es dentro de mi nav principal para algo así. Y entonces, , y por lo que hacen que el principal responsable de la representación de la barra lateral, , donde en realidad no hay estado siendo gestionado por el principal. No hay nada que diga que tiene que ser el responsable de la barra lateral. Así que si, en lugar de decir, Hey, voy a renderizar el principal y que es responsable de la disposición. Y luego, , voy a pasarle lo que quiero que ponga en él como los niños para ese diseño. Así que voy a ser responsable de decir lo que usted renderiza en las diferentes partes de lo que usted está poniendo.



Esto significa que el componente de nivel superior puede renderizar la barra lateral por sí mismo. Y así no hay perforación de prop, , de ningún tipo, porque el componente de nivel superior puede simplemente pasar esas indicaciones directamente al componente que lo necesita. Uh, es un poco difícil describir esto de forma audible. Así que, , el blogpost tiene un ejemplo, y, y en realidad hay un video de Michael Jackson donde explica esto muy bien.



y, y en realidad Michael Jackson hizo ese video porque, él estaba haciendo la sugerencia de que,, la mayoría de las aplicaciones no necesitan contexto en absoluto. ...lo cual creo... Usted podría ser capaz de salirse con la suya, , tal vez, pero no lo hago. Creo que la mayoría de las aplicaciones probablemente tienen al menos uno o dos casos de uso útil para el contexto, pero en espíritu es correcto.



El contexto es útil sobre todo para las bibliotecas, lo que creo que es el caso. Pero, de todos modos, si como, como usted dijo, también, , si usted cambia su enfoque de la, sólo la forma en que usted está escribiendo sus componentes, entonces usted puede simplemente eliminar el problema de la propulsión por completo y usted no tiene que llegar a contexto.



Y, y la otra cosa que, que reaccionó para ayudar a eliminar el problema de la perforación rápida, o al menos, reducir el impacto de, de prop babeo es haciendo contexto oficial y hacer que sea una API bastante sencillo de usar en relación con lo que solía ser, , antes de ganchos y esas cosas. 



Matias: [00:16:33]
Eso fue realmente útil.

Y al mismo tiempo, creo que fue una especie de daño al concepto de composición en términos de como un contexto tan fácil de usar que sólo lo utiliza y la gente va a empezar a caer en los mismos patrones que con redux, como, era tan fácil de empujar todo lo que se hace sólo con él. Pero por alguna razón, la composición no es ni siquiera enseñado por los instructores de todo el mundo, como el uso de este patrón de render prop como, porque es una especie de similar donde se pasa el componente como un prop, no los datos. ¿Y por qué crees que es tan difícil enseñar o aprender la composición y utilizarla realmente? Y porque he estado en un montón de proyectos de React y sí, este no es el patrón. Esto es, puedes encontrarlo, pero no es lo habitual 



Kent: [00:17:28] 
Sabes, tienes razón. Y en realidad, no creo que haya hablado de ello directamente ni siquiera en mis propias cosas. Lo uso de forma natural en la forma en que construyo cosas, pero no lo enseño específicamente. Y eso cambiará en una próxima versión de epic react. Voy a incluir una sección sobre el aprovechamiento de la competencia. Porque esa es una de las cosas geniales de Reactor. Así que eso es como una de las principales características clave



Creo que veo los componentes de react como funciones, que son, por supuesto, pero, incluso el JSX que veo es como las funciones que usted está pasando estos argumentos a estas funciones y no realmente a menudo aprovechar la composición, incluso en nuestras funciones. No tan fuertemente como lo ves cuando estás aprovechando la composición con react, donde sólo pasas esta función y pasas esta llamada a esta función, a esta otra función y cosas por el estilo. Creo que hay algo en nuestros cerebros, se siente más natural decir, bueno, aquí está este bloque de cosas.



Voy a poner esto en una función. Y ahora esta función es responsable de este bloque de cosas donde en realidad esa función sólo está a cargo de lo que una parte de eso y el resto se puede pasar como un argumento. Creo que ese es el gran desafío allí es que no parametrizamos lo suficiente cuando se trata de nuestro componente, 

Matias: [00:19:00]
Es una especie de modelo mental que vienes con un modelo mental imperativo, como la mayoría de nosotros. Y luego hay que cambiar un poco, como en el camino de la programación funcional, como declarativo, más donde la composición es una especie de rey, pero estamos tipo de caer en el medio con JavaScript y reaccionar en sí. 



Kent: [00:19:24] 
Sí, yo diría que, que una de las cosas más interesantes de JavaScript es su flexibilidad para, , atender a los diferentes casos de uso de la gente para la forma en que les gusta escribir su código, , ya sea funcional o, , orientado a objetos o, o lo que quieran.



Y así, , Porque JavaScript es tan flexible de esa manera, pero también, porque es tan omnipresente para bien o para mal, es el lenguaje de la web. Y es el lenguaje más popular en el mundo y la gente tiene que usarlo quieran o no. En muchos casos, tienes un montón de gente con diferentes antecedentes y preferencias, de lo que sería en, en un diferente, un lenguaje en una plataforma diferente.



porque no sólo están en diferentes entornos, sino que también están desplegando a diferentes objetivos y tienen diferentes casos de uso y, y todo tipo de cosas. Así que ninguno de ellos está necesariamente equivocado. Son sólo, son sólo diferentes casos de uso y diferentes preferencias. Y creo que debido a eso, tenemos una gran variedad de, , de, sólo la forma en que la gente escribe su código.

, cuando están ejecutando javascript 



Matias: [00:20:33] 
Tiene sentido. Avanzando con esta parte de la cosa del estado, tema, en la charla y, y otros lugares que son una especie de apoyo muy duro en la consulta de reacción y diciendo básicamente lo mismo que Tanner ha dicho o Tanner dijo lo mismo que hiciste, No sé - que el estado es en realidad dos naturalezas diferentes.

Uno es la interfaz de usuario y reaccionar es una herramienta y uno es un estado del servidor que o caché que es reaccionar herramienta de consulta. Así que entiendo que su reac-query es su atasco aquí. Y, pero puede poco describir esta diferencia entre la naturaleza del estado? 



Kent: [00:21:10]
Absolutamente. Descubrí o empecé a pensar en esto, tal vez hace dos años, cuando me di cuenta de que podríamos simplificar drásticamente nuestro estado de la interfaz de usuario si no tratamos el estado del servidor como su estado de la interfaz de usuario.



Y abrazar el hecho de que el estado del servidor es un efectivo. Y así Tanner y yo, Tanner vive muy cerca de mí en realidad. Y así que estábamos almorzando y él estaba hablando de esto antes de crear la consulta de react. Y él está diciendo que he estado construyendo algunas utilidades realmente interesantes para, para mi aplicación en el trabajo.



y hablamos de ello un poco, y luego salió con react query y fue un cambio de juego para mí. Sí, sólo cuando se separa su, lo que, por lo que en primer lugar, cuando usted abrazar el hecho de que su estado del servidor es una caché, , en lugar de, es sólo un estado que necesita para mantener actualizada, que hacer un par de cosas diferentes.



Así que una cosa que hice mucho antes fue, , cuando yo haría una actualización de, así que permítanme dar un paso atrás cuando, cuando usted está construyendo algún estado de la aplicación, algunas cosas de la interfaz de usuario, olvidando el servidor, cuando hay una actualización, se actualiza ese valor en la memoria. Así que usted está diciendo establecer el estado o establecer, , estado modal o lo que sea que usted está, usted está actualizando.



 Y así es como operamos de esa manera cuando estamos. Así que cuando traemos en el servidor y estamos empezando a hablar sobre el estado del servidor, sólo tipo de sensación natural para seguir adelante y actualizar ese estado y luego tal vez tener un useEffect o algo que vamos a actualizar en el backend.



...y más a menudo lo que terminamos haciendo es decir, no, no quiero tener una inconsistencia aquí. Así que voy a decir, ir a hacer esta solicitud de obtención para ir a actualizar esto. Y entonces me devolverá el nuevo estado y actualizaré mi estado local para que sea el nuevo estado. Y, en realidad, Apollo hace esto mucho, no, no es para criticar a Apollo ni nada.



Están resolviendo grandes problemas, pero tratan de mutar su caché para que coincida con lo que reciben del backend.  Y react query tiene un enfoque diferente.  Creo que, como, usted debe ser capaz de, para hacer que el trabajo, pero reaccionar consulta sólo dice, oh, usted hizo una mutación. Déjame ir a buscarlo de nuevo.



porque aceptas el hecho de que es un caché y, cuando haces eso, tienes que decir, tan pronto como obtengo estos datos, son obsoletos. Está mal. Uh, sólo, aceptas ese hecho. Y así estoy haciendo una solicitud adicional para ir a decir, de acuerdo, hice una mutación, déjame ir a obtener lo que el estado actual es y poner todo eso dentro de la consulta de reacción como un paquete significa que usted no tiene que preocuparse por mantener ese estado hasta la fecha a ti mismo.



Y así se simplifica drásticamente la gestión de sus cosas. Yo solía tener, como estos proveedores de contexto realmente grandes que tenían todos estos métodos diferentes o que estaban en un reductor, todos estos diferentes, ya sabes, cosas de reductores de declaraciones de conmutación para gestionar como, oh, lo agregué para hacer lo que tengo que empujar a la, la lista de matrices o lo que sea, pero con react query, ahora sólo digo seguir adelante y agregarlo a la API de backend y luego react query se encarga de obtener el estado fresco para mí. Este enfoque tiene sus desventajas, pero también hay formas de evitarlas, pero me gusta el valor por defecto que me da react query, que me hace más correcto.



Y, , porque he movido todo el estado del servidor a esta caché. Ahora lo que me queda para el contexto o la composición o lo que sea es muy simple. Y si estoy co-localizando mi estado, a menudo ni siquiera necesito algunas de esas cosas en un proveedor de contexto, simplemente lo pongo en el área de la aplicación que se preocupa por ese estado.

Y así, sí, el, , react query ha sido fenomenal para mis aplicaciones del lado del cliente. Realmente no lo uso mucho para cosas como remix, , porque remix elimina los problemas que react query resuelve. Y podemos hablar de eso si quieres. Pero, , para, si estoy haciendo una aplicación del lado del cliente, , cien por ciento, voy a estar usando react query. Me ahorra mucho tiempo. 



Matias: [00:25:11] 
Sí. Una de las cosas que me resonó fue esta diferencia de que básicamente un estado de la UI es síncrono y el estado del servidor o de la caché es asíncrono, y tienes todo el paquete en una solución realmente genial e inteligente. Así que no tienes que preocuparte por la sincronización de esos datos.



Y entonces sólo te preocupas de tu propia lógica, básicamente, porque los estados del servidor no son tu lógica, pertenecen a otro lugar. Así que eso me resuena mucho. Uh, sí. Quiero preguntar sobre el remix también, pero tengo mucha curiosidad, pero tengo otra pequeña pregunta ahí y estoy seguro de que recibes esta pregunta muchas, tantas, tantas veces que ya tienes un post sobre ello.



Uh, pero de todos modos, bueno tienes un post para casi todo junto con un gif. UseEffect es tan complejo como para que la gente simplemente suelte las dependencias en el useeffect y sólo siga las reglas. Como, eh, como tienes otra charla. Creo que se llama, "common react pitfalls" donde bromeas como las reglas de LinkedIn es Diana Vermont diciendo, usa estas cosas críticamente. 



Eh, lo sé, eh, Por qué, por qué la gente sólo, por qué usted, si usted piensa que es tan difícil de seguir estos efectos, la sincronización o permanecer sincronizado por el móvil, que el uso de efecto necesidad. 



Kent: [00:26:46]
Creo que hay varias razones por las que la gente se esfuerza por seguir la regla del linting. Si ya tienes experiencia con react, entonces tu reto es desaprender. Con esto quiero decir que si tienes experiencia con los componentes de clase de Reactor, estás pensando en los componentes de Reactor de una manera antigua. La forma en que solíamos pensar en ellos era ciclos de vida. Y entonces piensas, bien, cuando el componente se monta, y luego cuando el componente se actualiza, entonces cuando el componente se monta, quiero que estas cosas sucedan.



y con efecto de uso. Porque realmente no funciona de esa manera. Tratamos de hacer que funcione de esa manera, porque estamos pensando en, la forma en que, solíamos, pensamos en los componentes y los ciclos de vida, pero esa no es la manera de pensar en esas cosas. Así que, creo que es uno de los, los principales para las personas que han tenido experiencia con react ya, , es que están tratando de doblar el efecto de uso para operar en los ciclos de vida, , en lugar de sincronizar el estado del mundo con el estado de la aplicación.

...así que otra razón es que... ...a veces no entendemos o la gente no entiende cómo funciona la matriz de dependencia. ...así que el hecho es que tienes una matriz que proporcionas al efecto de uso y, cada vez que cualquiera de esos elementos cambia, incluso si es la misma forma exacta de un objeto, si es un objeto nuevo, va a desencadenar una repetición de tu efecto de uso.



Y si no entiendes eso y ves que tu efecto de uso se está ejecutando una y otra vez, vas a decir, bueno, vale, no importa. Yo sólo, , voy a apagar la regla y entonces tu, cuando apagas la regla, estás encendiendo un error. Eso es, eso es realmente lo que es. ...es como encender el modo de bicho, supongo, si quieres pensarlo así.



, pero, Pero su gente está haciendo esto porque están terminando con un bucle infinito porque se utiliza efecto llamado set state o algo así. y, o incluso peor que está llamando a una API y luego llamando a set state. Y así, si usted tiene, una dependencia siempre cambiante, usted es sólo para siempre llamando a esta API y luego se obtiene la tasa limitada o algo así.



Me gustaría poder decir que nunca he hecho eso antes. Oh, sí. Todos lo hemos hecho. Sí. Así que sí, nos gusta, quitamos las dependencias por desesperación, , por eso. Y es porque no entendemos que, ya sabes, , cuando creas un nuevo objeto, estás creando, incluso si todas las propiedades son las mismas, estás creando una nueva referencia a, una cosa completamente diferente.



...y es, honestamente, bastante complicado. Y tienes que tener una buena comprensión y como, Por un lado, si no tienes una buena comprensión de la forma en que JavaScript funciona y cierres y, ya sabes, , JavaScript pasa por valor y cosas por el estilo, entonces, , , entonces es sólo una cosa que está en su camino, y usted no entiende por qué está causando tantos problemas y eso es, eso es frustrante.



Uh, así que no, realmente culpo a la gente por querer apagarlo y seguir con la vida. ...pero como dije, están encendiendo, en modo difícil, modo negro. ...pero, sí, el otro... El punto de todo esto es que creo que el uso de hecho es un nivel muy bajo primitivo. ...y lo que es realmente impresionante acerca de los ganchos en general es que nos da la capacidad de abstraer las cosas muy bien de una manera que nunca podríamos con los componentes de clase.



Probamos con, con accesorios de renderizado y componentes de orden superior y esas cosas, pero, y, y eso realmente funcionó bastante bien. Yo estaba bastante feliz con los accesorios de renderizado. Uh, en general había, había diferentes problemas con él, pero cuando los ganchos llegaron, , tantos problemas fueron simplemente eliminados porque ahora podemos compartir el código de la misma manera, compartir el código de react y la lógica de react de la misma manera que compartimos cualquier otro código y eso es haciendo una función y lo llamamos un gancho personalizado, pero es sólo una función que utiliza otros ganchos.

Eso es todo lo que es un gancho personalizado. Y así, yo, me estoy encontrando con el uso de efectos cada vez menos como estoy usando otros, bibliotecas. ¿Y qué es lo bueno de eso? Soy un autor de la biblioteca, por lo que es bueno para mí para entender cómo funciona todo esto, pero el más,, buenas abstracciones que construimos, menos la gente realmente tiene que utilizar, utilizar afectar a sí mismos.



Y, y muchas de las veces que estoy viendo en mi comunidad de discordia o en línea es, la gente está usando el efecto de uso para hacer un montón de las mismas cosas para las que hay bibliotecas desarrolladas que, , Sugiero que la gente use, , react query es un ejemplo perfecto de esto. Así que mucha gente está usando react query o use, , haciendo llamadas fetch ellos mismos y cosas así.



Cuando digo, ¿por qué no usas react query? Uh, y entonces no tienes que preocuparte por las dependencias. Y otra cosa sobre el efecto de uso que hace que sea un poco difícil es que tan pronto como se abstrae algo, fuera de un componente. Así que usted está tratando de hacer su propio gancho personalizado o algo así.



Si esa lógica está usando el efecto de uso, entonces algunas otras cosas se vuelven complicadas también, porque ya no tienes acceso directo a las variables que, ese interno podría estar usando, especialmente si, , estabas, si quieres que sea abstracto, como lo que sucede en el uso de hechos con algún tipo de devolución de llamada o algo así?

Uh, porque ahora, usted no puede poner la devolución de llamada directamente en el uso de hecho, ¿quieres generar eso? Y entonces ahora tienes que aceptar eso como un parámetro. Y ahora, a medida que las cosas se rerenderizan, ese callback podría cambiarse, podrías terminar con un kosher más cercano. Así que tienes que memorizar eso o, o tienes que usar este último patrón de ref.



Así que la abstracción del efecto de uso es creo que otra cosa que, , hace que la matriz de dependencia, y no es sólo el efecto de uso, también se utiliza memo y que acaba de llamar de nuevo, pero hace que la matriz de dependencia un poco difícil, , porque. No se puede simplemente inline cosas. Estos ganchos son, funcionan mucho más fácil si sólo inline todo, pegar todo lo que necesita directamente en esa devolución de llamada.



...pero, sí, es, es genial porque cuando tienes, cuando entiendes esas cosas, puedes construir algunas abstracciones realmente impresionantes que no puedes hacer antes. Por eso digo que el efecto de uso es una primitiva de bajo nivel sobre la que puedes construir otras abstracciones geniales para que la mayoría de la gente no lo haga, incluyéndote a ti mismo, para que no tengas que preocuparte de usar efectos de uso en tu código de aplicación normal.



Matias: [00:33:25] 
Sí. Dos preguntas. Uh, ¿tienes algún recurso en particular con consejos y trucos para moverse con el efecto de uso, como el uso de una visión condicional del hecho sólo para evitar, para sacudir ese valor particular o lo que sea. Y segundo, ¿crees que el efecto de uso es de alguna manera una escopeta. Dispara a las armas. Dispara. 

Kent: [00:33:44]
Sí, sí.

Pistola de pie. Sí. Así que primero tengo algunos artículos muy buenos sobre epic react. Si vas a epic react.dev/articles, , así como en mi propio blog, Kent C dodds.com/blog, , donde hablé de usar efectos y también usar memo y, y, usar callback, también. Esos son, similares debido a la dependencia your'e situación.



...así que sí, esos son algunos recursos realmente buenos. Uno de ellos en particular es el, bueno, ahora debería, debería buscarlo. Así que te doy el título correcto. Es cómo react utiliza los cierres. Sí. Cómo react utiliza los cierres para evitar errores. Y eso describe la diferencia principal entre los componentes de clase de Reactor y los ganchos, y cómo Reactor ha cambiado el valor por defecto. 



Puede parecer que es más difícil, pero termina ahorrando un montón de dolor, en el largo plazo. Uh, y luego también tengo otra entrada de blog en allí atado a la última ref patrón en reaccionar, que resuelve muchos de los problemas que la gente encontraría, cuando están tratando de hacer algo similar a lo que solíamos tener en, , en componentes de clase.



En realidad es un patrón muy simple. ...pero es muy poderoso cuando construyes abstracciones. ...pero, sí. Así que tu, tu segunda pregunta sobre por qué es un uso efectivo de la pistola de pie. 



Matias: [00:35:17] 
si crees que es porque sí, la API de nivel inferior es realmente difícil de usarla, pero al mismo tiempo es inferior, pero es, es describirla como una de las básicas que necesitas aprender para desarrollar realmente una agregación.

Así es, 



Kent: [00:35:32]
Sí. Sí, eso es cierto. Yo diría que el efecto de uso es, es relativamente avanzado, pero el hecho es que es muy simple. Como podría, podría explicarte lo que es el efecto de uso en dos o tres frases y cubrir todo. porque es una cosa relativamente simple. El reto es que, , en la aplicación práctica, puede ser difícil de hacer bien.



Uh, y, y no es fácil. Se basa en, , varios conceptos que la gente no tiene super, , clavado cuando están trabajando con JavaScript. ...y porque, o, perdón, déjame decirlo de otra manera. Se basa en, , o en ser capaz de usarlo efectivamente. Depende de lo bien que entiendas estos conceptos fundamentales de JavaScript.



Y así, si no entiendes, el hecho de que el render realmente recuerda tu función y lo que eso implica sobre las, funciones que estás creando dentro de tus componentes, así como las variables que estás creando dentro de tu componente. Sí. Si usted no tiene esa comprensión, entonces puede ser absolutamente una cosa difícil de hacer bien. 

...entonces, ¿es un arma de pie? Sí, tal vez, , potencialmente, pero creo que sigue siendo el enfoque correcto. Sólo porque algo sea difícil no significa que esté mal, , que puedas encontrar lo correcto encontrando lo que es simple porque no puedes construir una aplicación simple con abstracciones realmente complejas.



Es que eso no se puede hacer. Sin embargo, puedes construir una aplicación simple con abstracciones simples y, , y también puedes construir una aplicación compleja con abstracciones simples. No es como una bala de plata o algo así, pero, sí, si tienes simples, , primitivas, entonces puedes construir una aplicación simple a partir de eso y puedes construir abstracciones simples sobre ella.



Eso es lo que creo que es el efecto de uso, está destinado a. Vamos a proporcionar algo que es simple. La idea es sincronizar lo que ocurre fuera de Ray o sincronizar lo que ocurre dentro de react con cosas que están fuera de react. Ese es todo el objetivo de use effect.



Y, , y luego la gente puede construir en la parte superior de eso, para, para hacer buenas abstracciones para que la mayoría de la gente no tiene que trabajar con el perímetro de bajo nivel. 



Matias: [00:37:54]
tiene sentido. Quiero saltar a otro tema antes de que se acabe el tiempo y que te metas de lleno en TypeScript. Yo soy un desarrollador de JavaScript desde hace mucho tiempo, pero ahora te estás moviendo a, eh, lo que la onda nos da.



Eso es TypeScript. Todo el mundo está escribiendo TypeScript ahora mismo. Así que la pregunta es realmente sencilla. ¿Por qué escribir TypeScript? ¿Por qué TypeScript? 



Kent: [00:38:19]
Sí. Sí. Así que en realidad he estado usando TypeScript durante, , Tres o cuatro años. , pero yo, yo decidí durante mucho tiempo, hace mucho tiempo, y en realidad antes de que era el flujo. , Yo uso el tipo de flujo en PayPal durante mucho tiempo.

...pero, sí. , creo que reaccionar todavía está escrito en el flujo y esas cosas, pero sí, eso fue los únicos. Sí. Sí, de verdad. Así que sí, decidí no añadir tipografías a mi material de código abierto y a mi material educativo, porque no quería que fuera una barrera para que la gente se metiera en él. especialmente para el código abierto.

Simplemente sentí que no, no quiero limitar la gente que puede, participar en mis cosas de código abierto a los que saben TypeScript, porque hay menos gente que sabe TypeScript. La cosa es que. Y la gente que sabe TypeScript también sabe JavaScript, pero la gente que sabe JavaScript no necesariamente sabe TypeScript.



Así que si voy con el mínimo común denominador, puedo llegar a más gente tanto en mi código abierto, como en mi material educativo. Pero hace unos meses cambié mi forma de pensar después de hablar con Ryan Florence, porque me dijo que estaban empezando a pasar su material a TypeScript.

Y yo dije, bueno, ¿y esto? Y él dijo, por qué. Cuando nos pusimos a dar estos talleres, dijimos que quién usaba TypeScript y literalmente todo el mundo levantó la mano. Y, , y además, mientras ayudábamos a la gente a trabajar en los ejercicios y otras cosas, vimos que, estaban realmente confundidos cuando no tenían autocompletado para diferentes cosas básicas.



Y fue realmente frustrante para ellos. Y si lo haces bien. para el material educativo, puedes hacer que, para los estudiantes, TypeScript es mayormente opcional. ...así que configuras TypeScript para no tener que escribir todo, ya sabes, cualquiera está bien, lo que sea. Y así, si soy un desarrollador de JavaScript normal, la única diferencia para mí es que el archivo termina en punto TSX.

Todo lo demás es igual. No tengo que preocuparme por ello. Uh, y luego además de eso, si hay, , utilidades que son proporcionadas por, el, como parte del material que estoy llamando a esta función, estoy recibiendo auto-completar, que es realmente útil. Uh, incluso si sólo soy un desarrollador de JavaScript regular y no me importa sobre TypeScript.



Y así, si configuras las cosas, bien, , incluso los alumnos no tienen que saber TypeScript para poder utilizar un taller que está principalmente en TypeScript. Y, en el lado abierto, me he estado diciendo a mí mismo esto durante mucho tiempo que, mi preocupación sobre, TypeScript siendo una barrera de entrada, era simplemente falso, porque espero que la gente escriba pruebas, además de implementar lo que sea que estén haciendo y el script táctil es sólo pruebas.



Al final del día, eso es, eso es todo lo que es. Y así que ya estaba esperando que la gente, como yo ya tenía una barrera de entrada en el lado de la prueba de las cosas,, aprender a añadir algunos parámetros y esas cosas. ...ya sabes, tipos perimetrales y cosas así, no es mucho pedir. Concedida la biblioteca, TypeScript es mucho más difícil que el script de tipo de aplicación.



Así que veremos cómo se desarrolla todo esto, pero, y tal vez hay algunas personas que ya han tratado de contribuir a mi material de código abierto y decidieron no hacerlo, porque era TypeScript y me siento mal por eso, pero al final del día, el, el producto final es mucho mejor para la gente. Así que estoy bien con el intercambio porque lo bueno de TypeScript es que sí, son pruebas, pero también son pruebas que puedes entregar a los consumidores.



...porque las definiciones de tipo también están ahí, así que... sí, eso es... sí. Sí, es fantástico. Me encanta ser un consumidor de mis propias cosas ahora que todo está muy bien escrito. ...así que sí, ahí es donde ha estado el cambio públicamente. ...pero sí, he estado usando JavaScript mecanografiado durante mucho tiempo y, y, me parece obvio, realmente como es.

En realidad, nunca me gustó trabajar sólo en JavaScript después de que empecé a usar Flo y TypeScript en PayPal hace varios años. Pero lo hice por esas razones y no lo hago ahora por esas otras razones. 



Matias: [00:42:35] 
Sí. Tu ordenador escribiendo TypeScript y luego volviendo a jugar con JavaScript.



Es algo así como, volver a los noventa. Sí, no, nunca más. Una pregunta más con TypeScript. Eh, ahora estás creando entradas de blog de material, principalmente con TypeScript. ¿Crees que vas a trasladar Epic React a eso también?



Kent: [00:42:54] 
Absolutamente. Todo lo que estoy haciendo se está moviendo a TypeScript.

Así que, , probando javascript.com también será todo TypeScript cuando haya terminado. Uh, y epic reacts será todo TypeScript. Uh, antes de actualizar cualquiera de esos, sin embargo, estoy trabajando en un par de talleres de TypeScript, , porque quiero, para las personas que simplemente no tienen experiencia con TypeScript o que quieren subir de nivel su TypeScript, quiero darles un lugar para ir antes de ir a través de epic react y, y pruebas de JavaScript.



Así que puedo, por lo que si dicen, Hey, no puedo ir a través de epic react. No sé un TypeScript. Puedo decir, bueno, no, pasar por esto primero. Y entonces usted puede ir a través de epic react. No será un problema. Así que, , bueno, lo que estoy haciendo ahora mismo es que estoy actualizando todo el material y luego voy a hacer una, una especie de pequeña encuesta sobre mi material y ver qué características de TypeScript estoy usando.

Y me aseguraré de incluir todo eso en, estos tipos de talleres agarrados que la gente puede pasar primero. 



Matias: [00:43:52]
Bien, bien. Eso va a estar muy bien. , para terminar, creo que este rodaje para remezclar.



Kent: [00:43:59]
Sí. Me encantaría hablar de la remezcla. ¿Qué quieres saber? 



Matias: [00:44:03] 
Uh, pero básicamente todo lo que no era capaz de, lo siento, mi llamada, lo siento, Ryan. No pude finalmente comprar mis propias lecciones en ese momento. , pero lo haces así puede, puede tipo de resumir de nuevo y es corto en, es sólo LD, pero ¿por qué remezcla tiene tan emocionado, como, para mí, es una especie de similar en algún momento acabamos de hablarlo por lo que yo sé, pero sí, soy todo oídos aquí.



Kent: [00:44:31]
Así que tengo cero experiencia con el kit de fieltro. Y en realidad tengo una experiencia bastante limitada con Next JS, con el que mucha gente compara la remezcla. Pero por la experiencia que tengo, no se parece mucho a Next JS. A mí me gusta. Hay mucha coincidencia en los casos de uso que pueden manejar, pero son bastante diferentes en muchos aspectos.



La cosa que, el elefante en la habitación, así que voy a abordar que rápidamente es, remezcla tiene licencia, , software donde usted tiene que comprar una licencia para utilizar el software. Esto va a eventualmente planear, tener un período de prueba para eso. Sé que mucha gente está realmente frustrada porque no hay manera de probarlo y ver si, si te gusta.



Uh, así que están planeando tener un período de prueba eventualmente. , pero en este momento son, son todavía . ...y por eso están ahí. Uh, centrándose en las personas que, , están dispuestos a pagarles para, , para trabajar en él para que puedan alimentar a sus familias y esas cosas. 



Matias: [00:45:35]
Creo que es un código abierto bastante impresionante para el modelo.



Kent: [00:45:40]
Estoy totalmente de acuerdo. Mucha gente se siente como si hubieras ofendido a su madre cuando sugieres que un software como este debería ser de pago, lo cual no entiendo en absoluto, pero, , sí. Algunas personas se sienten así. ...pero, sí, así que la remezcla, ¿por qué es tan impresionante? Me encanta la remezcla porque siento que abraza los fundamentos de la web de la manera que, , que siempre deberíamos haber estado abrazando esos fundamentos.



...así que, pasamos mucho tiempo, resolviendo problemas con JavaScript. Eso es lo que hacemos como humanos. Resolvemos problemas. ...y porque somos tan buenos resolviendo problemas, o al menos lo disfrutamos tanto... ...y tendemos a buscar problemas también. ...y cuando empezamos a necesitar hacer más cosas en el navegador con JavaScript...



Y, , y así, porque estábamos corriendo en el navegador, que era, que era el área de programación que nosotros, que poseía y, las estructuras del equipo tipo de cambio. Y así, usted tenía el equipo de front-end y el equipo de back-end. Y así, si usted necesita para resolver un problema en ese entorno, usted no va al equipo de backend.



Dijiste, ¿cómo puedo resolver esto sin hablar con el equipo de backend? Y así resolveríamos todo tipo de problemas, como el almacenamiento en caché. Así que no llamamos al backend si no es necesario o lo que sea, con, como tantas cosas diferentes que es, que hacemos como solucionadores de problemas. Y especialmente cuando, como gran parte de nuestras cosas con el lado del cliente ahora, las cosas se están moviendo más hacia una especie de enfoque híbrido con la hidratación y la representación del lado del servidor y esas cosas.



...pero aún así estamos en JavaScript y queremos usar nuestro JavaScript para resolver nuestros problemas. Y se nos ocurren estas soluciones muy, muy complicadas para, para estas cosas. Así, por ejemplo, digamos que estamos usando nuestra propia cosa Webpack, todo es cliente, y decimos, oh, sabes qué, hay un problema de SEO aquí.

Necesitamos pre-renderizar estas cosas, pero no quiero administrar un servidor. He estado disfrutando mucho enviando estos archivos JavaScript y HTML a los cubos de AWS S3. Y no quiero perder eso. Así que lo que si en lugar de pre, nosotros, porque reaccionar puede ejecutar un nodo. Puedo ejecutar este pequeño. Uh, script que generará todos los archivos HTML para todas las páginas.



Y luego envío eso a S3 y, y ahora todavía tengo la experiencia de despliegue agradable que he tenido sin tener que hablar con los ingenieros de backend o sin tener que gestionar un servidor. Y, , Y entonces yo, y sólo rehidratar todo en, , ya sabes, en el arranque y, y eso es lo que es Gatsby o reaccionar estática.



Uh, es este generador de sitios estáticos. Y, funciona, es una solución al problema de los problemas de SEO y, y, y varias otras cosas. Mejora el rendimiento percibido también. ...pero viene con toda una serie de otros problemas que una compañía entera ha estado trabajando para resolver durante años. Y, uno grande de esos problemas es lo que si tengo una tienda con muchos productos o cuando yo era un PayPal, trabajé en paypal.me y todo el mundo tiene su propio enlace. Y así evaluamos Gatsby y fue muy rápidamente obvio que esto no funcionaría porque tenemos millones de usuarios. Y así como tú, no puedes hacer eso. 



Se necesitarían semanas para construir todo, para construir todas esas, esas páginas HTML y la gente dirá bueno, pero lo bueno es que puedes cobrarlo y esas cosas, pero literalmente cada vez que vuelves a desplegar, estás volando todo tu dinero.



Y de hecho, Netlify está construido expresamente para hacer volar su dinero en cada despliegue. ...y esto no es necesariamente algo terrible porque Netlify es un CDN... ...pero el hecho es que está construido con eso en mente, donde si cambias el enfoque, puedes eliminar todos estos problemas en primer lugar.



Y creo que eso es lo que hace la remezcla: cambia el enfoque de tal manera que elimina muchos de los problemas que nos creamos al hacer todo en JavaScript. ...ahora estamos intercambiando problemas, ¿no? No es que eliminamos todos los problemas y eso es todo lo que hacemos. También estamos intercambiando, , por diferentes problemas porque ahora sí tenemos que manejar un servidor.



Ahora, voy a decir antes que nada que remix está planeando o es, , no es exactamente una ciencia de cohetes para hacer el soporte de remix, la generación de sitios estáticos, o completamente renderizado del lado del cliente. Y de hecho, creo que planean apoyar eso con trabajadores de servicio. Así que se ejecuta remix en el servidor, por lo que puede tener una aplicación totalmente fuera de línea con remix.



Por lo tanto. Remix será capaz de hacer estas cosas, pero el valor por defecto es lo que es mejor para ti y mejor para el usuario. Uh, a pesar de que ahora tienes que gestionar un servidor, lo bueno es que hoy en día tenemos servicios que nos permiten manejar miles de solicitudes por segundo por como 10 centavos de dólar al día. Es como, es ridículo lo barato y fácil que es gestionar estos, , objetivos de despliegue.



Yo diría que no es tan fácil como simplemente enviar un par de archivos a un cubo de S3, pero es llegar allí y es, usted S y entonces usted también tiene que preocuparse por como, por lo que la única razón por la que estoy mencionando esto es porque la gente siempre trae esto cuando digo esto. ...pero dicen, bueno, una de las cosas buenas de enviar archivos JavaScript y HTML a S3 es que ahora no tengo que preocuparme de que el servidor se cuelgue y de los problemas de ejecución, y no, no, tienes que preocuparte de los problemas de ejecución porque tu código se va a ejecutar.



Se va a ejecutar, si se ejecuta en el servidor o el cliente no hace ninguna diferencia, usted tiene problemas de tiempo de ejecución. Y por lo tanto, no es diferente con esto. La única diferencia real es que ahora tienes un servidor, que si estás usando cualquiera de estos servicios, que probablemente deberías, entonces, , entonces es básicamente un no problema.

...y sí, Remix está abarcando todas las cosas realmente geniales de, los fundamentos de la web, las bases de la web, con el almacenamiento en caché del navegador y el historial. Y, y luego añaden algunas de las cosas realmente geniales como, , enrutamiento anidado y, , Como archivo único real, componentes donde usted tiene, aquí es cómo obtener mis datos aquí.



Y esto se ejecuta en el servidor. Esto es lo que sucede cuando el usuario publica algún formulario o hace alguna mutación... Esa es mi acción. Y luego aquí está lo que va a renderizar para la interfaz de usuario. Y luego tienen como límites árabes, cosas para su, cada módulo. Usted puede especificar lo que sucede cuando hay un error. , y luego también tiene incluso una interfaz de usuario pendiente, por lo que puede, esto es tan loco, pero, pero pueden, pueden representar su aplicación.



Y si tienes una interfaz de usuario pendiente para un componente en particular, entonces ellos dirán, de acuerdo, voy a renderizar la interfaz de usuario pendiente. Y vamos a llenar eso en el cliente cuando la solicitud termina. Así que si tienes algo que es caro, sólo tienes que poner una interfaz de usuario pendiente allí y ya está. Y esto, esto, esto funciona incluso.

Incluso si ese UI pendiente es como un padre, y luego tiene hijos que no están pendientes. Simplemente, puedes renderizar los hijos que no están pendientes y entonces, ese padre puede tener la parte de su UI. Es increíblemente genial. Y el, sólo la API, y no API para remix es realmente genial.



Así que te dan acceso al documento HTML. Tú eres el que responde a la solicitud. Y así eres el que llama a react para renderizar, para, renderizar a stream si quieres, o renderizar a string. Uh, tú eres el que llama a react a hydrate. Y así, porque usted es responsable de todas estas cosas, usted tiene, una enorme cantidad de control con cero API, re remix.



No necesita, para darle una API especial para anular el documento o, o nada. Y porque está anidado, , , Un enrutador anidado. No tienes que preocuparte de renderizar tu componente de diseño para cada página, lo que haces con, con Gatsby y siguiente, , que es un punto de frustración para la gente que ha experimentado esto.



Y, sí, hay un montón de cosas realmente interesantes sobre la remezcla, pero fundamentalmente para mí, se trata de darme un mecanismo realmente agradable para usar las cosas geniales de los fundamentos de la web con los avances realmente impresionantes que hemos tenido en las innovaciones en la parte frontal de JavaScript, también.



Matias: [00:54:18]
Tengo la sensación de que se apropian realmente de esa frase de "usar la plataforma". " Sí. Creo que eso está llegando, pero esto es realmente real. Todos están ahí. El ATD, porque el video que Ryan grabó en YouTube, es realmente impresionante. Sí. Lo comparo con Belkin porque este es el producto final que puede entregar una aplicación sin ningún tipo de JavaScript, porque simplemente no se requiere como creo que es bastante sorprendente.



Kent: [00:54:49] 
Bueno, con el remix, porque eres responsable de renderizar el elemento HTML. Así que el elemento raíz, , es muy trivial para, , no renderizar las etiquetas de script. Uh, y así puedes, , hacer toda tu aplicación y, debido a la forma en que hacen las mutaciones. ...toda tu aplicación puede funcionar sin... sin JavaScript.



Y, y lo que es realmente genial sobre esto es, , usted puede construir su, su aplicación para trabajar muy bien. El lado del cliente. Muestra mensajes de error y cosas, , para todas las mutaciones y lo que sea. Y luego, si por alguna razón, el JavaScript no se carga. Esto nos ha pasado a todos cuando el JavaScript no se carga por alguna razón, , con remix debido a la forma en que estructuran sus APIs.



y, y la forma que es la forma idiomática de hacer esto, su aplicación funcionará exactamente igual. Uh, incluso si no hay JavaScript en la página. Así que la gente será capaz de enviar sus formularios. Pueden obtener una actualización completa de la página, , ya sabes, porque es un formulario que se está publicando, , pero los mensajes de error todavía volverán a renderizar y todo.



Uh, y uh, como si, si hay un error en el formulario, todo será, seguirá funcionando. Y así. Uh, sí. Si usted tiene un caso de uso donde usted es como, Ooh, realmente no quiero tener, cualquier JavaScript en la página de inicio de sesión porque quiero que la página de inicio de sesión para cargar como un rayo entonces, , es trivial para, para añadir que no hay API para ello.




Matias: [00:56:22]
Es obvio por la forma en que está construido. Me parece, dos cosas, me parece que reinventan la idea de framework porque actualmente los frameworks de JavaScript son cosas que envías con tu obligación. Y esto es algo que es sólo la delegación de chips, no el marco en sí.



Uh, y la otra cosa es como remix, , un poco como una herramienta, mecanismo, derrame, kit, y otros son una especie de abrir la puerta a lo que puede ser llamado la tercera era de JavaScript. Como que estamos pasando de los frameworks de cliente a algo más. Es increíble. 



Kent: [00:56:56]
Sí. Y esto, y viene con construcciones que toman 50 milisegundos.



Bueno, sí, es bastante grande. Soy un gran fan de eso. 



Matias: [00:57:08] 
Ok. Entonces estamos, casi al final de esta increíble conversación sobre Ken. Gracias por venir. Uh no. No estoy seguro. ¿Quieres obviamente mirar algo y recomendar algo a la audiencia?

 

Kent: [00:57:22]
Ooh, , sí, así que yo, no sé, como, una recomendación sólo en general.



...creo que puedes ser realmente, realmente impresionante. Un desarrollador sólido y realmente bueno en la codificación y esas cosas. pero no importa lo bueno que seas en la codificación, si no eres agradable, no encontrarás satisfacción en la vida. Siempre estarás persiguiendo algo que te haga feliz. Y creo que encontrar la felicidad en la vida tiene mucho que ver con la cantidad de felicidad que trabajas para traer a la vida de otras personas.



Y, , y la amabilidad tiene mucho que ver con eso. Así que, sí, supongo que si hay algo que recomendaría a la audiencia es, , evaluar lo amable que eres, , o lo amable que fuiste en tu última interacción y trabajar para mejorar eso cada día. 



Matias: [00:58:16]
Me encanta porque somos humanos y no somos sólo una colección de habilidades técnicas.



Somos humanos y trabajamos con otros humanos. Así que ser amable, ser feliz es parte de nuestro objetivo de alguna manera.



Kent: [00:58:29]
No sé qué haces si no quieres ser feliz. 



Matias: [00:58:33]
Sí. Sí. , obviamente como un enchufe, lo haré, eh, epic reactor dev ir a material react en la web. Así que todas estas cosas que Ray puede mencionar a través de su charla estarán en las notas del programa como siempre, y, espero que las transcripciones también.



Así que gracias por estar aquí. Uh, puede de nuevo, no estoy seguro. Oh, una última pregunta. ¿Quién más debería venir a este programa? 



Kent: [00:59:03] 
Ooh, esa es una buena. Yo, tengo un número de, de personas en mi comunidad de discordia que son simplemente increíbles. que podría mencionar a usted y tal vez yo, yo te tiro un correo electrónico o algo así, pero,, yo.



Cualquiera que haya estado en uno de mis podcasts, sería increíble. Así que vayan a ver Kent C dodds.com/podcast. Tenemos tres temporadas, la cuarta temporada viene pronto. Y sí, como la gente que quiero escuchar en un podcast son, son los que invito a la mía. Así que también hay una reacción épica, una especie de podcast en ella también.



Así que usted puede ir a echar un vistazo a, a la gente que tenía en, en eso. Y todos ellos son como reaccionar centrado, obviamente. Así que sí, es la épica reaccionar a las entrevistas de expertos. ...y todos son personas fantásticas. Me encantaría verte en este podcast.



Matias: [00:59:53]
Un contenido realmente impresionante allí también. Así que sí. Gracias, Kent. Esto fue impresionante.



Kent: [00:59:58] 
Gracias. Ha sido un placer 


Matias: [01:00:01]
y nos escuchamos, en la próxima semana.
