# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB

## AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed

•	Computer with i3 Processor
•	SCI LAB


## Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results


## PROGRAM
```
//Mean
function X=f(x)
    z=3*(1-x)^2;
    X=x*z;
endfunction

a=0;
b=1;

EX=intg(a,b,f);
function Y=c(y)
    z=3*(1-y)^2;
    Y=y*z;
endfunction

EY=intg(a,b,c);
disp("i)Mean of X =",EX)
disp("ii) Mean of Y =",EY)

//Variance

function X=g(x)
    z=3*(1-x)^2;
    X=x^2*z;
endfunction

a=0;
b=1;

EX2=intg(a,b,g);
function Y=h(y)
    z=3*(1-y)^2;
    Y=y^2*z;
endfunction

EY2=intg(a,b,h);

vX2=EX2-(EX)^2;
vY2=EY2-(EY)^2;

disp("iii) Variance of X",vX2);
disp("iv) Variance of Y",vY2);

// Cross Correlation

x=input("type in the reference sequence=");
y=input("type in the second sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);


```


## CALCULATION
<img width="522" height="850" alt="image" src="https://github.com/user-attachments/assets/8424e84f-7414-4e4e-bb8a-e39fc211ab24" />

<img width="534" height="836" alt="image" src="https://github.com/user-attachments/assets/b6748d4f-32ce-469c-8013-24248d9ec02c" />






## OUTPUT

<img width="1918" height="1138" alt="Mean variance output waveform" src="https://github.com/user-attachments/assets/fefa94e3-3150-42d5-b770-fef006e06095" />



<img width="507" height="421" alt="mEAN" src="https://github.com/user-attachments/assets/f56e7ed6-4004-4903-a82d-a710a1d97c0f" />



## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
