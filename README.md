# I2C-Receiver-Temperature-Sensor
Projet for the course of hardawre/software platforms (M. Valderrama) at the Faculty Polytechnic of Mons Belgium. The members of the project are : Denis Pierre, Liégeois Loïc & Rasic Cyril.
# Introduction
The goal of this project is to be the master of a I2C bus linking a temperature sensor and a reader. Being the master means that we are the only one able to initiate a communication on the bus.
The project is devided in two parts, the first is the software and the second one is the hardware part.

The project is built as following : Software linked to the harware - hardware linked to the bus 

# SOFTWARE
The code (C) is following this algorithm :

-Fetch the bits in the register :

We get the address from the terminal where we do an IPconfig. The IP adress is then to be put in putty (ssh).

-Convert the unsigned int bits :

The bits are coded in 2's complement (-127 to 127) but stored in a variable of type int unsigned (0 to 255). Due to that, we have to convert the integer and the decimal part in a int type
<br><br>
![image](image1hs.jpg)

In the sowtware branch you can find several files :

- main.c

The main file is the code that have to be run making everything working together. It displays the temperature measured by the sensor.

- hps_0.h
All the adress are stored in this file.

- DRIVER_read.h & DRIVER_read.c

These two codes are used to realise the algorithm explained above.

# HARDWARE
The goal of the harware part is to build the I2C driver on quartus.
<br><br>
The physical scheme of the driver is presented on the following pictures. On it, you can see all the different logic gates and all the hardware circuit user to build the driver.
![image](hs2.png)
![image](hs3.png)
![image](hs4.png)
![image](hs5.png)

The two following pictures show the test bench results after simulation. On it, we see the bits received after a simulation of communication on the bus.
![image](hs8.png)
![image](hs9.png)


# Other ressources
To learn more about the project, you can refer to our youtube video where we show each thing that we built.
https://www.youtube.com/watch?v=_gH3XU8YFmI
