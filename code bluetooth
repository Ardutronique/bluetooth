
#include <SoftwareSerial.h>
#include <Wire.h> 

SoftwareSerial BTSerial(4, 8);  // TXD = 4 , RXD = 8

void setup() {
  
  Serial.begin(9600);           // set up Serial library at 9600 bps
  Serial.println("Entrer une commande:"); // ecrire Entrer une commande
  BTSerial.begin(9600); 
 

}

void loop() {
  
  String message;
    // Boucle de lecture sur le BT
  
    while (BTSerial.available()){
      // Lecture du message envoyé par le BT
        
        message = BTSerial.readString();
      // Ecriture du message dans le serial usb
        Serial.println(message);



        
    }
    // Boucle de lecture sur le serial usb
 
    while (Serial.available()){
      // Lecture du message envoyé par le serial usb
     
      message = Serial.readString();
      // Ecriture du message dans le BT
     
      BTSerial.println(message);
    }



   if(message == "slt\r\n"){
      Serial.println("slt cv!");
    }// else if message off
    if(message == "bien\r\n"){
      Serial.println("cool") ;
    }
}
