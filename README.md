# Electro3_M-todo-de-relajaci-n

Este código  proporciona una implementación del método de relajación para resolver la ecuación de Laplace en una región rectangular con unas condiciones de frontera particulares conocidas como Condiciones de frontera de Dirichlet y muestra la distribución de potencial resultante. A continuación se presenta una descripción detallada de cómo funciona:

Primero se define la función 'initialize_grid' que inicializa la malla con condiciones de frontera, la cual crea una matriz de tamaño (N, M) donde N es el número de puntos en la dirección x y M es el número de puntos en la dirección y. Luego, se aplican las condiciones de frontera a la matriz V, donde se establece el valor en el borde inferior (y=0) como -v0 y el valor en el borde superior (y=b) como v0. La matriz inicializada se devuelve como salida.

Definimos la función 'relax_potential' que realiza un paso de relajación en la malla del potencial. Esta función toma la matriz de potencial V y calcula una nueva matriz V_new aplicando la regla de relajación en cada punto interior de la malla. El nuevo valor en cada punto se calcula como el promedio de los valores de sus vecinos, después el programa devuelve la matriz actualizada a la que se llamó 'V_new'.

Después se define la función 'solve_laplace' que resuelve la ecuación de Laplace utilizando el método de relajación. Esta función toma como entrada el número de puntos en las direcciones x e y (N y M), el tamaño del paso (dx), el ancho (a) y la altura (b) del dominio rectangular, el valor de la condición de frontera (v0) y una tolerancia (tol) para determinar la convergencia. La función inicializa la malla del potencial, realiza iterativamente pasos de relajación hasta que el cambio en el potencial sea menor que la tolerancia y luego devuelve la matriz convergida del potencial.

Por último se define la función 'main' que actúa como punto de entrada del programa.

*Correr el programa: Una vez se ejecuta el programa el usuario puede proporcionar los parámetros de entrada requeridos para resolver la ecuación de Laplace, como el número de puntos en las direcciones x(N) e y(M), el tamaño del paso, el ancho y la altura del dominio y el valor de la condición de frontera. 
