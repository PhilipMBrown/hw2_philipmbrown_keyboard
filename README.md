# hw2_philipmbrown_keyboard

#if defined(ARDUINO) 
SYSTEM_MODE(SEMI_AUTOMATIC); 
#endif

// Set pinvalues of knob and pushbuttons
int knob1 = D8;
int knob2 = D9;
int knob3 = D10;
int knob4 = D11;
int knob5 = D12;
int pushButton1 = D0;
int pushButton2 = D1;
int pushButton3 = D2;
int pushButton4 = D3;
int pushButton5 = D5;
int pushButton6 = D13;

// the setup routine runs once when you press reset:
void setup() {
  // initialize serial communication at 9600 bits per second:
  Serial.begin(9600);
  // make the knobs and tactile switches pins as inputs:
  pinMode(knob1, INPUT);
  pinMode(knob2, INPUT);
  pinMode(knob3, INPUT);
  pinMode(knob4, INPUT);
  pinMode(knob5, INPUT);
  pinMode(pushButton1, INPUT);
  pinMode(pushButton2, INPUT);
  pinMode(pushButton3, INPUT);
  pinMode(pushButton4, INPUT);
  pinMode(pushButton5, INPUT);
  pinMode(pushButton6, INPUT);
}

// the loop routine runs over and over again forever:
void loop() {
  
  // read the input pin for knob and pushbuttons:
  int knobState1 = digitalRead(knob1);
  int knobState2 = digitalRead(knob2);
  int knobState3 = digitalRead(knob3);
  int knobState4 = digitalRead(knob4);
  int knobState5 = digitalRead(knob5);
  int buttonState1 = digitalRead(pushButton1);
  int buttonState2 = digitalRead(pushButton2);
  int buttonState3 = digitalRead(pushButton3);
  int buttonState4 = digitalRead(pushButton4);
  int buttonState5 = digitalRead(pushButton5);
  int buttonState6 = digitalRead(pushButton6);
  
  // Check state of knob, and then check state of individual buttonsw:
  
  if (knobState1 == LOW){
    if (buttonState1 == LOW){
    Serial.print('a');
    delay(625);        
    }
    else if (buttonState2 == LOW){
    Serial.print('b');
    delay(625);        
    }
    else if (buttonState3 == LOW){
    Serial.print('c');
    delay(625);        
    }
    else if (buttonState4 == LOW){
    Serial.print('d');
    delay(625);        
    }
    else if (buttonState5 == LOW){
    Serial.print('e');
    delay(625);        
    }
    
    // If the space button is held, weight 2 sec and see if button 1 is held. If button 1 is not held, create a space, if button one is held after 2 seconds, create the letter 'z'. This is the same for all 5 knob states.
    
    else if (buttonState6 == LOW){
      delay(2000)
      if (buttonState1 == HIGH){
      Serial.print(' ');
      delay(625);        
      }
      else if (buttonState1 == LOW){
      Serial.print('z');
      delay(625);
    }
  }
  }
  
  else if (knobState2 == LOW){
    if (buttonState1 == LOW){
    Serial.print('f');
    delay(625);        
    }
    else if (buttonState2 == LOW){
    Serial.print('g');
    delay(625);        
    }
    else if (buttonState3 == LOW){
    Serial.print('h');
    delay(625);        
    }
    else if (buttonState4 == LOW){
    Serial.print('i');
    delay(625);        
    }
    else if (buttonState5 == LOW){
    Serial.print('j');
    delay(625);        
    }
    else if (buttonState6 == LOW){
      delay(2000)
      if (buttonState1 == HIGH){
      Serial.print(' ');
      delay(625);        
      }
      else if (buttonState1 == LOW){
      Serial.print('z');
      delay(625);
    }
  }       
    
  }

  else if (knobState3 == LOW){
    if (buttonState1 == LOW){
    Serial.print('k');
    delay(625);        
    }
    else if (buttonState2 == LOW){
    Serial.print('l');
    delay(625);        
    }
    else if (buttonState3 == LOW){
    Serial.print('m');
    delay(625);        
    }
    else if (buttonState4 == LOW){
    Serial.print('n');
    delay(625);        
    }
    else if (buttonState5 == LOW){
    Serial.print('o');
    delay(625);        
    } 
    else if (buttonState6 == LOW){
      delay(2000)
      if (buttonState1 == HIGH){
      Serial.print(' ');
      delay(625);        
      }
      else if (buttonState1 == LOW){
      Serial.print('z');
      delay(625);
    }
  }
  }

  else if (knobState4 == LOW){
    if (buttonState1 == LOW){
    Serial.print('p');
    delay(625);        
    }
    else if (buttonState2 == LOW){
    Serial.print('q');
    delay(625);        
    }
    else if (buttonState3 == LOW){
    Serial.print('r');
    delay(625);        
    }
    else if (buttonState4 == LOW){
    Serial.print('s');
    delay(625);        
    }
    else if (buttonState5 == LOW){
    Serial.print('t');
    delay(625);        
    }
    else if (buttonState6 == LOW){
      delay(2000)
      if (buttonState1 == HIGH){
      Serial.print(' ');
      delay(625);        
      }
      else if (buttonState1 == LOW){
      Serial.print('z');
      delay(625);
    }
  }
  }

  else if (knobState5 == LOW){
    if (buttonState1 == LOW){
    Serial.print('u');
    delay(625);        
    }
    else if (buttonState2 == LOW){
    Serial.print('v');
    delay(625);        
    }
    else if (buttonState3 == LOW){
    Serial.print('w');
    delay(625);        
    }
    else if (buttonState4 == LOW){
    Serial.print('x');
    delay(625);        
    }
    else if (buttonState5 == LOW){
    Serial.print('y');
    delay(625);        
    } 
    else if (buttonState6 == LOW){
      delay(2000)
      if (buttonState1 == HIGH){
      Serial.print(' ');
      delay(625);        
      }
      else if (buttonState1 == LOW){
      Serial.print('z');
      delay(625);
    }
  }
}
}
