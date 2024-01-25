<p align = "center"> “Año del Bicentenario, de la consolidación de nuestra Independencia, y de la conmemoración de las heroicas batallas de Junín y Ayacucho” </p> 

  

# <p align = "center"> UNIVERSIDAD PERUANA CAYETANO HEREDIA </p> 

  

### <p align = "center"> Facultad de Ciencias y Filosofía “Alberto Cazorla Talleri” </p> 

  

<p align="center"> 

  <img src="https://github.com/Fx2048/Team_4_FdD/blob/main/Im%C3%A1genes/Logo_upch.jpeg" width="250" height="150" style="margin: auto;"> 

</p> 

  

  

### <p align = "center"> FUNDAMENTOS DE DISEÑO </p> 

  

  

### Docentes:👨‍🏫 

  

  - Mg Umbert Lewis De La Cruz   

  - Mg. Paulo Camilo Vela Antón  

  - Mg. Moises Stevend Meza Rodriguez  

  - Dr. Harry Anderson Rivera Tito  

  - Ing. Juan Manuel Zuñiga Mamani   

  - Ing. Renzo José Chan Ríos 

  

  

### Integrantes:   👩‍🎓🧑‍🎓                                                                            

  

  - Bernal Belisario, Brigitte 

  - Llanos Angeles Leily Marlith 

  - Luque Mamani, Magno Ricardo 

  - Quispe Baldeon, Melissa 

  - Turpo Huaman, Nilda Maribel (Coordinadora general) 

  

  

<p align="center"> 

  Lima-2024 

</p> 

  

<p >------------------------------------------------------------------------------------------------------------------------------------------------------------- 

</p> 

  

  

##   Introducción: 

<p align="justify"> 

En la actualidad, la medición de factores climatológicos ha sido más accesible gracias a recursos como el internet de las cosas, es por ello; que mediante una adaptación experimental básica y simplificada, se ha procedido a recrear cómo registrar la temperatura y la humedad localmente leyendo el sensor HTS221 con el que viene equipado el MKR IoT Carrier usando un kit de IoT lúdico y educativo. Para ello, nuestros tres objetivos planteados son los siguientes:  

</p> 

 

<p align="justify"> 

Visualizar los valores de humedad (en valores positivos) y temperatura (En Celsius) en la plataforma de Arduino y en la pantalla del Arduino MK 1010. </p> 

 

<p align="justify"> 

 Visualizar en la pantalla del arduino IDE, y de la pantalla del MKR IoT Carrier los valores de temperatura, acorde a los toques sobre la superficie indicada del MKR IoT Carrier, alternando entre celsius, farenheit y kelvin. </p> 

 

<p align="justify"> 

Detectar mediante el MKR IoT Carrier a través de colores el nivel de temperatura y humedad. </p> 

 

<p align="justify">  

Con todo lo anterior expuesto, esperamos presentar la correcta realización de los tres objetivos planteados, y posterior a ello, el análisis de cada uno y la conclusión general como condensación de nuestros conocimientos adquirido en práctica. </p> 

 

<p align="center"> 
  <img src="https://github.com/Fx2048/Team_4_FdD/assets/131219987/c0077439-a26c-407f-9186-0fe03975fbe3" width="350" height="900" style="margin: auto;"> 
</p>


## Procedimiento: 

<p align="justify"> 

Esta actividad empezamos unir las partes del sensor y de esa manera implementar el código, por lo cual seguimos los siguientes pasos: 

</p> 

 

<p align="justify"> 

Primero necesitamos montar la placa Arduino MKR WiFi 1010 sobre la MKR IoT Carrier y todo esto ponerlo dentro de un pote circular implementado para este tipo y conectarlo a nuestro ordenador a través de un cable USB para que funcione y a la vez transmitir el código implementado, por otra parte, una vez transferido el código, si queremos que funcione sin estar conectado a la laptop se le conecta a una batería a través de dos cables pequeños. 

</p> 

 

 

 

 

## *Ejercicio 1:* 

  

### Explicación:  

<p align="justify"> 

Para la ejecución de este primer ejercicio se hará uso del sensor HTS221 que determina la humedad y la temperatura, donde los datos serán mostrados en la pantalla del MKR IoT y para un mejor funcionamiento y visualización serán intercambiados a través del touch. Asimismo, para realizar todo lo anterior, se nos brindó un código, lo cual se visualizan en las siguientes líneas:  

</p> 

 

 

<p align="justify"> 

En este bucle principal del loop(), la primera parte nos permite leer la temperatura y la humedad del sensor, asimismo, mediante el método .update nos facilita actualizar y tener una información contundente sobre los botones táctiles. Después, en el Serial se imprimen los valores actuales de la temperatura y humedad importantes para un buen funcionamiento, además, la parte final verifica si los botones táctiles han sido tocados y así cumplir lo solicitado, como observamos el TOUCH0 nos habilita la opción de cambiar a temperatura y, por otra parte, el TOUCH1 nos posibilita cambiar a humedad, por lo cual, estas funciones nos proporcionan la facilidad de configurar los colores y el tamaño de las letras de la pantalla.  

</p> 

 

Continuando con lo implementado tenemos el siguiente código. 

 

<p align="justify"> 

En este código se puede presenciar las dos funciones: temperatura y humedad, las cuales serán visualizadas con la configuración en la pantalla táctil y a la vez poder distinguir ambos. En el caso de la temperatura tenemos un fondo de color rojo, con el texto de color blanco y un tamaño de 6, y para mostrar la temperatura actual en grados Celsius nos brinda un tamaño de letra 4 y para el caso de humedad tenemos un fondo azul, letras blancas y un tamaño de 2. 

