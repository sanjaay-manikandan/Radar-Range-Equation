#                                                                                                EVALUATION OF RADAR RANGE 

## AIM :

  To calculate the maximum range of a radar system using the Radar Range Equation and verify the results 

## Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/aef551f5-cd66-4289-9f89-c1b43eeb230d" />


## Procedure
1.	Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.
2.	Import Necessary Libraries: Import the math library in Python.
3.	Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
4.	Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
5.	Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
6.	Execute the Program: Run the Python script to calculate and display the maximum range of the radar.


## Code :
``` scilab
Pt = 500;
G = 40;
lambda = 0.03;
sigma = 1;
L = 1;

R = 500:500:50000;
Pr_R = (Pt * G^2 * lambda^2 * sigma) ./ ((4*%pi)^3 * R.^4 * L);
subplot(3,1,1);
plot(R/1000, 10*log10(Pr_R));

Pt_values = 100:100:5000;
R_fixed = 20000;
Pr_Pt = (Pt_values * G^2 * lambda^2 * sigma) ./ ((4*%pi)^3 * R_fixed^4 * L);
subplot(3,1,2);
plot(Pt_values, 10*log10(Pr_Pt));

G_values = 1:1:80;
R_fixed = 20000;
Pt_fixed = 500;
Pr_G = (Pt_fixed * (G_values.^2) * lambda^2 * sigma) ./ ((4*%pi)^3 * R_fixed^4 * L);
subplot(3,1,3);
plot(G_values, 10*log10(Pr_G));


```

## Tabular Column :

## Output Graph :

<img width="1912" height="997" alt="image" src="https://github.com/user-attachments/assets/7525210e-8ff6-4b5a-a529-416d7f5c81e6" />


## Result:

Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program.

