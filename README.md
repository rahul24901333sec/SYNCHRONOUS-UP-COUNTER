
NAME:RAHUL.R

REGISTRATION NO:212224050034


**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 BIT SYNCHRONOUS UP COUNTER**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**PROCEDURE**

1. Initialize the shift register to a known state (e.g., all zeros).
2. Input a bit serially into the shift register.
3. Shift the contents of the register to one position to the right (or left).
4. Output the shifted bit from the last stage of the register.
5. Repeat steps 2-4 for each bit you want to input and shift.


**PROGRAM**

![Screenshot (82)](https://github.com/user-attachments/assets/9f6d5572-89c9-4b0e-952a-e000db4a9619)


**RTL LOGIC UP COUNTER**

![Screenshot (83)](https://github.com/user-attachments/assets/0c2dc8f2-7803-475f-9567-9d13652d1ad4)


**TIMING DIAGRAM FOR IP COUNTER**

![Screenshot (84)](https://github.com/user-attachments/assets/11260a46-de84-46cc-b3ad-ec7d4257ae05)

**TRUTH TABLE**

![Screenshot (85)](https://github.com/user-attachments/assets/1ea46e34-1695-4d49-a1a6-671dffc8e70a)

**RESULTS**

Hence a 4 bit synchronous up counter is implemented successfully
