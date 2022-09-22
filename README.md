# Static-Timing-Analysis
VSD Udemy Course Static Timing Analysis

## Installing OpenTimer
To install the opentimer, 
  - Make sure cmake is installed
  - Type the following commands in the terminal
  
I am cloning the OpenTimer repo in `Desktop/sem_5/asic` directory.It can be done anywhere
```
git clone https://github.com/OpenTimer/OpenTimer.git
cd OpenTimer
mkdir build
cd build
cmake ../
make 
```
<p align="center">
  <img src="/images/sta1.png">
</p><br>

## Invoking OpenTimer
Opentimer can be invoked by typing the following command 
```
cd Desktop/OpenTimer
./bin/ot-shell
```
<p align="center">
  <img src="/images/sta2.png">
</p><br>

I made an alias for the command so that opentimer can be invoked easily.

```
alias ot='Desktop/sem_5/asic/OpenTimer/bin/ot-shell'
```
<p align="center">
  <img src="/images/sta3.png">
</p><br>

The commands available in `OpenTimer can be viewed by typing the command `help` in after invoking OpenTimer.
<p align="center">
  <img src="/images/sta4.png">
</p><br>

## Specifying Constraints in OpenTimer

Consider the following example of timing constaint file for the design shown in below figure.

<p align="center">
  <img src="/images/sta5.png">
</p><br>

```
clock clk 1000 50
at clk 0 500 0 500
at in 50 50 100 100
slew clk 70 50 70 50
slew in 150 100 150 100
load out 40
rat out 160 160 180 180
```

From `clock clk 1000 50` we can tell that `clk` is the primary input of the design and it is a clock input. *clock* is a keyword. 
We also assume in OpenTimer that clock goes from low to high.Here, clk has a period of 1000ps/1ns and a 50% duty cycle.

<p align="center">
  <img src="/images/sta6.png">
</p><br>

Consider `at clk 0 500 0 500`. This signifies arrival time(at) of the clock.
<p align="center">
  <img src="/images/sta7.png">
</p><br>


# Contributors 

- **B Sathiya Naraayanan** 
- **Kunal Ghosh** 



# Acknowledgments


- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.

# Contact Information

- B Sathiya Naraayanan, IMT2020534, International Institute of Information Technology, Bangalore  ,Sathiya.Naraayanan@iiitb.ac.in
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
