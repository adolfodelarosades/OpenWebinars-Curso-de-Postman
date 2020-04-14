# 2. Introducción al testing 54m

* ¿Qué es el testing y por qué es necesario? (Parte I) 10:04 
* ¿Qué es el testing y por qué es necesario? (Parte II) 13:24 
* Niveles de pruebas 6:31 
* Tipos de pruebas 5:51 
* Técnicas de caja negra o basadas en especificación 18:33 
* Contenido adicional 5

## ¿Qué es el testing y por qué es necesario? (Parte I) 10:04 

[¿Qué es el testing y por qué es necesario? (Parte I)](pdfs/Qué_es_el_testing_y_por_qué_es_necesario_Parte_I.pdf)

### Definiciones

* **Defect (defecto)**: Imperfección en un componente o sistema que puede causar que el componente o sistema falle en desempeñar las funciones requeridas, por ejemplo una sentencia o una definición de datos incorrectas. Si se localiza un defecto durante una ejecución puede causar un fallo en el componente o sistema.

* **Bug**: Sinónimo de defecto.

* **Fault (falta)**: Sinónimo de defecto.

* **Error**: Acción humana que produce un resultado incorrecto.

* **Mistake (equivocación)**: Sinónimo de error.

* **Failure (fallo)**: Desviación del componente o del sistema respecto de prestación, servicio o resultado esperado.

*Una persona puede cometer un error (equivocación), que puede llevar a la introducción de un defecto (falta o bug) en el código software o un documento. Si se ejecuta un fragmento de código que contiene un defecto, se podría causar un fallo en el sistema. Los defectos en software, sistemas o documentos pueden ocasionar fallos, pero no necesariamente en todas las circunstancias.*

Los defectos tienen lugar porque las personas pueden cometer errores debido a diversas motivos, como requisitos de tiempo muy ajustados, código complejo, complejidad de la infraestructura, cambios de tecnologías, etc.

* **Testing**: Proceso que consiste en todas las actividades del ciclo de vida de desarrollo software, tanto estáticas como dinámicas, concernientes con la planificación, preparación y evaluación de productos software y los productos de trabajo relacionados para determinar que estos satisfacen los requisitos especificados, demostrar que se ajustan al propósito y detectar defectos.

* **Debugging (depuración)**: Proceso de encontrar, analizar y eliminar las causas de fallos en software.

* **Quality (calidad)**: Grado al cual un componente, sistema o proceso se ajusta a los requisitos especificados y/o necesidades y expectaciones del usuario o cliente.

## ¿Qué es el testing y por qué es necesario? (Parte II) 13:24 

[¿Qué es el testing y por qué es necesario? (Parte II)](pdfs/Qué_es_el_testing_y_por_qué_es_necesario_Parte_II.pdf)

### Los 7 principios del Testing

* **Principio 1**: El Testing muestra la presencia de defectos: El Testing puede mostrar que la evidencia de defectos, pero no puede demostrar que estos no existan. El Testing reduce la probabilidad de defectos sin descubrir en el software pero, incluso si no se encuentran defectos, no se puede demostrar que el software esté libre de ellos.

* **Principio 2**: Es imposible probarlo todo: Es imposible probar todas las combinaciones de entradas y precondiciones salvo para casos triviales. En lugar de probarlo todo, se deberían establecer niveles de prioridad y análisis de riesgos para concentrar los esfuerzos en las pruebas.

* **Principio 3**: Testing temprano: Para encontrar defectos pronto, las actividades de Testing deberían empezar lo antes posible en el ciclo de vida de desarrollo software, y deberían estar concentradas en objetivos definidos.

* **Principio 4**: Agrupamiento de defectos: Los esfuerzos invertidos en las pruebas deben concentrarse proporcionalmente a la densidad de defectos de los módulos esperada (y posteriormente observada). La mayoría de los defectos y fallos operacionales se suelen concentrar en un número bajo de módulos.

* **Principio 5**: La paradoja del pesticida: Si se repiten las mismas pruebas una y otra vez, llegará el momento en el que el mismo conjunto de pruebas no encontrarán ningún defecto nuevo. Para solucionar esta paradoja del pesticida, las pruebas se tienen que revisar regularmente, y se tienen que añadir nuevas pruebas para cubrir las diferentes partes del software o sistema con el objetivo de encontrar más defectos.

* **Principio 6**: Las pruebas dependen del contexto: La forma de probar un sistema es diferente según el contexto de ese sistema. Por ejemplo, un software donde la seguridad es primordial (como un banco) se prueba de forma diferente a una tienda online.

* **Principio 7**: La falacia de la ausencia de errores: Encontrar y corregir defectos no sirve de mucho si el sistema no es usable y no cumple las necesidades y expectaciones de los usuarios.


### PROCESO FUNDAMENTAL DEL TESTING

