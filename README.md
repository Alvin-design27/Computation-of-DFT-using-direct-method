# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
<br>
clc;

clear;

clf;

xn = [1,2,3,4,4,3,2,1];

N = length(xn);

n = 0:N-1;

j = %i;

Xk = zeros(1, N);

// Direct DFT calculation

for k = 0:N-1

    for r = 0:N-1
    
        Xk(k+1) = Xk(k+1) + ...
        
            xn(r+1)*exp(-j*2*%pi*k*r/N);
    end
    
end

disp("DFT output:");

disp(Xk);

K = 0:N-1;

magnitude = abs(Xk);

phase = atan(imag(Xk), real(Xk));

subplot(3,1,1);

plot2d3(n, xn);

xtitle("Input Sequence", "n", "x(n)");

subplot(3,1,2);

plot2d3(K, magnitude);

xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(3,1,3);

plot2d3(K, phase);

xtitle("Phase Spectrum", "k", "Phase (radians)")
<br>
<br>
<br>
<br>
<br>
### CALCULATIONS:
<img width="1080" height="730" alt="image" src="https://github.com/user-attachments/assets/fb37113c-04f9-4074-b666-2642a71f98c1" />
<img width="729" height="1280" alt="image" src="https://github.com/user-attachments/assets/a89986ab-5a32-4e1c-8f6f-1fbff89beb98" />
<img width="839" height="1280" alt="image" src="https://github.com/user-attachments/assets/b37c2a40-8d1f-4059-93da-a17665ab5ece" />
<img width="855" height="1280" alt="image" src="https://github.com/user-attachments/assets/0164c7d8-7df1-4f9c-83da-3c38e41d0cc5" />
<img width="767" height="1280" alt="image" src="https://github.com/user-attachments/assets/7f22ac8c-e97e-4bea-beaa-b1923cbe8df4" />
<img width="973" height="1280" alt="image" src="https://github.com/user-attachments/assets/358fecb6-edc8-4f78-af23-c5a304dbc67e" />
<br>
<br>
<br>
<br>
<br>
### SAMPLE OUTPUT:
<br>
<img width="1280" height="1087" alt="image" src="https://github.com/user-attachments/assets/1b90dbfd-552e-4aee-aa7c-bd22b8000e3b" />

<br>
<br>
<br>



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

