# MÓDULO INFERENCIA FILOGENÉTICA

<p align="center">
  <img src="https://scx2.b-cdn.net/gfx/news/hires/2015/treeoflifefo.jpg" width="330" height="300" />
</p>

Figura tomada de: _https://scx2.b-cdn.net/gfx/news/hires/2015/treeoflifefo.jpg_

## Objetivos

1. Aprender las bases metodológicas de los principales métodos de inferencia filogenética a partir de matrices de caracteres homólogos y evaluar críticamente los supuestos, virtudes y desventajas de estos métodos.

2. Conocer los principios estadísticos para medición de la confianza de las hipótesis filogenéticas.  

3. Adquirir destrezas computacionales básicas para llevar a cabo análisis de inferencia filogenética a partir de matrices de caracteres.

## Competencias

1. Habilidad de inferir e interpretar críticamente hipótesis de relaciones filogenéticas en cualquier grupo de organismos generadas bajo distintas metodologías a partir de matrices de caracteres.

2. Capacidad para interpretar fundamentos de la biología evolutiva en un árbol filogenético generado a partir de matrices de caracteres empíricas.

3. Entendimiento de la importancia de la inferencia filogenética para abordar problemas biológicos en un contexto evolutivo.

## Estructura general del módulo

### Preparación

Este módulo ha sido diseñado para estudiantes del curso de pregrado "Sistemática Biológica" del programa de Biología de la Universidad Nacional de Colombia. Los estudiantes inscritos en este curso ya debieron haber tomado clases previas sobre temas introductorios de evolución y sistemática filogenética para poder seguir con los contenidos de este módulo. Este módulo fue diseñado para ser tomado de manera remota dada la emergencia generada por el COVID-19. 

#### Requerimientos y materiales básicos

Aunque este módulo está diseñado para llevarse a cabo mínimamente con acceso a un computador, celular o tablet durante las horas de clase y para acceder a los ejercicios, se recomienda a los estudiantes que puedan y tengan acceso a computadores propios bajar los siguientes programas:

