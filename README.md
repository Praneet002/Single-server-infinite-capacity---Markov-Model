# Ex No : 4
# Date : 13/10/23
# Single server with infinite capacity (M/M/1):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![Screenshot (424)](https://github.com/VelasiriSreeja/Single-server-infinite-capacity---Markov-Model/assets/118344328/016527cb-62af-4191-b879-06c706994def)


This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![Screenshot (425)](https://github.com/VelasiriSreeja/Single-server-infinite-capacity---Markov-Model/assets/118344328/1c27ab7a-ff63-4a4e-ba9a-d22a7ae90b2c)


## Experiment:
![image](https://github.com/Vanitha-SM/Single-server-infinite-capacity---Markov-Model/assets/119557985/167967bf-5f56-4534-a09a-e09db679d7c3)
 
## Program
```python
### Developed by    : Praneet S
### Register Number : 212221230078
```
```python
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rate per second : %0.2f "%lam)
print("The mean service rate per second : %0.2f "%mu)
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print("Average number of objects in the system : %0.2f "%Ls)
    print("Average number of objects in the conveyor :  %0.2f "%Lq)
    print("Average waiting time of an object in the system : %0.2f secs"%Ws)
    print("Average waiting time of an object in the conveyor : %0.2f secs"%Wq)
    print("Probability that the system is busy : %0.2f "%(lam/mu) )
    print("Probability that the system is empty : %0.2f "%(1-lam/mu) )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```

## Output :
![Screenshot 2023-11-08 110023](https://github.com/Praneet002/Single-server-infinite-capacity---Markov-Model/assets/94308200/7e32ccbf-7824-47e5-9591-90b5d0e0afd3)


## Result :
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.
