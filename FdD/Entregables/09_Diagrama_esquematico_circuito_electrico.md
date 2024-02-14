![image](https://github.com/Fx2048/Team_4_FdD/assets/131219987/84851120-fdf1-4d56-8913-b782fd5ffb4d)



![image](https://github.com/Fx2048/Team_4_FdD/assets/131219987/1c361b20-874d-4d26-b355-46d7d8639e7b)


![FLUJO TITLE](https://github.com/Fx2048/Team_4_FdD/assets/131219987/28a1f97a-6aa1-4b39-88c2-abf4804b01e7)

A continuación mostraremos el diagrama de flujo donde se encuentran al margen los comentarios respecto a las instancias de nuestro procedimiento.

![image](https://github.com/Fx2048/Team_4_FdD/assets/131219987/49598391-a8be-4c26-bd8c-4c455c975427)

[IMAGEN DE FLUJO CENTEAL]

![image](https://github.com/Fx2048/Team_4_FdD/assets/131219987/88aff30e-a657-4409-82dc-dff470d58abf)


[IMAGEN DE FLUJO SENSORES]


![TITLE CIRCUITS](https://github.com/Fx2048/Team_4_FdD/assets/131219987/0abbabdd-5bd8-49eb-81ed-425ae01978a9)


![circuito jejejej](https://github.com/Fx2048/Team_4_FdD/assets/131219987/278d9fd8-791d-43cd-9468-8b019ef8aed4)



![TITLE DESARROLLO PROTO](https://github.com/Fx2048/Team_4_FdD/assets/131219987/459513f2-7fa7-4c5d-8a46-573f9f69b0ac)

![image](https://github.com/Fx2048/Team_4_FdD/assets/131219987/aaa709fb-c21b-4a52-80b2-8c0727f74af4)


[LINK APK ANDROID](https://github.com/Fx2048/Team_4_FdD/blob/main/Software/ECOPUREHARVEST.apk)

[TABLA DE NIVEL DE PH VS TIEMPO EN APK](https://thingspeak.com/channels/2428834/charts/1?bgcolor=%23ffffff&color=%23d62020&dynamic=true&results=60&type=line&update=15)


![protoinal_title](https://github.com/Fx2048/Team_4_FdD/assets/131219987/7f8a8efe-7a2e-4f45-b25e-39c1977b3dca)




![procedimintro](https://github.com/Fx2048/Team_4_FdD/assets/131219987/b426f154-8f37-49f0-ac67-07f515cd8d49)


![PROCESO TAPAS](https://github.com/Fx2048/Team_4_FdD/assets/131219987/6f703fce-f67f-4012-a93c-5d50dcb699f9)


![image](https://github.com/Fx2048/Team_4_FdD/assets/131219987/e6390524-de7d-4a2c-8443-5c9539669b6b)


![PROGRAMACIÓN 1](https://github.com/Fx2048/Team_4_FdD/assets/131219987/c4ac2470-d4c7-4191-a7da-9014664b7512)


    #include <SPI.h>      // Para la conexión de dispositivos
    #include <nRF24L01.h> // Para dar uso soporte al módulo transceptor 
    #include <RF24.h>     // Para la interacción con el módulo de radio NRF24L01
    #include "MHZ19.h"

    RF24 myRF24(7, 8);    // Se declara el objeto y los pines para la 
                        // comunicación SPI con el módulo NRF24L01
    byte address[6] = "00001"; // Dirección de transmisión


    // Configuración de objetos

    const int PO = A0; 
    float buf[15];
    float val; 
    float pH;

    // CONFIGURACIÓN
    void setup() {
    Serial.begin(9600);
  
    myRF24.begin();
    myRF24.openWritingPipe(address);
    myRF24.setPALevel(RF24_PA_MIN);
    myRF24.stopListening();   // Permite la trasmición de datos

    // Configuración del pin analógico para el sensor de pH
    pinMode(PO, INPUT);  
    }

    // BUCLE
    void loop() {
    val = 0;
    for(int i = 0; i < 15; i++) {    // Realizamos 10 lecturas y almacenamos en buf
    // Leemos el valor de pH
    buf[i] = analogRead(PO);       // Convertir la lectura en un valor de pH
    delay(15);
    val += buf[i];
    }

    val /= 15;

    float val_1 = (val/1023)*5;
    float pH = (val_1/5)*14 - 3.37;

    // Leemos el valor de CO2
    float CO2 = 123.45;
  
    // Enviamos el valor de pH  y CO2 a través de nRF24L01
    myRF24.write(&pH, sizeof(pH));
    myRF24.write(&CO2, sizeof(CO2));

    // Mostramos el valor de pH en el monitor serie
    Serial.print("pH: ");
    Serial.println(pH, 2);
    // Mostramos el valor de CO2 en el monitor serie
    //Serial.print("CO2: ");
    //Serial.println(CO2, 2);

    delay(1000);
    }

![CO2 TTUTLE PORGRAMACIÓN 2](https://github.com/Fx2048/Team_4_FdD/assets/131219987/f765d8a6-421a-48bd-a082-430920285b29)

    // INCLUIMOS LAS LIBRERÍAS
    #include <MHZ19.h>          // Sensor CO2                                     
    #include <SoftwareSerial.h> // la libreria controla el puerto serial entre el módulo de co2 y el ordenador 
    #include <SPI.h>            // Para la conexión de dispositivos
    #include <nRF24L01.h>       // Para dar uso soporte al módulo transceptor 
    #include <RF24.h>           // Para la interacción con el módulo de radio NRF24L01

    //DEFINIMOS LOS PINES
    #define RX_PIN 4            //Pines del sensor CO2                                        
    #define TX_PIN 2            // Pines del sensor CO2                                        
    #define BAUDRATE 9600       //Frecuencia a la que se va a abrir el puerto serial                                    
 
    const int PO = A0; 
    float buf[15];
    float val; 
    float pH;
  
    MHZ19 myMHZ19;              //Definimos el nombre del sensor de co2                                           
    SoftwareSerial mySerial(RX_PIN, TX_PIN); //El puerto serial que va a permitir la comunicacion entre 
    //el ordenador el sensor de CO2 estará fijando en los pines RX_PIN, TX_PIN

    RF24 myRF24(7, 8);         // Se declara el objeto y los pines para la 
                           // comunicación SPI con el módulo NRF24L01
    byte address[6] = "00001"; // Dirección de transmisión

    // CONFIGURACIÓN
    void setup() {

    Serial.begin(9600); 
    mySerial.begin(BAUDRATE);     // empieza el serial  de comunicación                             
    myMHZ19.begin(mySerial);      //inicia el sensor de CO2                           

    myMHZ19.autoCalibration();    //Autocalibración del sensor                             

    myRF24.begin();
    myRF24.openWritingPipe(address);
    myRF24.setPALevel(RF24_PA_MIN);
    myRF24.stopListening();       // Permite la trasmición de datos

    // Configuración del pin analógico para el sensor de pH
    pinMode(PO, INPUT); 
    }

    // BUCLE
    void loop() { 
    val = 0;
    for(int i = 0; i < 15; i++) {    // Realizamos 10 lecturas y almacenamos en buf
    // Leemos el valor de pH
    buf[i] = analogRead(PO);       // Convertir la lectura en un valor de pH
    delay(15);
    val += buf[i];
    }

    val /= 15;

    float val_1 = (val/1023)*5;
    float pH = (val_1/5)*14 - 3.37;

    // Mostramos el valor de pH en el monitor serie
    Serial.print("pH: ");
    Serial.println(pH, 2);
  
    // Leemos el valor de CO2
    static int CO2 = 0; //variable CO2=0
    CO2 = myMHZ19.getCO2();   //Para obtener los datos de CO2
    // Mostramos el valor de CO2 en el monitor serie
    Serial.print("CO2 (ppm): "); // Puerto serial del ordenador , para que aparezca el texto
    Serial.println(CO2); // Aparecen las mediciones de CO2 en el puerto serial

    // Enviamos el valor de pH  y CO2 a través de nRF24L01
    myRF24.write(&pH, sizeof(pH));
    myRF24.write(&CO2, sizeof(CO2));

    delay(1000); //Espera un 1 segundo
    }
