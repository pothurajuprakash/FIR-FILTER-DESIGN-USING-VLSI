COMPANY: CODTECH IT SOLUTIONS

NAME: POTHURAJU PRAKASH

INTERN ID: CTIS3676

DOMAIN: VLSIRATION

DURATION: 6 MONTHS

MENTOR: NEELA SANTOSH KUMAR

Description:

The designed **Finite Impulse Response (FIR) filter** implemented using Verilog demonstrates a fundamental digital signal processing structure that is highly suitable for VLSI-based systems. This task focuses on designing, simulating, and analyzing a 4-tap FIR filter, where the filter performs convolution between the input signal and a fixed set of coefficients. The implementation uses a synchronous design approach, ensuring that all operations occur with respect to a clock signal, which is essential for reliable hardware realization.

The FIR filter operates based on the discrete-time convolution equation, where the output is computed as a weighted sum of current and past input samples. In this design, the coefficients are chosen as {1, 2, 3, 4}, which represent the impulse response of the filter. These coefficients determine the behavior of the filter, such as smoothing or amplification of certain signal components. The hardware architecture consists of shift registers, multipliers, and adders. The shift registers store delayed versions of the input signal, effectively maintaining a history of the last four input samples. Each stored sample is multiplied by its corresponding coefficient, and the results are summed to produce the output.

The Verilog code reflects a clean and efficient Register Transfer Level (RTL) implementation. The module includes inputs for clock, reset, and the incoming data signal, along with an output register for the filtered result. On every rising edge of the clock, the input data is shifted through a series of registers. This shifting mechanism is crucial as it aligns past input values with their respective coefficients. The multiplication and accumulation are performed within the same clock cycle, resulting in a single-cycle latency design. The reset signal ensures that all registers and outputs are initialized to zero, providing a known starting condition for simulation and hardware execution.

The simulation results, as observed in the EPWave waveform, clearly validate the correct functionality of the FIR filter. Initially, when the system starts, the output remains zero because the shift registers have not yet been filled with meaningful input data. This phase is known as the transient response. As new input values are applied over time, the filter begins producing valid outputs. For example, when the input sequence progresses from 1 to 8, the output gradually increases as more past samples contribute to the computation. The output values such as 1, 4, 10, 20, 30, and so on, reflect the cumulative weighted sum of current and previous inputs, demonstrating the convolution operation in action.

An important observation from the waveform is the delay between input changes and corresponding output updates. This delay is inherent to FIR filters due to the dependency on previous samples. However, since the design uses a parallel architecture, the computation is completed within one clock cycle after data alignment, making it efficient for high-speed applications. The waveform also shows stable and predictable output transitions, confirming that the design is free from glitches and timing issues.

From a performance perspective, this FIR filter design offers several advantages. It is inherently stable because it does not use feedback, unlike Infinite Impulse Response (IIR) filters. The linear structure also makes it highly suitable for pipelining and parallel processing, which are critical for VLSI implementations. The hardware complexity is moderate, involving four multipliers and three adders, which is acceptable for small-scale designs. Additionally, the use of fixed coefficients simplifies the design and reduces computational overhead.

In conclusion, the FIR filter design successfully meets the objectives of the task by providing a functional and efficient digital filtering solution. The Verilog implementation accurately models the theoretical behavior of the filter, and the simulation results confirm its correctness. This design serves as a strong foundation for more advanced implementations, such as higher-order filters, pipelined architectures, or coefficient optimization techniques, making it highly relevant for real-world VLSI and DSP applications.

OUTPUT:
<img width="1680" height="936" alt="Image" src="https://github.com/user-attachments/assets/5f488fa4-87e6-440a-b02a-d083056d666e" />

