# Large-Colorful-Clock
Large colorful clock on Processing
void setup() {

size(800, 800);

stroke(255);

smooth();

}

void draw() {

background (275, 100, 320);

fill(400, 210, 0);

noStroke();

// Angles for sin() and cos() start at 5 o'clock;

// add HALF_PI to make them start at the bottom

rect(200, 50, 800, 1000);

float s = map(second(), 0, 60, 0, TWO_PI) + HALF_PI;

float m = map(minute(), 0, 60, 0, TWO_PI) + HALF_PI;

float h = map(hour() % 12, 0, 12, 0, TWO_PI) + HALF_PI;

stroke(255);

strokeWeight(10);

line(500, 500, cos(s) * 72 + 200, sin(s) * 72 + 200);

strokeWeight(20);

line(500, 500, cos(m) * 60 + 100, sin(m) * 60 + 100);

strokeWeight(15);

line(500, 500, cos(h) * 50 + 200, sin(h) * 50 + 200);
text("Michelle's Clock", 70, 350);



rect(800, 100, 100, 100);
scale(2);
rect(30, 20, 50, 50);
rect(30, 20, 50, 50);
scale(0.5);




}
