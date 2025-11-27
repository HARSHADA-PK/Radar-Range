## Aim:

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Scilab programming.

## Theory:

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by: image

<img width="483" height="547" alt="image" src="https://github.com/user-attachments/assets/38f7483b-cb10-4995-b7a7-9bf3ab716b6c" />

## Procedure

Refer to the Algorithm and write the Scilab code for the experiment.

Open Scilab on your system.

Create a New Editor File: Go to File → New → Script.

Type Your Code in the editor window.

Save the File with a suitable name (e.g., radar_range.sce).

Execute the Code:

Press F5 or click Execute → File with echo.

If Any Errors Occur: Review and correct the code.

Save and run it again until it executes successfully.

## PROGRAM:

```
Gt=70;
Gr=70;
L=0.04;
sigma=12;
Pmin=1e-8;

Pt=0:0.05:5; 
R = (((Pt .* Gt .* Gr .* L.^2 .* sigma) ./ (((4 * %pi)^3) .* Pmin)) ).^(1/4);
subplot(3,1,1);
plot(Pt,R);

G=0:0.05:5;

Pt=2;
R = (((Pt .* G .* L.^2 .* sigma) ./ (((4 * %pi)^3) .* Pmin)) ).^(1/4);
subplot(3,1,2);
plot(G,R);

Gt=70;
Gr=70;
Pmin=1e-12:1e-12:1e-8;
R = (((Pt .* Gt .* Gr .* L.^2 .* sigma) ./ (((4 * %pi)^3) .* Pmin)) ).^(1/4);
subplot(3,1,3);
plot(Pmin,R);

```

## OUTPUT:

<img width="758" height="646" alt="image" src="https://github.com/user-attachments/assets/626f2a29-1345-49bf-ac72-0dc62ba563b7" />

## RESULT:

Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Scilab program.

