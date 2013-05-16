Easing
======

Gets ball to follow mouse

    float x;
    float y;
    float circleX;
    float circleY;
    float distX;
    float distY;
    float easing = 0.1;
    
    void setup() {
      size(500,500);
      colorMode(HSB,360,100,100);
      circleX = width/2;
      circleY = height/2;
    }
    
    void draw() {
      background(0);
      x = mouseX;
      y = mouseY;
      fill(200,100,100);
      ellipse(circleX,circleY,30,30);
      distX = x-circleX;
      distY = y-circleY;
      circleX+=distX*easing;
      circleY+=distY*easing;
    }
