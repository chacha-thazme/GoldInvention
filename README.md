# Miro
SIA2020DAP 수업 과제입니다.
 var sqrX = 0;
var sqrY = 0;
var sqrW = 20;
var sqrH = 20;

var i;
let intrX;
let intrY;
var intrW = 20;
var intrH = 20;

function setup() {
  createCanvas(600, 600);
  frameRate(5); 
  
}

function draw() {
  background(200);
  
  // draw square
  fill(255);
  noStroke();
  rect(sqrX,sqrY,sqrW, sqrH);
  
  // create interrupt object
    for (i=1; i<=25; i++)  {
    intrX = random(0.5,19.5)*30;
    intrY = random(0.5,19.5)*30;
    
    fill(50);
    noStroke();
    rect(intrX, intrY, intrW, intrH);
  }
  
  if (sqrX <= 0) {
    sqrX = 0;
  }
  if (sqrY <= 0) {
    sqrY = 0;
  }
  if (sqrX >= 600) {
    sqrX = 580;
  }
  if (sqrY >= 600) {
    sqrY = 580;
  }
  
}

function keyPressed() {
  if (keyCode === UP_ARROW) {
    sqrY -= 20;
  } else if (keyCode === DOWN_ARROW) {
    sqrY += 20;
  } else if (keyCode === RIGHT_ARROW) {
    sqrX += 20;
  } else if (keyCode === LEFT_ARROW) {
    sqrX -= 20;
  }
}
