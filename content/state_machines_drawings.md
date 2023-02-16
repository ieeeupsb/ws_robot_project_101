# Extras - State Machines

Like any other kind of programming the best way is to cut down to pen and paper and design your idea before facing the IDE that can be distractive when you need to code a slightly more complex function.

First it is defined what kind of variables you have, dividing them into inputs and outputs. For example in a radio controlled car, the trottle is an intput and the engine velocity is an output.

In microcontrollers the way of designing your project is by sketching a State Machine that is defined as follows:

![image](https://user-images.githubusercontent.com/71400611/219400648-0815abe4-7d00-4a53-9b63-ecba66e83e30.png)


It is composed of various States that correspond to an output combination. In the given example, two combinations are possible, engine ON and engine OFF. Those States are reached conditionaly according to the given inputs.
These diagrams are very important so you don't forget to specify any state or any action for a given set of inputs, which could lead to a unexpected chain of events, and saves you some debugging time. 


[Main Menu](../readme.md)
