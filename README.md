# Cod_ProjetoA3_SistemasComputacionais
int pino6 = 6;
int pino7 = 7;
int pino5 = 5; 
int pino4 = 4;
int pino3 = 3;
int pino2 = 2;
int pino11 = 11;

void setup()
{
  pinMode(pino6, INPUT);
  pinMode(pino7, INPUT);
  pinMode(pino5, OUTPUT);
  pinMode(pino4, OUTPUT);
  pinMode(pino3, OUTPUT);
  pinMode(pino2, OUTPUT);
  pinMode(pino11, OUTPUT);

  digitalWrite(pino5, LOW);
  digitalWrite(pino4, LOW);
  digitalWrite(pino3, LOW);
  digitalWrite(pino2, LOW);
  digitalWrite(pino11, HIGH); 
}

void loop()
{
  if (digitalRead(pino7) == 0 && digitalRead(pino6) == 0) {
    digitalWrite(pino5, HIGH);
    digitalWrite(pino3, HIGH);
    digitalWrite(pino4, LOW);
    digitalWrite(pino2, LOW);
  }
  
  if (digitalRead(pino7) == 0 && digitalRead(pino6) == 1) {
    digitalWrite(pino5, HIGH);
    digitalWrite(pino4, LOW);
    digitalWrite(pino3, LOW);
    digitalWrite(pino2, LOW);
  }
  
  if (digitalRead(pino7) == 1 && digitalRead(pino6) == 0) {
    digitalWrite(pino5, LOW);
    digitalWrite(pino4, LOW);
    digitalWrite(pino3, HIGH);
    digitalWrite(pino2, LOW);
  }
  
  if (digitalRead(pino7) == 1 && digitalRead(pino6) == 1) {
    digitalWrite(pino5, LOW);
    digitalWrite(pino4, LOW);
    digitalWrite(pino3, LOW);
    digitalWrite(pino2, LOW);
  }
}
