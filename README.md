# Arduino
Sri Cyberpunk Arduino Tutorials


void setup() {
 
 pinMode(10,INPUT);//right sensor
 pinMode(11,INPUT);//left  sensor
 
 pinMode(2,OUTPUT);
 pinMode(3,OUTPUT);
 pinMode(4,OUTPUT);
 pinMode(5,OUTPUT);
}

void loop() {
 
  if(digitalRead(10)==1 && digitalRead(11)==0){
     digitalWrite(4,LOW);
     digitalWrite(5,HIGH);
     digitalWrite(3,HIGH);
     digitalWrite(2,LOW);
    }else if(digitalRead(10)==0 && digitalRead(11)==1){
     digitalWrite(4,HIGH);
     digitalWrite(5,LOW);
     digitalWrite(3,LOW);
     digitalWrite(2,HIGH);
    }else if(digitalRead(10)==1 && digitalRead(11)==1){
     digitalWrite(4,HIGH);
     digitalWrite(5,LOW);
     digitalWrite(3,HIGH);
     digitalWrite(2,LOW);
    }else{
      digitalWrite(4,LOW);
     digitalWrite(5,LOW);
     digitalWrite(3,LOW);
     digitalWrite(2,LOW);
      }
   
}
