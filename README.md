# Simple_store

Para inicializar la clase, se necesita 1 matriz y 2 fechas que se correspondan con los datos de la matriz.

La matriz debe ser de 4 columnas y n filas, donde n corresponde al numero total de incidentes registrados.
1° columna: Contiene la descripcion del incidente (irrelevante para el ejercicio)
2° columna: Se encuentran los "status" de cada incidente, es decir, "open" o "solved"
3° columna: Contiene el tiempo (en horas) que se requirió para los casos "solved" y el tiempo que ha transcurrido desde el incidente para los casos "open"
4° columna: La fecha del incidente solo considerando el dia del mes

Ejemplo visual:
-----------------------------------------------------------------------
Incident description        Status         Tiempo(hrs)          Fecha(día)
-----------------------------------------------------------------------
"incident description"     'solved'           25                  2                  
"incident description"      'open'            10                  5
"incident description"     'solved'            3                  18
       ...                    ...             ...                 ...

Para la matriz de prueba n=10, y se utilizan casos para el mes de Abril 2022, donde las fechas van desde el 1 al 7.

Luego, para inicializar la clase:

Simple_store.incident_status(Matriz, primera fecha, segunda fecha)

el resultado en pantalla muestra una nueva matriz (Shop_status) solo con los datos entre las fechas propuestas y los resultados solicitados.

--------------------------------------------------------------------------------------------------------------------------------------------
Datos adicionales:
*Para el caso de los incidentes con status "open", el tiempo que se utiliza en la matriz original corresponde a la hora en que se produce el incidente, por lo que el 
tiempo final(current time) se calcula segun el tiempo transcurrido segun la fecha del computador: 

Ej: Si se realiza el test el día 7, a las 18:00:
-----------------------------------------------------------------------
Incident description        Status         Tiempo(hrs)          Fecha(día)
-----------------------------------------------------------------------
"incident description"      'open'            10                  5

current time = ((hora actual)+(24*(fecha actual - fecha))) - tiempo inicial
current time = ((18)+(24*(7-5))) - 10
current time = 56
