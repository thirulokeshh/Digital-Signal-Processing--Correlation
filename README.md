# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2012.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 
~~~
clc;            % Clear screen
clear all;      % Clear workspace
close all;      % Close all figure windows

%% INPUT SIGNAL-1
a = input('Enter the starting index for x(n): ');
x = input('Enter the x(n) sequence: ');

n = a : (a + length(x) - 1);

figure(1)
stem(n, x)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-1')

%% INPUT SIGNAL-2
b = input('Enter the starting index for y(n): ');
y = input('Enter the y(n) sequence: ');
m = input('Enter the ending y(n): ');    % (User-defined but not used in original meaning)

n1 = b : (b + length(y) - 1);

figure(2)
stem(n1, y)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-2')

%% DISCRETE AUTO-CORRELATED SIGNAL
out1 = xcorr(x, x);
n2 = (a - m) : (a - m + length(out1) - 1);

figure(3)
stem(n2, out1)
xlabel('Time')
ylabel('Amplitude')
title('Discrete Auto-Correlated Waveform')

%% DISCRETE CROSS-CORRELATED SIGNAL
out2 = xcorr(x, y);
n3 = (a - m) : (a - m + length(out2) - 1);

figure(4)
stem(n3, out2)
xlabel('Time')
ylabel('Amplitude')
title('Discrete Cross-Correlated Waveform')
~~~

OUTPUT:

## OUTPUT:
<img width="692" height="623" alt="Screenshot 2025-11-18 221522" src="https://github.com/user-attachments/assets/69f7a3cb-44d8-44e1-b4a3-e4042e92aa8f" />
<img width="699" height="614" alt="Screenshot 2025-11-18 221505" src="https://github.com/user-attachments/assets/873c4757-b906-4f5a-bc33-a4d8f6882689" />
<img width="696" height="625" alt="Screenshot 2025-11-18 221436" src="https://github.com/user-attachments/assets/63128ccf-648a-4ffb-a8c5-7b01fa4d974a" />

<img width="700" height="621" alt="Screenshot 2025-11-18 221552" src="https://github.com/user-attachments/assets/76e78c22-3315-460b-99e4-e7c1d2ab4cec" />

## RESULT:
![WhatsApp Image 2025-11-27 at 22 14 31_58c5dcf6](https://github.com/user-attachments/assets/b1e9aa1e-15e3-42fc-ac26-73968add49bf)


