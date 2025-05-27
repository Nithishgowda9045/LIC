# Monostable Multivibrator Using 555 Timer IC

### AIM

 Design, simulate, and analyze a 555 timer IC-based monostable multivibrator circuit that produces a single output pulse lasting 0.5 ms in response to a trigger signal.

### THEORY

* A monostable multivibrator (one-shot) has a single stable state and generates a single output pulse of fixed width when triggered by an external pulse.

* Upon receiving a trigger pulse, the output switches from its stable state for a duration determined by the resistor-capacitor (RC) time constant, then automatically returns to the stable state.

* The output pulse’s leading edge aligns with the trigger, while the pulse width (trailing edge) depends on the RC time constant, allowing control over pulse duration and timing.
  
### working 
* In a 555 timer monostable multivibrator, the output stays in a stable state until triggered, during which the internal transistor and capacitor are effectively "shorted."

* When the voltage at pin 2 falls below a threshold, the output goes high (quasi-stable state), the discharge transistor turns off, and the capacitor begins charging through resistor R1.

* The capacitor charges toward Vcc with a time constant determined by R1 and C1; when its voltage exceeds 2/3 of Vcc, the internal flip-flop resets the output back to the stable low state.

* The output pulse duration (T) is given by the formula: **T = 1.1 × R1 × C1**.

- R = Resistance in ohms
- C = Capacitance in farads
  
## circuit diagram 

