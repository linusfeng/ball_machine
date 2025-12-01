# Tennis Ball Shooter

add some description stuff here once it's finished...

  
# First Version

My first version of my ball machine was a design to test whether the method that I wanted to use to launch the balls was effective. It was only functional for launching the ball a few feet, and was poorly built as well. I abandoned the CAD halfway through due to not designing it well, and it had no other functionality besides being able to shoot the balls. However, it did serve its purpose and gave me confidence that this design would work in future designs with more features.

## CAD

The first thing that I did when building my first version was CAD a design for my shooter. For any mechanical project, creating a CAD is essential because it allows you to know exactly how you want to build your design and what parts you need to build it, without actually having to spend money on things like parts.

![V1 CAD](V1.pdf)

## Electrical

To power my first version, I simply used an Arduino Uno and a L298 motor driver to control the speed a direction of the two 12V Pololu motors that I was using. I used jumper wires to wire everything together, and powered them using a 12V battery. The wiring was quite messy and disorganized, but it got the job done, which was all I cared about since this was just the first version.

![V1 Wiring Diagram](v1_wiring_diagram.pdf)

insert picture of wiring IRL...

## Code

```c++
// Motor A connections
int enA = 9;
int in1 = 8;
int in2 = 7;
// Motor B connections
int enB = 3;
int in3 = 5;
int in4 = 4;


void setup() {
 // put your setup code here, to run once:
 // Motor A connections
 int enA = 9;
 int in1 = 8;
 int in2 = 7;
 // Motor B connections
 int enB = 3;
 int in3 = 5;
 int in4 = 4;
 // Set all the motor control pins to outputs
 pinMode(enA, OUTPUT);
 pinMode(enB, OUTPUT);
 pinMode(in1, OUTPUT);
 pinMode(in2, OUTPUT);
 pinMode(in3, OUTPUT);
 pinMode(in4, OUTPUT);
  // Turn off motors - Initial state
 digitalWrite(in1, LOW);
 digitalWrite(in2, LOW);
 digitalWrite(in3, LOW);
 digitalWrite(in4, LOW);
}


void loop() {
 // put your main code here, to run repeatedly:
 analogWrite(enA, 255);
 analogWrite(enB, 255);
 digitalWrite(in1, HIGH);
 digitalWrite(in2, LOW);
 digitalWrite(in3, HIGH);
 digitalWrite(in4, LOW);


}
```

# Second Version

I only CADed the second version of my ball machine. This was partly because I finished the CAD during the summer, when I didn't have access to my school's robotics workshop, so I couldn't machine any of the parts that I needed to build it. But also, I already had plans for the third version, and I knew that if I built the second version, I would end up wasting a lot of materials, so I let the second version stay as a CAD, and moved on to CADing the third version. The second version utilized Neo brushless motors instead of Pololu motors, which can spin at 5,676 rpm. It also has a basket attached to the top, which allows it to feed balls at a set rate.

## CAD

![V2 CAD](v2_cad.pdf)
