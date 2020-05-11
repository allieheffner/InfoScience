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

Here's the code for the Coronavirus simulation

x = [100,200] # represent a list by using square brackets
y = [100,250]
h = [False, True]



def setup():
size(500,500)
for n in range(20):
x.append(random(0,500))
y.append(random(0,500))
h.append("Healthy")

def distance(x1, x2, y1, y2):
a = (x1-x2)
b =(y1-y2)
c = sqrt(a**2 + b**2)
return c

def draw():
global x, y
background(255)

#create individual
for ind in range(len(x)):
if h[ind] == True:
fill(255)
elif h[ind] == "Recovered":
fill(50, 230, 120)
else:
fill(255,0,0)
circle(x[ind], y[ind], 40)

#calculate the distance to each neighbour
for nei in range(len(x)):
if nei == ind:
continue
d = distance(x[ind], x[nei], y[ind], y[nei])
if d < 40 and (h[nei] == False or h[ind]== False):
h[ind] = False
h[nei] = False

for m in range(len(x)):
#move

#move randomly
x[m] += random(-20, 20)
y[m] += random(-20,20)

#boundaries conditions
if x[m] > 500:
x[m] = 500
if y[m] > 500:
y[m] = 500
if x[m]< 0:
x[m] = 0
if y[m]< 0:
y[m]= 0

delay(1)

days = [30,-1]



delay(100)
