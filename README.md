
Hi, here is the description of a project I have been working on for some time. It's supposed to be a two-legged robot.
I have a Master in Machine Learning so you might wonder if this project is not too far from my competencies and interest centers. I would answer that 
I tried to diversify my studies as much as possible to have an overview of the field of robotics. I learned electronics, mechanics, control, automation, visions, health and of course Machine Learning. Indeed I believe symbiose between all the levels of a system from its mechanical conception to its algorithms passing by its sensor is the key for high performance robots.

This project is innovative in its motorization. As with hydraulic systems, there is a motor providing most of the mechanical power
with the difference that control and transmission are carried out using universal joints and worm gears.
I like these kinds of systems because they provide light limbs (very important for fast movements), a good power-to-weight ratio, and allow you to concentrate the
effort in the desired joint at the desired time.
I tried to develop my own mechanisme as I really like research of new posssible paradigms. It took me about two months to make the CAO and one additionnal month to build the first leg with only two actuated joints for the moment.

![image](https://user-images.githubusercontent.com/71259481/161513728-d9715894-1d42-4d84-a139-c8082130c227.png)


Unlike previous project I used servo-motors electronics to control the joint. Previously I just used potentiometres connected to the Arduino controlling the motors through H-bridges. But the Arduino with several motors to control was to slow to provide a proper closed-loop control. Furthermore the wires could be up to one meter long, then there was a lot of noise. Therefore servo motor are a good solution as each controller is placed closed to each corresponding potentiometre and motor. Nevertheless the dynamics of my system are slower than the one the servo controller was designed for. So sometimes the joint might strongly oscillate. This is a very bad drawback but as it rarely happens I consider this is acceptable for this cheap and fast solution. Furthermore as I don't need analog readings anymore (servo control is only digital) I can use a Raspberry Pi directly instead of using a communication with an Arduino to handle analog measurments (this was very slow!).

Once this leg will be finished I will conduct some strength and precision tests. Then the controler design will start. I plan to use machine learning with vision to improve balance keeping (an external camera looking at the robot to monitor its leg position). In fact according to what I have seen, potentiometres only are not enough, the error are not negligible with a one meter leg. I think I could had some force sensor in the joint to increase precision.
