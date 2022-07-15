# KDAG-Tasks
This is my task on image editing, processing and segmentation as a part of the selection procedure for Kharagpur Data Analytics Group

The dall-e prompts I have given for my Task-1 are:
1. Artificial Intelligence and Machine Learning
2. Data Analytics
3. Data Processing

In p5.js:
1. Firstly, I have used the default random chords code and edited it according to blue background and green strokes.

function setup() {
  createCanvas(400, 400);
  background(0, 0, 255);

  // translucent stroke using alpha value
  stroke(0, 255, 0,155);
}

function draw() {
  // draw two random chords each frame
  randomChord();
  randomChord();
}

function randomChord() {
  // find a random point on a circle
  let angle1 = random(0, 2 * PI);
  let xpos1 = 200 + 200 * cos(angle1);
  let ypos1 = 200 + 200 * sin(angle1);

  // find another random point on the circle
  let angle2 = random(0, 2 * PI);
  let xpos2 = 200 + 200 * cos(angle2);
  let ypos2 = 200 + 200 * sin(angle2);

  // draw a line between them
  line(xpos1, ypos1, xpos2, ypos2);
}

2. I have made a histogram using the following code:

function setup() {
  createCanvas(400, 400);
  background(255);
  
  fill(12, 10, 225, 180);
  stroke(129, 154, 251);
  rect(50, 380, 10, 20);
  rect(60, 350, 10, 50);
  rect(70, 330, 10, 70);
  rect(80, 320, 10, 80);
  rect(90, 330, 10, 70);
  rect(100, 310, 10, 90);
  rect(110, 300, 10, 100);
  rect(120, 320, 10, 80);
  rect(130, 340, 10, 60);
  rect(140, 350, 10, 50);
  rect(150, 370, 10, 30);

}

3. I punched the code of pulses on mouse click and bubble patterns with the following code but I have finally not used it. Still I am putting it here:

let angle = 0;

function setup() {
  createCanvas(710, 400);
  background(300);
  noStroke();
  fill(0, 150);
}

function draw() {
  variableEllipse(mouseX, mouseY, pmouseX, pmouseY);
  
  if (mouseIsPressed === true) {
    angle += 5;
    let val = cos(radians(angle)) * 12.0;
    for (let a = 0; a < 360; a += 75) {
      let xoff = cos(radians(a)) * val;
      let yoff = sin(radians(a)) * val;
      fill(125);
      ellipse(mouseX + xoff, mouseY + yoff, val, val);
    }
    fill(50);
    ellipse(mouseX, mouseY, 2, 2);
  }
}

function variableEllipse(x, y, px, py) {
  let speed = abs(x - px) + abs(y - py);
  stroke(speed);
  ellipse(x, y, speed, speed);
}
