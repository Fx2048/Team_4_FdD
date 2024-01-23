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


# Práctica 1: Manejo de protoboard

## *Ejercicio 1:*

### Explicación: 
  - En el presente circuito, trabajamos resistencias de 220 ohm de las cuales se encontraban en serie y paralelo, respectivamente:

  **Calculando en serie:**

   Rs= 220 ohm + 220 ohm = 440 ohm
    
   conciderando dicho resultado (Rs), procedemos a calcular en paralelo.
    
   **Calculando en paralelo:**
    
   1/Rt = 1/Rs + 1/220 ohm
    
   1/Rt = 1/440 ohm + 1/220 ohm
    
   Rt = (440 ohm)(220 ohm)/440 ohm+220 ohm
    
   Rt = 146.6 ohm

  - Por lo cual de este caso concluimos que la resistencia total nos dió 146.6 ohm.


<table style="width: 100%;">
    <tr>
        <td style="border: 0px solid #ddd; padding: 4px; text-align: center;">
            <img src="https://github.com/Fx2048/Team_4_FdD/blob/main/Im%C3%A1genes/Taller_03/Img_1.png" alt="" style="width: 100%; max-width: 100px; display: block; margin: auto;">
        </td>
        <td style="border: 0px solid #ddd; padding: 4px; text-align: center;">
            <img src="https://github.com/Fx2048/Team_4_FdD/blob/main/Im%C3%A1genes/Taller_03/Img_1.2.jpg" alt="" style="width: 70%; max-width: 50px; display: block; margin: auto;">
        </td>
    </tr>
</table>


  

## *Ejercicio 2:*


En el experimento aplicativo, se elaboró un esquema en paralelo  a los extremos y al centro en forma de serie, para colocar las resistencias



<img src="https://github.com/Fx2048/Team_4_FdD/assets/131219987/1276cc8b-9d7a-4eb3-8dc4-0769e31030c2" alt="Imagen_General_experimento_2" width="300" height="200" align="center" border="1">

 



Lo cual al calcularse el valor resultante se obtuvo 87.9 ohmios,

<img src="https://github.com/Fx2048/Team_4_FdD/assets/131219987/74fe31b3-b65d-402f-9dcc-4b5680c4591a" alt="88_ohm_experimento_2" width="300" height="200" align="center" border="1">


Luego, al momento de analizar la estructura faltante la cual era proveniente de la resistencia de 220 ohmios, dado que  se conectaba  a un mismo nodo que las resistencias en paralelo de los extremos de 220 ohmios , se comprobó que producía un cortocircuito al medir su voltaje y resultaba 0 ohmios


<img src="https://github.com/Fx2048/Team_4_FdD/assets/131219987/3195662c-925f-4197-825a-119dd6953b1a" alt="0_ohm_experimento_2" width="300" height="200" align="center" border="1">

 Por lo que nos mantuvimos con la respuesta inicial preevaluada.

<img src="https://github.com/Fx2048/Team_4_FdD/assets/131219987/a0d8b736-984f-473d-a762-5ee81156a3f2" alt="88_ohm_experimento_2" width="300" height="200" align="center" border="1">


 

## Ejercico 3:

Para el desarrollo de este ejercicio identificamos las ubicaciones de las resistencias(serie o paralelo).
Resistencias: R1(220 ohm), R2(220 ohm), R3(220 ohm), R4(1000 ohm), R5(220 ohm), R6(220 ohm).

Serie_1: R1, R3

Serie_2: R5, R6

Serie_3: R2, R4

Paralelo: serie_1, Serie_2, Serie_3

Calculando y remplazando con los valores de las resistencias respectivamente y aplicando la fórmula de la resistencia como también del paralelo, el resultado final fue 186.39 ohm, en la imagen podemos ver la respuesta comparada con el resultado del multímetro que fue 186.0 ohm.

<table style="width: 100%;">
    <tr>
        <td style="border: 0px solid #ddd; padding: 4px; text-align: center;">
            <img src="https://github.com/Fx2048/Team_4_FdD/blob/da6e65f5dd195d752efc92a2db35e866a13971aa/Im%C3%A1genes/Taller_03/ejercicio3.png" alt="" style="width: 100%; max-width: 100px; display: block; margin: auto;">
        </td>
        <td style="border: 0px solid #ddd; padding: 4px; text-align: center;">
            <img src="https://github.com/Fx2048/Team_4_FdD/blob/f336c85fe123c5ead3596861d5a282d3fe95fd08/Im%C3%A1genes/Taller_03/ejerc_im3.jpeg" alt="" style="width: 70%; max-width: 50px; display: block; margin: auto;">
        </td>
    </tr>
</table>



## Tema 1.1: Circuitos útiles

## *Ejercicio 4:*

En este ejercicio se presenta la implementación de resistencias para lograr una salida de 1.1V (OUTPUT) partiendo de una entrada de 5V (INPUT). A continuación, se dará a conocer el procedimiento teórico para encontrar dicho diferencial de potencial de 1.1 V:
 
Antes de comenzar, cabe resaltar que, para encontrar una relación entre las resistencias, se utilizó el "Circuito Divisor de Tensión", el cual es una aplicación de la Ley de ohm que nos permite encontrar el voltaje de salida reducido de una resistencia y se basa en la siguiente fórmula:

<p align="center">
  <img src="../../../Imágenes/Imagen_formula.png">
</p>

El desarrollo se basa en lo siguiente: 

- Despejando la relación entre las resistencias para el correspondiente estimado. 

<p align="center">
  <img src="../../..//Imágenes/Imagen_desarrollo.jpg"
  width="400" height="180">
</p>

- Asignando el valor de 1k ohm a la resistencia 2 (R2) para encontrar la resistencia 1 (R1). 

 ........ aqui aqui
