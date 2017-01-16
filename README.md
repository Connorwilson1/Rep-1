# Rep-1
The First Repository
I am currently making some changes, please help me it is 2.15 am and I want to sleep but I am curious about this and I want to get uni work done.
*/

Clock clock;
Theme theme;

void settings(){
  fullScreen(); 
}

void setup(){
  noCursor();
  
  theme = Theme.DARK;
  
  // Create Clock with radius just less than half of display height
  clock = new Clock(displayHeight * 0.45, theme); 
}

void draw(){
  background(clock.getBackgroundColor());
    
  // draw all of the clock components
  clock.drawClockFace();
  clock.drawHours();
  clock.drawMinutes();
  clock.drawSeconds();
}

void mousePressed(){
  
  if (theme == Theme.DARK) {
    theme = Theme.LIGHT;
  }
  else {
    theme = Theme.DARK; 
  }
  
  clock.setTheme(theme);
}
