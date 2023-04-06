Modeling of Library Flow Evacuation
====
Background
----------
This is part of my undergraduate graduation thesis.Cellular automata method was used to realize pedestrian evacuation simulation in the library,which is one of my undergraduate school. After completion of the simulation, the way I use hypothesis test about the structure of the library in the design of evacuation escape ability check, satisfactory results were obtained, and this is just one part of the evacuation modeling, I think the simulation using this model, and analyze the data to teach is easy, so did not upload the hypothesis test. Also, please note that due to some incompatibilities between NETLOGO versions, be sure to use NetLogo3D6.1.1, otherwise you may need to debug the code several times to run it.

Install
---------
NETLOGO is a a multi-agent programmable modeling environment, and is devloped by Uri Wilensky from Northwestern University.

 * To install `NetLogo3D6.1.1`,please visit https://ccl.northwestern.edu/netlogo/
 
 * To learn more about Netlogo, refer to `An Introduction to Agent-Based Modeling: Modeling Natural, Social, and Engineered Complex Systems with NetLogo`,you can have a deeper understanding about modeling after reading this book. 

How to build a model
--------
There are three kinds of agents in Netlogo, turltes, patches and observers. turtles can move in the environment, but patches cannot. Obervers can give turtles and patches orders. you can create different viriables for differents agents, and agents can access these virables.

To build the model of library, you can set different patches to different colors. To model pedestrain in the library, you can set some turtles in these areas. The following is a example that has been done:

![image](https://github.com/WangSuhan/library-evacuation-model/blob/master/picture1.png)

The library is divided into different parts, so that turtles can access the color of patch to distinguish different areas in the environment.

Algorithm
---------
This is a classical evacuation algorithm. In a two-dimensional scenario, calculate the distance from each patch to the exit, and store this number in each patch, when turtle arrive the patch, it can get the number, and also the number around it. Then the turtle make a dicision according to this number about next patch it can go. Refer to the following figure:
