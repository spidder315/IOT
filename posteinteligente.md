# Projeto de Poste inteligente

Este projeto foi desenvolvido dentro do Tinkercad, na disciplina de Internet das Coisas (IOT), para a criação de um protótipo com arduino que simula um Poste inteligente que permite que o Arduino leia a intensidade da luz e controle a intensidade do LED com base na leitura do sensor.

# componentes usados

Arduino Uno.

LED: Um diodo emissor de luz que será controlado pela leitura do sensor de luminosidade.

Resistor para o LED: Geralmente um resistor de 220Ω ou 330Ω é usado em série com o LED para limitar a corrente e evitar que o LED queime.

Sensor de Luminosidade (por exemplo, LDR - Resistor Dependente de Luz): Um componente que varia sua resistência com a quantidade de luz que incide sobre ele.

Resistor para o LDR: Um resistor (geralmente entre 10kΩ e 100kΩ) é usado em um divisor de tensão com o LDR para permitir a leitura do nível de luminosidade no pino analógico.

Fios de Conexão: Fios jumpers para fazer as ligações entre os componentes e a placa Arduino.

# Montagem do circuito

![Imagem do Circuito](posteinteligente.png)

# Explicação do Código

int led =4;
int led =3;
int sensorluminosidade= A0;

int luz =0;

void setup()
{
  
  pinMode(led,OUTPUT);
  
  pinMode(sensorluminosidade,INPUT);
}

void loop()
{
 
 
  luz = analogRead(sensorluminosidade);
  
 
  
  if(luz<500){
   digitalWrite(led,HIGH); 
   
   
  analogWrite(led,1023);
   
  } else if (luz >= 500 && luz < 900) {
 
 
   
  analogWrite(led,500);
   
  }else{ 
   digitalWrite(led,LOW); 
    
    analogWrite(led,0);
 
  }
 
}

int sensorluminosidade =A0;

void setup()
{

  pinMode(led,OUTPUT);
 
  pinMode(sensorluminosidade, INPUT);
}

void loop()//variaveis
int led =3;
int sensorluminosidade= A0;

int luz =0; 

void setup()
{
 
  pinMode(led,OUTPUT);
  
  pinMode(sensorluminosidade,INPUT);
}

void loop()
{
  
  
  luz = analogRead(sensorluminosidade);
  
 
  if(luz<500){
   digitalWrite(led,HIGH);
    
  
  analogWrite(led,1023); 
    
  }if(luz>500 & luz<900){
  
   
    analogWrite(led,500); 
    
  }else{ 
    digitalWrite(led,LOW); 
  
    
  analogWrite(led,0);
  
  }
  
}
{
  
  luz = analogRead(sensorluminosidade);
  
  
  if(luz<500){
    digitalWrite(led,HIGH);
  }else{//se tiver luz
    digitalWrite(led,LOW); 
  }
}