</p> 

 

Y todo lo anterior nos brindó la siguiente salida: 

 

 

 

Insertando imagen...Insertando imagen...Insertando imagen...Insertando imagen... 

<p align="justify"> 

En base a lo anterior, según los datos presentados en la pantalla digital, analizamos que la información relacionada con la temperatura es precisa, ya que proporciona lecturas reales del entorno en grados Celsius. Sin embargo, en cuanto a los datos de humedad, se ha identificado un error, dado que el valor es negativo. Tras analizar y aplicar los conceptos abordados durante la clase, se infiere que este error podría deberse a diversos factores, pero lo más probable es una falta de calibración adecuada en el sensor. 

</p> 

 

## *Ejercicio 2:*  **Visualizar temperaturas: Fahrenheit, Celsius y Kelvin** 

 

###  Explicación: 

 

<p align="justify">  

Para este ejercicio, se pidió mostrar en la pantalla de la MKR IoT Carrier las temperaturas en Fahrenheit, Celsius y Kelvin recopiladas por el sensor HTS221 (sensor de humedad y temperatura). Inicialmente implementamos líneas de código Arduino que permitía mostrar la temperatura solo en Celsius, el cual estaba denotada con una función como se muestra a continuación:  

</p> 

 

 

<p align="justify">  

La característica de la MKR IoT Carrier es que presenta 5 botones táctiles y el objetivo se trata de tocar tres de ellos para que pueda mostrar las respectivas temperaturas, de tal manera que necesitamos implementar tres funciones y dentro de ellas su respectiva escala de medición. Cabe mencionar que la escala de medición de temperatura por defecto del sensor HTS221 es el Celsius, por ende, tomaremos este valor para realizar las conversiones en las funciones de temperatura en Kelvin y Fahrenheit. Antes de ello se debe implementar condicionales cuando se presione el TOUCH 0, TOUCH 1, TOUCH 2 y TOUCH 3. Y esto se muestra a continuación: 

</p> 

 

Insertando imagen... 

<p align="justify">  

Como se podrá notar, se declaró tres funciones de las escalas de temperatura y una de humedad. Pero para este ejercicio se dará detalle de las tres primeras funciones. La estructura de estas tres funciones tomó el valor de la temperatura en Celsius e hizo las conversiones para obtener las otras dos. La declaración de las funciones y sus componentes puede visualizar a continuación: 

</p> 

 

 

 

 

<p align="justify">  

Así se puede visualizar que se añadieron en las dos últimas funciones las variables, tanto de temperatura en Kelvin como en Fahrenheit, que toma una ecuación de conversión que usa el valor de temperatura en Celsius, permitiendo obtener y mostrar lo que se pidió para este ejercicio.  

También se mostrarán a continuación, como evidencia de lo trabajado, las fotos de las temperaturas en la pantalla de la MKR IoT Carrier: 

</p> 

 

 

 

<p align="justify"> 

En este ejercicio es importante resaltar que se implementaron funciones requeridas para mostrar las temperaturas en diferentes escalas en la pantalla MKR IoT  Carrier. Además, las fotos de las temperaturas en la pantalla proporcionan los resultados de los códigos mostrados en dicho ejercicio. 

</p> 

 

 

 

CONCLUSIÓN: 

<p align="justify"> 

 

En síntesis, se desarrollaron los ejercicios propuestos cumpliendo algunas partes de los objetivos planteados, entre otras dificultades. En el objetivo 1, debíamos visualizar los valores de humedad (en valores positivos) y temperatura (En Celsius) en la plataforma de Arduino y en la pantalla del Arduino MK 1010, para lo cual se logró visualizar los datos, las mediciones de temperatura eran correctas, pero los valores de la humedad que obtuvimos fueron negativos. En el 2° objetivo, visualizamos en la pantalla del Arduino IDE, y de la pantalla del MKR IoT Carrier los valores de temperatura, acorde a los toques sobre la superficie indicada del MKR IoT Carrier, alternando entre Celsius, Fahrenheit y kelvin, lo cual se logró satisfactoriamente. En el 3° objetivo detectaríamos mediante el MKR IoT Carrier a través de colores el nivel de temperatura y humedad, pero no lo completamos dado que demoramos en la consecución del primer objetivo el cual afectó negativamente la resolución de los posteriores objetivos trazados. 

</p> 

 

<p align="justify"> 

A pesar de enfrentar estas dificultades mencionadas, el equipo 4 demostró realizar estos ajustes en tiempo real y aprender de las dificultades encontradas, dado que, la importancia de alcanzar los objetivos establecidos es fundamental extraer lecciones y logros para futuras mejoras y desarrollo en la integración de tecnologías IoT para las mediciones de humedad y temperatura en sensores climatológicos. La capacidad de reflexionar sobre los desafíos enfrentados y las lecciones aprendidas no solo resultará en un crecimiento personal, sino que también contribuirá al fortalecimiento y la mejora continua del equipo en proyectos futuros. Estos aprendizajes proporcionan una base valiosa para abordar eficientemente dificultades similares en el futuro, permitiendo un enfoque más efectivo y una mayor eficiencia en el diseño e implementación de soluciones en el ámbito de la monitorización climática mediante tecnologías de IoT. </p> 

 

 

 

 

 

 


