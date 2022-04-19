# area---SA-calculations
code to calculate the surface area or area of shapes with the user input 
from decimal import Decimal
import math



def welcomemessage():                 #welcoming mesage 
    print("hello, this is a practice code \nit is a calculator for areas and surface areas")
    print("")

def areas():                 #here the calculation famulas for areas are done
    whichArea=input("area of what?: ")
    if whichArea=="square":
        inputBase=int(input("enter value of the base: "))
        areaOfsquare=inputBase*inputBase
        print(str(areaOfsquare) +" is the area of the square")
    

    elif whichArea=="rectangle":
        inputBase=int(input("enter value of the base: "))
        intputWidth=int(input("enter value of the base: "))
        areOfRectangle=inputBase*intputWidth
        print(str(areOfRectangle)+" is the area of the rectangle")

    elif whichArea=="circle":
        inputRadius=int(input("enter the radius: "))
        areaOfCircleNotRound=((inputRadius*inputRadius)* math.pi)        #here it multiplies the radius by pi, but does not round the answer
        areaOfcircleRound= format(areaOfCircleNotRound, '.4f')           #here it rounds the answer to 4 decimal places
        print(str(areaOfcircleRound)+" is the area of the circle")

    elif whichArea=="triangle":
        inputBase=int(input("enter the base: "))
        inputHeight=int(input("enter the height: "))
        areaOfTriangle=((inputBase*inputHeight)/2)
        print(str(areaOfTriangle)+" is the area of the triangle")

    elif whichArea=="trapezoid":
        inputBaseOne=int(input("enter the first base: "))
        inputBaseTwo=int(input("enter the second base: "))
        inputHeight=int(input("enter the height: "))
        areaOfTrapez=(((inputBaseOne+inputBaseTwo)/2)*inputHeight)
        print(str(areaOfTrapez)+" is the area of the trapezoid")

    elif whichArea=="ellipse":
        maj=inputMajRadius=int(input("enter value of major radius: "))
        min=inputMinRadius=int(input("enter value of minor radius: "))
        areaOfEllipse=((math.pi)*min*maj)
        areaOfEllipseRound=format(areaOfEllipse, '.4f')
        print(areaOfEllipseRound+" is the area of the ellipse")
    else:
        print("test")

    


def surfacearea():                      #here it calculates surface areas 
     whichArea=input("surface area of what?: ")
     if whichArea=="pyramid":
        l=inputBaseLenght=int(input("enter value of base lenght: "))
        w=inputBaseWidth=int(input("enter value of base width: "))
        h=inputHeight=int(input("enter value of height: "))
        areaOfPyramid=((l*w)+(l*(math.sqrt(((w/2)*(w/2))+(h*h))))+(w*(math.sqrt(((l/2)*(l/2))+(h*h)))))
        areaOfPyramidRound= format(areaOfPyramid, '.4f')
        print(areaOfPyramidRound+" is the area of the pyramid")

     elif whichArea=="cuboid":
        l=inputLenght=int(input("enter value of lenght: "))
        w=intputWidth=int(input("enter value of width: "))
        h=inputinputHeight=int(input("enter the value of height: "))
        areaOfCuboid=((2*l*w)+(2*l*h)+(2*h*w))
        areareaOfCuboidround=format(areaOfCuboid, '.4f')
        print(areareaOfCuboidround+" is the area of the rectangular cuboid")




    



def askAreaOrSA():            #user input as well as figuring what type of calculation they want
    
    firstquestion=input("surface area or area?:  ")
    
    if firstquestion=="area":        #if they picked area, then ask area of what
        areas()
        askRetry()
    elif firstquestion =="surface area":
        surfacearea()
        askRetry()
 

def askRetry():           #here it asks if another calculation wants to be made
     
     repeatYorN=(input("do you have another question?(y/n): "))
     if repeatYorN == "y" :
         askAreaOrSA()      #if yes, it goes tot he section where it asks for input
         
         
     if repeatYorN == "n" :
         print(str("thanks for testing"))   #end message
         


      
            


        



def main():
    
    welcomemessage()
    askAreaOrSA()
    #askRetry()
    
    


if __name__=="__main__":      
   main()
