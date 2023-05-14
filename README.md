# distro

This repo is the file distribution of the Ball on Wheel system.
The system is about a billiard ball is ballanced on a HUB motor where a BALLUF distance sensor used for position detecting, an Arduino Nano is used for ADC and 6 step commutation for HUB motor. The control algorithm runs on Scilab on any computer which communicates via UART with Arduino Nano.
https://drive.google.com/file/d/11ZUFCLI1WgMBgq3CjRYAuPaKNTTK7fin/view?usp=share_link
For modelling the space state equations are created from Newton and also Lagrange equations.
For controller design a state feedback method is done.

The following folders there are:
/model
 - Maxima source code of the model, arranging the system equations to space state form,
 - Scilab script for initials,
 - Scilab script for contnous time LQ controller and observer design, 
 - and xcos model in continous time;
/simulation (the real system in discrete time)
 - Scilab script for discrete time LQ controller and observer design,
 - and xcos model in discrete time;
/experiment_1 (target: float numbes usage on an OS, xcos scope, as simple as possible setup)
 - xcos model with Scilab atom of 'WG Serial Xcos IO Block'
 - Arduino code 
    - with Scilab atom of 'WG Serial Xcos IO Block' 
    - six step BLDC motor drive with 'simple-circuit.com' and BTS7960-M,
    - BALLUF distance measurement tool;
/experiment_2 (target: float number usage on Linux, without x-window, automatic start, ready for html serving)
 - Scilab srcipt with 
 - Arduino code 
    - with a single byte communication, Scilab atom of 'Serial Communication', 
    - six step BLDC motor drive with 'simple-circuit.com' and BTS7960-M,
    - BALLUF distance measurement tool;








