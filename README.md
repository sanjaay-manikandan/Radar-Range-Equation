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
lambda = 0.03; 
sigma = 1;     

Pt_vals = 0.1:0.1:10;   
Gt_const = 35;           
Pm_const = 1e-13;        

Rmax_Pt = ((Pt_vals .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);

Gt_vals = 1:1:50;        
Pt_const = 2;            
Pm_const = 1e-13;

Rmax_Gt = ((Pt_const .* Gt_vals.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);
Pm_vals = logspace(-15, -10, 50); 
Pt_const = 2;
Gt_const = 35;

Rmax_Pm = ((Pt_const .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_vals)).^(1/4);   

subplot(3,1,1);
plot(Pt_vals, Rmax_Pt, 'r', 'LineWidth', 2);

subplot(3,1,2);
plot(Gt_vals, Rmax_Gt, 'g', 'LineWidth', 2);

subplot(3,1,3);
plot(Pm_vals, Rmax_Pm, 'b', 'LineWidth', 2);

```

## Tabular Column :

![RADAR RANGE](https://github.com/user-attachments/assets/3218ebe0-c7ea-4474-aaf9-e14c68c4f627)


## Output Graph :

<img width="1527" height="965" alt="image" src="https://github.com/user-attachments/assets/d5af6ad6-a096-417d-a762-ed9d7f9184fa" />


## Result:

Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program.