![Screenshot 2025-05-26 232958](https://github.com/user-attachments/assets/63647717-6be0-43ed-b148-25eac260dabb)

## calculation 
Here’s a clearer and corrected version of your calculation section:

Given:

* Pulse duration, $T = 0.5 \text{ ms} = 0.5 \times 10^{-3} \text{ s}$
* Capacitance, $C = 0.1 \, \mu\text{F} = 0.1 \times 10^{-6} \text{ F}$

Using the formula:

T = 1.1 \times R \times C

Rearranging for $R$:

$$
R = \frac{T}{1.1 \times C} = \frac{0.5 \times 10^{-3}}{1.1 \times 0.1 \times 10^{-6}} = 4545.45 \, \Omega = 4.55 \, k\Omega
$$

## Output Waveform

![image](https://github.com/user-attachments/assets/4ff3113f-d845-4684-b053-e50b7d29faac)


In the above circuit, the output goes high when the trigger pulse voltage falls below one-third of the supply voltage (Vcc).

## Inference


* The output remains LOW in its stable state until a trigger input is applied.
* When triggered, the output switches to HIGH for a duration determined by the RC time constant.
* For a capacitor value of 1 µF, the calculated resistor value to achieve a 0.5 ms pulse is approximately 454.54 Ω.
* This experiment demonstrates the 555 timer’s use in monostable mode to generate precise time delays.


# Astable multivibrator and monostable multivibrator using 555 timer IC
## Aim
 Generate pulse of width 0.5ms using 555 timer IC.
## Theory


* An astable multivibrator generates a continuous rectangular waveform without needing an external trigger; its output timing is set by two resistors and a capacitor.

* In a differentiator amplifier, the capacitor is placed at the input of the inverting amplifier, and a resistor is used as the feedback element, enabling the circuit to perform voltage differentiation.

* The differentiator’s output voltage changes sharply in response to rapid changes in the input signal, producing spikes, with the RC network controlling its behavior.

* A clipper circuit removes specific parts of a waveform (e.g., negative spikes) and provides a clean trigger signal for the monostable multivibrator.

## Calculation

![IMG-20250526-WA0025 1](https://github.com/user-attachments/assets/4de3de6d-f2e3-4cb2-8de6-db29cbe58dd4)
![IMG-20250526-WA0026 1](https://github.com/user-attachments/assets/270e4059-518e-4af6-b858-1d7dfdfe871b)



## Circuit Diagram:
![image](https://github.com/user-attachments/assets/c2f97c01-2db6-413b-bc8c-eb7d100cdd41)

## Waveform

## case 1

![image](https://github.com/user-attachments/assets/bdcbd7d8-b042-44d8-a02f-16989a367a90)

## case 2

![image](https://github.com/user-attachments/assets/bb0dabe9-f63f-4be1-9e6b-fbbc78f23174)

## case 3

 in case 3 the ton<toff which is not possible in astable Multivibrator , thus we can use an inverter to invert the pulse generated.
 
![image](https://github.com/user-attachments/assets/62330045-4a0a-422d-b977-9699a629bb00)


 ![image](https://github.com/user-attachments/assets/5974cd20-b140-48e9-b307-9e661e8e4906)



## Inference


* Controlling ON and OFF times with a 555 timer isn’t always straightforward. Changing resistor and capacitor values helps, but not every timing combination is achievable with the basic setup.

* The 555 timer has limitations; for example, it can’t directly produce an OFF time longer than the ON time in the astable mode. Using an inverter after the 555 output can help overcome this.

* Very short pulses require precise, low-value resistors and capacitors, highlighting the importance of component accuracy for fast timing.

* Edge detection using a differentiator circuit allows capturing the exact moment a signal changes, which can then trigger a monostable 555 to produce clean, consistent pulses.



* **Case 1:** Using a basic 555 astable circuit, you can control ON and OFF times by selecting appropriate resistor and capacitor values. This works well for moderate timing intervals like 0.2 ms ON and 0.3 ms OFF.

* **Case 2:** When you need very short pulses (e.g., 0.1 ms ON, 0.05 ms OFF), you must use very small resistor and capacitor values. This requires precise components to keep the timing accurate.

* **Case 3:** The standard 555 can’t directly produce an OFF time longer than ON time in astable mode. By adding an inverter stage after the 555 output, you can flip the signal to achieve this timing behavior (e.g., 0.3 ms ON, 0.4 ms OFF).

# Simulation in Virtual Lab Astable Multivibrator


## Procedure:

1. Make the connections as follows: L1 to L12, L14 to L12, L16 to L12, L4 to L9, L8 to L9, L10 to L19, L3 to L17, L11 to L13, L7 to L19, L6 to L13, L2 to L13, L5 to L15, and L18 to L9. (For example, click on 1 and drag to 12, then continue similarly.)
2. Press the **Check Connection** button to verify the wiring.
3. If any connections are incorrect, click on the wrong connection to remove it. Otherwise, click **Delete all connection** to clear all wiring.
4. Initially, set the component values as:

   * Resistance Ra = 3.3 kΩ
   * Resistance Rb = 6.8 kΩ
   * Capacitance C = 0.1 µF
   * Supply voltage Vcc = 5 V
5. Click the **Calculate** button.
6. Record the output voltage displayed.
7. Click the **Plot** button to visualize the output voltage and capacitor voltage.
8. Use the **Clear** button to reset the data.
9. Repeat the experiment with different resistor values.
10. Adjust Ra within the range 1 kΩ to 10 kΩ.
11. Adjust Rb within the range 1 kΩ to 10 kΩ.
12. Change the capacitance C within 0.1 µF to 10 µF.
13. Set the supply voltage Vcc as needed.


## Circuit Diagram
![image](https://github.com/user-attachments/assets/303eba91-66eb-4a6a-9dbc-12f03dbb176c)


## Otuput Waveform
Voltage Across the Capacitor: 
![image](https://github.com/user-attachments/assets/3894310a-e307-4e17-a570-e0371812d10f)


Output Waveform: -
![image](https://github.com/user-attachments/assets/8e9a313b-de9a-41da-a336-7ae45c7bbe49)


## Conclusion


This experiment effectively demonstrated the application of a **555 timer IC configured in monostable mode** to produce an accurate **0.5 ms pulse**, triggered by a well-shaped signal originating from an astable waveform. The results confirm theoretical expectations and highlight how signal conditioning combined with precise timing control can be used in practical scenarios like digital pulse creation, edge detection, and delay-driven automation.








