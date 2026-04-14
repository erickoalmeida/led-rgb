<h1>LED for RGB: Research Project</h1>
<h2>Declarations:</h2>
<p>I make many codes for this project. And, in at the moment (04/14/26), I will finalize the code. I will update this repository in the future too.</p>
<h2>Logic Code and Fisical Circuits:</h2>
<div align="center">
  <img width="332" height="332" alt="Novo Projeto" src="https://github.com/user-attachments/assets/8415fae3-6f5f-4287-a46e-bd9e5e2e9ba8" />
  <img width="303px" height="332px" alt="image_led_green" src="https://github.com/user-attachments/assets/442206a7-9d0b-4668-bf41-074dd5d3204d">
</div>
<hr>
<div align="center">
  <img width="332" height="332" alt="Novo Projeto (1)" src="https://github.com/user-attachments/assets/5632cee0-3898-446b-b2d0-e3f44881b74e" />
  <img width="303px" height="332px" alt="image_led_blue" src="https://github.com/user-attachments/assets/6d79d5e8-31b4-4923-9a5a-9f10cfb1fda0">
</div>
<h2>Codes:</h2>
<code>
const int led_vermelho = 10;
const int led_azul = 9;
const int led_verde = 5;

// Tempo de cada etapa
int tempo = 1000;

// Sequência: 1 = Azul | 2 = Vermelho | 3 = Verde
int sequencia[] = {1, 2, 3, 4, 5, 6, 7};
int tamanho = 7;

void setup() {
  pinMode(led_azul, OUTPUT);
  pinMode(led_verde, OUTPUT);
  pinMode(led_vermelho, OUTPUT);
}

void loop() {

  for (int i = 0; i < tamanho; i++) {

    // Desliga todos
    analogWrite(led_vermelho, 0);
    analogWrite(led_azul, 0);
    analogWrite(led_verde, 0);

    // Liga conforme a sequência
    if (sequencia[i] == 1) { // Azul
      analogWrite(led_azul, 255);
      analogWrite(led_verde, 0);
      analogWrite(led_vermelho, 0);
    } 
    else if (sequencia[i] == 2) { // Vermelho
      analogWrite(led_azul, 0);
      analogWrite(led_verde, 0);
      analogWrite(led_vermelho, 255);
    } 
    else if (sequencia[i] == 3) { // Verde
      analogWrite(led_azul, 0);
      analogWrite(led_verde, 255);
      analogWrite(led_vermelho, 0);
    }else if(sequencia[i] == 4){
      analogWrite(led_azul, 255);
      analogWrite(led_verde, 0);
      analogWrite(led_vermelho, 255);
    }else if(sequencia[i] == 5){
      analogWrite(led_azul, 0);
      analogWrite(led_verde, 255);
      analogWrite(led_vermelho, 255);
    }else if(sequencia[i] == 6){
      analogWrite(led_azul, 255);
      analogWrite(led_verde, 255);
      analogWrite(led_vermelho, 0);
    }else if(sequencia[i] == 7){
      analogWrite(led_azul, 255);
      analogWrite(led_verde, 255);
      analogWrite(led_vermelho, 255);
    }
    delay(tempo);
  }
}
</code>
