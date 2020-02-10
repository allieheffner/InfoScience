# These are my coding projects

Here's the code for the dice

```.py
def setup():
    size(700,700)
  
def mouseClicked(): 
    fill(255,255,255)
    rect(100, 100, 505, 505, 50);
    fill(0, 0, 0)
    
    dice=int(random(1,10))
    if dice == 1:
        circle (350,350,60)
        
    if dice == 2:
        circle(500,200,50)
        circle(200,500,50)
        
    if dice == 3:
        circle(350,350,50)
        circle(200,200,50)
        circle(500,500,50)
    if dice == 4:
        circle(200,200,50)
        circle(500,500,50)
        circle(500,200,50)
        circle(200,500,50)
        
    if dice == 5:
        circle(200,200,50)
        circle(500,500,50)
        circle(500,200,50)
        circle(200,500,50)
        circle(350,350,50)
        
    if dice == 6:
        circle(200,200,50)
        circle(500,500,50)
        circle(500,200,50)
        circle(200,500,50)
        circle(200,350,50)
        circle(500,350,50)
        

def draw():
    circle(0,0,0)
    
```.py