- Editor de texto (recomendados notepad++ para Windows y Atom o BBEdit para Mac).
- [MEGA X](https://www.megasoftware.net/). Útil para muchas tareas asociadas a análisis filogenéticos usando secuencias de ADN.
- [Mesquite](https://www.mesquiteproject.org/). Útil para construir y/o visualizar matrices de caracteres.
- R y R Studio (bajar los paquetes: Ape, Claddis, Phangorn, Phytools).
- [TNT](http://www.lillo.org.ar/phylogeny/tnt/). GUI solo para Windows. Para análisis de Máxima Parsimonia.
- [jmodelTest](https://github.com/ddarriba/jmodeltest2). Para selección de modelos evolutivos de secuencias de nucleótidos.
- [RAxML-GUI](https://antonellilab.github.io/raxmlGUI/). Para análisis de Máxima Verosimilitud.
- [BEAST2](https://www.beast2.org/). Para análisis de Inferencia Bayesiana (y muchas cosas más). 
- [FigTree](https://github.com/rambaut/figtree/releases). Para visualización y edición de árboles filogenéticos.
- [Tracer](https://github.com/beast-dev/tracer/releases/tag/v1.7.1). Para visualizar resultados de MCMC.

**Nota:** Todos los programas de inferencia filogenética vienen acompañados con sus respectivos tutoriales. Se sugiere seguirlos en su tiempo libre si quieren adquirir destrezas más avanzadas; no se limiten únicamente a los ejercicios de la clase.  

### Dinámica de las clases

Para facilitar el trabajo autónomo de los estudiantes desde sus casas y minimizar la presencialidad en las sesiones virtuales, este módulo está principalmente enfocado en talleres y lecturas en casa. Las sesiones virtuales estarán limitadas a clases cortas sobre conceptos fundamentales de los métodos, explicación de las tareas, resolución de dudas y presentación de resultados. Todas las presentaciones con diapositivas, artículos y talleres serán subidos a esta plataforma en su debido momento. 

#### Evaluación

La nota del módulo será dividida de la siguiente manera: talleres y tareas (60%), proyecto del módulo (40%).

## Contenido

#

**Clase 1. Esta clase estará dividida en dos partes:**

**1. Repaso árboles filogenéticos y caracteres.** Durante la primera parte de la clase haremos un breve repaso de conceptos fundamentales sobre la lectura de árboles filogenéticos y la interpretación de la evolución de los caracteres. Esta clase incluye una corta presentación con pequeños quizes anónimos relámpago para evaluar qué tan solidos están los conceptos básicos por parte de los estudiantes. Para interactuar virtualmente en esta presentación, los estudiantes deben entrar al enlace que enviará el profesor al comienzo de la clase. Para que el enlace funcione, los estudiantes deben tener sus cuentas de correo abiertas.

**2. Explicación del proyecto del módulo** (ver las instruciones del proyecto [aquí](/clase_3/proyecto.md)). Las presentaciones y entrega de resumen para este proyecto serán el **Jueves 27 de mayo de 2021**

**Tarea.** Leer para la próxima clase la siguiente guía rápida de generación de matrices morfológicas: [Matrices](/clase_1/Matrices.pdf) y el [Capítulo 4 del libro de Lanteri & Cigliano 2006](/clase_1/Lanteri_Caracteres_taxonomicos.pdf)

#

**[Clase 2](/clase_2/clase_2.pdf). Estructura de un estudio de inferencia filogenética y construcción de matrices.** Esta clase estará dividida en dos partes:

**1. Estructura de un estudio de inferencia filogenética.** Exploración del esqueleto de un estudio de inferencia filogenética con base en la lectura del artículo de [Argnarsson (2004)](/clase_1/Agnarsson_2004.pdf). Para esta actividad haremos la discusión con base en las preguntas del siguiente taller: [Taller 1](/clase_2/Taller_1.md) y una corta charla (bajar la presentación [aquí](/clase_2/clase_2.pdf)). 

<p align="center">
  <img src="https://desinsectador.files.wordpress.com/2013/06/steatoda-nobilis-01.jpg" width="200" height="200" />
</p>

[Fuente de la_imagen](https://desinsectador.files.wordpress.com/2013/06/steatoda-nobilis-01.jpg)

**Tarea:** Subir las respuestas del taller 1 a la carpeta "Taller 1" del [Drive del curso](https://drive.google.com/drive/folders/1SP-YRP3jQhl2p5EDTzSmP5smE9-PBpBB?usp=sharing).

**2. Matrices de caracteres para inferencia filogenética.** En esta parte práctica sentaremos las bases de la construcción de matrices de datos para inferir hipótesis filogenéticas. Hablaremos sobre homología primaria y codificación de matrices y haremos un taller de construcción de matrices morfológicas y de secuencias de ADN. En este último ejercicio aprenderán las bases para descargar datos de [GenBank](https://www.ncbi.nlm.nih.gov/nucleotide/); entender un archivo de extensión "fasta"; generar un alineamiento de secuencias con mafft; y entender los formatos de archivos para inferencia filogenética. La instrucciones detalladas del taller se encuentran [aquí](/clase_3/Taller_4.md).

**Tarea:** Subir las respuestas del taller 2 a la carpeta "Taller 2" del [Drive del curso](https://drive.google.com/drive/folders/1SP-YRP3jQhl2p5EDTzSmP5smE9-PBpBB?usp=sharing).

**_NOTA:_** Para las próximas dos clases se requiere leer alguno de los siguientes artículos:

- Máxima Parsimonia: [Lanteri (2006)](/clase_3/Parsimonia.pdf) **o** [Baum & Smith (2013)](/clase_3/MP_baum_smith2013.pdf)

#

**[Clase 3](/clase_4/Taller_MP.md). Distancias, Inferencia Hennigiana y Máxima Parsimonia (Parte I)** Esta clase hace una breve mención a los métodos que dieron origen a los métodos modernos de inferencia filogenética y abordaremos el concepto del criterio de optimalidad y el método de la Máxima Parsimonia. Descargar diapositivas [aquí](/clase_4/Clase_4.pdf). Para la parte práctica, haremos el siguiente taller con los mismos grupos de trabajo de siempre: 

**[IR AL TALLER](/clase_4/Taller_MP.md)**

<p align="center">
  <img src="https://github.com/jaaguirresant/Sistematica-Filogenetica/blob/master/clase_2/Hennig_book.jpg" width="130" height="200" />
</p>

**NOTA 1:** Para la próxima clase leer el siguiente artículo: 

- [Wiens_2011](/clase_4/Wiens_2011.pdf)

**NOTA 2:** Para quien quiera ir prácticando con el script de R que usaremos en la próxima clase, se puede bajar [aquí](/clase_5/parsimonia.R)

**NOTA 3:** Altamente recomendado que para la próxima clase ya tengan la matriz de datos alineados de sus proyectos lista y en los formatos fasta, tnt (o XREAD), Nexus y Phyllip.

#
