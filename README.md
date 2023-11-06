# 4. Single server with infinite capacity (M/M/1):(oo/FIFO)


## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![exp no 04 theroy](https://github.com/DINESH18032004/Single-server-infinite-capacity---Markov-Model/assets/119477784/c6fa3bf5-5939-47ea-a5e6-3d6f534e1041)


This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![exp 04 pro](https://github.com/DINESH18032004/Single-server-infinite-capacity---Markov-Model/assets/119477784/673c4e85-4d02-44a2-bc55-3f739c4d5cca)


## Experiment:

![exp 04 1](https://github.com/DINESH18032004/Single-server-infinite-capacity---Markov-Model/assets/119477784/268b7c90-6e0d-4647-a6e0-8179a059e238)


 ![exp no 04 2](https://github.com/DINESH18032004/Single-server-infinite-capacity---Markov-Model/assets/119477784/f09587b4-14df-4767-a661-6dd0fd9637d2)

## Program

Developed By: PRAVEEN S

Register No:212222240078


```
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs):
"))
ser_time=float(input("Enter the mean inter service time of Lathe Machine (in secs) :
"))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) : "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rate per second : %0.2f "%lam)
print("The mean service rate per second : %0.2f "%mu)
if (lam < mu):
Ls=lam/(mu-lam)
Lq=Ls-lam/mu
Ws=Ls/lam
Wq=Lq/lam
print("Average number of objects in the system : %0.2f "%Ls)
print("Average number of objects in the conveyor : %0.2f "%Lq)
print("Average waiting time of an object in the system : %0.2f secs"%Ws)
print("Average waiting time of an object in the conveyor : %0.2f secs"%Wq)
print("Probability that the system is busy : %0.2f "%(lam/mu) )
print("Probability that the system is empty : %0.2f "%(1-lam/mu) )
else:
print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```
## Output :

![EXP NO 04 maths](https://github.com/DINESH18032004/Single-server-infinite-capacity---Markov-Model/assets/119477784/d23c69fe-61c5-43ab-8cda-45b904d9ff49)


## Result :

The average number of material in the sysytem and in the conveyor and waiting time are
successfully found.
