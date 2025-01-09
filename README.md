# TASK-4-DIGITAL-FILTER-DESIGN
**COMPANY** CODETECH IT SOLUTIONS

**NAME** PRADNYA BHAGWAN PAWAR

**INTERN ID** CT08FVW

**DOMAIN** VLSI

**BATCH DURATION** December 25th, 2024 to January 25th, 2025.

**MENTOR NAME** NEELA SANTHOSH

# ENTER DESCRIPTION OF THE TASK
1. Overview:
The Verilog implementation describes a 4-tap Finite Impulse Response (FIR) filter, which processes discrete-time input signals to produce a filtered output. The filter coefficients are pre-defined and determine the filter's frequency response.

2. Key Features:
Filter Structure:

The FIR filter uses a direct form structure.


Shift Register:

A 4-stage shift register stores the last four input samples.
Each new input shifts the previous samples to the next stage, preserving the order.
Pipeline Design:

The output is computed in a single clock cycle once the pipeline is filled.
The initial latency equals the filter length (4 clock cycles).
Input and Output:

Input (x_in): Signed 16-bit input samples.
Output (y_out): Signed 16-bit filtered output.
3. Simulation Behavior:
Reset Operation:

When reset is active, the shift register and output are set to zero.
Filtering Process:

On every clock cycle:
The input sample is shifted into the register.
The weighted sum of the stored samples is computed using the filter coefficients.
The computed sum is assigned to y_out.

4. Frequency Response:
The symmetric coefficients result in a linear phase low-pass filter:
Passband: Low frequencies are passed with minimal attenuation.
Stopband: High frequencies are attenuated.
Transition Band: The slope of the attenuation is determined by the number of taps (4 in this case).
5. Design Performance:
Advantages:

Stable and straightforward due to the FIR structure (no feedback).
Linear phase response preserves the shape of the input waveform.
Limitations:

Fixed coefficients limit flexibility for dynamic frequency filtering.
Longer filters (more taps) may be needed for sharper frequency cutoff.
Applications:
This FIR filter design is ideal for:
Smoothing noisy signals.
Low-pass filtering for audio, communication, or sensor signals.
# OUTPUT
[TASK 4.docx](https://github.com/user-attachments/files/18357125/TASK.4.docx)
