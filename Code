#include <IRremote.h>

int RECV_PIN = 2;      
IRrecv irrecv(RECV_PIN); 
decode_results results;

void setup()
{
  int i;
  for(i=0;i<10;i++)
  {
    pinMode(i,OUTPUT);
  }
  Serial.begin(9600);   
  irrecv.enableIRIn();  
}

void loop() {
  
  if (irrecv.decode(&results)) 
  {
    Serial.println(results.value,HEX);   
    
    if (results.value==0XFD08F7)
    {
      digitalWrite(7,HIGH);
      delay(50);
      digitalWrite(7,LOW);
    }
    
    else if (results.value==0XFD8877)
    {
      digitalWrite(8,HIGH);
      delay(50);
      digitalWrite(8,LOW);
    }
    
    else if (results.value==0XFD48B7)
    {
      digitalWrite(9,HIGH);
      delay(50);
      digitalWrite(9,LOW);
    }
   
    else if (results.value==0XFD28D7)
    {
      digitalWrite(10,HIGH);
      delay(50);
      digitalWrite(10,LOW);
    }
   
    else if (results.value==0XFDA857)
    {
      digitalWrite(11,HIGH);
      delay(50);
      digitalWrite(11,LOW);
    }
   
    else if (results.value==0XFD6897)
    {
      digitalWrite(12,HIGH);
      delay(50);
      digitalWrite(12,LOW);
    }
    
      irrecv.resume();                    
  }
}
