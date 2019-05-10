# Etapas-3-e-4

EQUIPE:

Aluno: Thiago Souza de Oliveira

Aluno: MOISES SIQUEIRA DE ALCANTARA


Eatapa 03 - *Aparecimento aleatório do objeto assim que toca a extremidade direita da tela de saída*




var xo = 0;
var yo = 50;

function setup() {
  createCanvas(500,500);
}

function draw() {

  background(220);
  
  rect(xo, yo, 40, 40);
  
  xo=xo+4;
  
  if(xo > 500){
     xo = -random(1000);
    console.log(xo);
  }
  
}








Etapa 04 - *Fazendo a projeção do tiro...*

var x = 100;

var y = 100;

var v = 15

var xd = 0;

var yd = 0;

var estadoDisparo = false



function setup() {
  createCanvas(513, 513);
}

function draw() {
  background(220);
  
  if(keyIsDown(LEFT_ARROW))
    x-=v;
  
  if(keyIsDown(RIGHT_ARROW))
    x+=v;

   if(keyIsDown(UP_ARROW))
    y-=v;
  
  if(keyIsDown(DOWN_ARROW))
    y+=v

  ellipse(x,y,50,50)
  
  if(keyIsDown( CONTROL ) && estadoDisparo == false ){
    xd = x
    yd = y
    estadoDisparo = true
}

  if (estadoDisparo == true){
  ellipse(xd, yd, 4, 4);
    yd = yd - 10;
    if (yd < 0){
    estadoDisparo = false
    }
    
}
}