* Planificación y Control
* Análisis y Diseño
* Implementación y Ejecución
* Evaluación de los criterios de salida y Reporte
* Actividades de cierre de las pruebas

### GRADOS DE INDEPENDENCIA DE LAS PRUEBAS

1. Autor del código sometido a la prueba
2. Otra persona del mismo equipo que el autor del código
3. Una persona de un equipo distinto en la misma organización
4. Una persona de una organización diferente

## Niveles de pruebas 6:31 

[Niveles de pruebas](pdfs/Niveles_de_pruebas.pdf)

### Pruebas de componente(unitarias)

Las pruebas de componente buscan defectos y verifican la funcionalidad de módulos software, programas, objetos, clases... Para esto, se debe aislar el software bajo prueba del resto del sistema.

Normalmente, las pruebas de componente requieren acceso al código bajo prueba y un entorno de desarrollo, como un framework de pruebas unitarias o una herramienta de depuración. En la práctica, involucran al programador que escribió el código.

### Pruebas de integración

Las pruebas de integración verifican las interfaces entre componentes, interacciones con diferentes partes del sistema e interfaces entre sistemas, puede haber más de un nivel de pruebas de integración:

* **Pruebas de integración de componentes**: Ponen a prueba las interacciones entre componentes software y se realizan después de las pruebas de componente.

* **Pruebas de integración de sistemas**: Verifican las interacciones entre diferentes sistemas o entre hardware y software, y se realizan después de las pruebas de sistema.

### Pruebas de sistema

Las pruebas de sistema verifican el comportamiento de un sistema o producto completo. En este tipo de pruebas, el entorno de pruebas debería de parecerse lo máximo posible al entorno de producción con el objetivo de minimizar el riesgo de fallos no encontrados relativos al entorno no encontrados durante la fase de pruebas.

Este nivel puede albergar tanto pruebas funcionales como no funcionales y suele llevarse a cabo a través de un equipo de testers independiente.

### Pruebas de aceptación

Es el siguiente nivel a las pruebas de sistema. Ambos niveles están orientados a requisitos y procesos de negocio, pero el principal objetivo en las pruebas de aceptación no es encontrar defectos, sino generar confianza en el sistema o parte de éste. Estas pruebas sirven para evaluar si el sistema está listo para su uso.

A diferencia de las pruebas de sistema, este tipo de pruebas suele ser responsabilidad de los clientes o usuarios de un sistema, aunque también podrían entrar en juego otras partes relacionadas (stakeholders).

Existen 4 tipos:

* Pruebas de aceptación de usuario
* Pruebas operacionales
* Pruebas de regulación y contrato
* Alpha and beta testing

## Tipos de pruebas 5:51 

[Tipos de pruebas](pdfs/Tipos_de_pruebas.pdf)

### Pruebas funcionales

Las pruebas funcionales verifican las funcionalidades que implementa el sistema, que pueden estar definidas como requisitos, casos de uso, especificaciones funcionales o incluso indocumentadas. Estas pruebas consideran el **comportamiento externo** del software (caja negra) y se pueden realizar en todos los niveles de pruebas.

### Pruebas no funcionales

Las pruebas no funcionales describen las pruebas requeridas para medir características de sistemas y software que se puedan cuantificar, como tiempos de respuesta en caso de probar el rendimiento de un sistema. Estas pruebas también consideran el **comportamiento externo** del software y se pueden realizar en todos los niveles.

### Pruebas estructurales

Verifican la estructura de un software o sistema (caja blanca) y se pueden realizar en todos los niveles de pruebas. Se suelen aplicar después de las técnicas basadas en especificación con el objetivo de ayudar a medir el grado de confianza en las pruebas, determinando la cobertura de pruebas sobre un tipo de estructura.

### Pruebas relacionadas con cambios

* **Retesting**: Pruebas para determinar si un defecto ha sido eliminado.

* **Pruebas de regresión**: Pruebas para determinar si han surgido fallos inesperados como consecuencia de un cambio en el código del programa. Son las principales candidatas para la automatización de pruebas.

 
## Técnicas de caja negra o basadas en especificación 18:33 

[Técnicas de caja negra o basadas en especificación](pdfs/Ténicas_de_caja_negra_o_basadas_en_especificación.pdf)

## Contenido adicional 5

 [¿Qué es el testing y por qué es necesario? (Parte I)](pdfs/Qué_es_el_testing_y_por_qué_es_necesario_Parte_I.pdf)
 
 [¿Qué es el testing y por qué es necesario? (Parte II)](pdfs/Qué_es_el_testing_y_por_qué_es_necesario_Parte_II.pdf)
 
 [Niveles de pruebas](pdfs/Niveles_de_pruebas.pdf)
 
 [Tipos de pruebas](pdfs/Tipos_de_pruebas.pdf)

 [Técnicas de caja negra o basadas en especificación](pdfs/Ténicas_de_caja_negra_o_basadas_en_especificación.pdf)
