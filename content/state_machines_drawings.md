# State Machines 

Like any other kind of programming the best way is to cut down to pen and paper and design your idea before facing the IDE that can be distractive when you need to code a slightly more complex function.

First it is defined what kind of variables you have, dividing them into inputs and outputs. For example in a radio controlled car, the trottle is an intput and the engine velocity is an output.

In microcontrollers the way of designing your project is by sketching a State Machine that is defined as follows:

![image](https://user-images.githubusercontent.com/71400611/219400648-0815abe4-7d00-4a53-9b63-ecba66e83e30.png)


It is composed of various States that correspond to an output combination. In the given example, two combinations are possible, engine ON and engine OFF. Those States are reached conditionaly according to the given inputs.
These diagrams are very important so you don't forget to specify any state or any action for a given set of inputs, which could lead to a unexpected chain of events, and saves you some debugging time. 



# State Machines on Code

The world would be ideal if State Machines were just doing the drawings and it was done. But unfortunately we need to type all the steps... 

It would take some time to write all about it, so I will leave here the coding steps to follow and then a repository where you can check for yourself how it is done!

  1. Read Inputs
  2. Calculate next states
  3. Update States
  4. Write Outputs

I know it is a little abstract by only seeing these steps, but you have an example on this [repository](https://github.com/Smiguel02/ACE/tree/main/ACE_01/src)

## Time loop

Also and advantage of state machine sis that you can easily set your **time intervals without using delays()**. This is super importante because with delays() if anything happened to your code, you wouldn't be able to exit that function, but by having everything inside an **if** it works! Here is and example:

``` C
void setup(){
(...)
}
#define CYCLE_INTERVAL 50 //microsseconds

unsigned long current_time=micros(); //or millis()
unsigned long last_cycle=micros();

void loop(){
  
  current_time=micros();
  
  if(current_time-last_cycle<CYCLE_INTERVAL){
  last_cycle=micros();
  /*Your State Machine Code here*/
  }

}
```


[Main Menu](../readme.md)
