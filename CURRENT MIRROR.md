# **CURRENT MIRROR EXPERIMENT**

## PART A
Aim : Design and Analyze Current mirror circuit as active load in amplifier circuit.

Given :  Vdd=1.8V, P<=1 mW, Av>-10 V/V.

### perform
 - DC analysis 
 - transient analysis
 - AC analysis 
 - Required parameter

## circuit Diagram:

![image](https://github.com/user-attachments/assets/efbf9c25-9402-4c19-b28b-53f7f284ae52)

CALCULATIONs:
Drain current equation is given by:

I<sub>D</sub> = (1/2)μnC<sub>ox</sub>(W/L)(VGS - Vth)^2\
I<sub>Total</sub> = P / V<sub>DD</sub>\
I<sub>Total</sub> = I<sub>ref</sub> + I<sub>x</sub>\
For 1:1 ratio I<sub>ref</sub> = I<sub>x</sub>\
I<sub>ref</sub>(2) = I<sub>Total</sub>\
I<sub>ref</sub> = I<sub>Total</sub>/2\
I<sub>Total</sub> = 1 mW/1.8 V\
I<sub>Total</sub> = 0.555 mA\
I<sub>ref</sub> = 0.555 m/2\
Therefore, I<sub>ref</sub> = 0.2778 mA.

# For 1:1 Ratio :
## DC Analysis:

![cm1](https://github.com/user-attachments/assets/21795a69-cbb8-41b7-ba4a-4f8058ac8931)

same for M1, M2, M3.

![cm1lw](https://github.com/user-attachments/assets/9a1f5414-3757-48da-b3f5-3afbc4f8e7ff)

![cm1dc](https://github.com/user-attachments/assets/99668227-94ab-4cd3-8738-cf082d3a0fbf)

## Transient Analysis :

- Change the input voltage to sine and change the amplitude to 5 mV , frequency to 1 kHz
- Select transient analysis and choose 10 ms for stop time.
- Click on ok.
  
![image](https://github.com/user-attachments/assets/fc1ffcf1-e8e9-44ab-845b-1438e26b4f23)

![image](https://github.com/user-attachments/assets/04c6aa67-3384-458e-9599-65a3038892a1)

The expected gain was greater than or equal to 10 V/V and the obtained gain is 13.5 V/V.

## AC Analysis :

- Change the Vin to AC and set AC amplitude to 1.
- Click on run simulation and choose AC analysis.
- Select type of sweep to decade , frequency range to 0.1 - 1 THz.
- Click on Ok.

  ![image](https://github.com/user-attachments/assets/6fc8a12b-7283-4764-ab6c-aeae89325547)

  ![Screenshot 2025-03-22 155758](https://github.com/user-attachments/assets/e36365ee-5261-493a-b19f-1d09ead1ee02)

|Parameter      |Theory value  | Practical value |
|---------------|--------------|-----------------|
|Av(in dB)      | 20dB         | 22.16dB         |
|Av(in V/V)     | 10           | 13.5            |

## For 1:2 Ratio :

## DC Analysis :

![image](https://github.com/user-attachments/assets/16b08607-482d-4d02-8da4-8ad7f25379e4)

![cm2 ](https://github.com/user-attachments/assets/875f38dd-d733-4ecf-84a9-0394d950b778)

![image](https://github.com/user-attachments/assets/e639b286-84ac-4a95-8bae-665e6c362709)

## Transient Analysis :

![image](https://github.com/user-attachments/assets/109ee783-8643-42ab-ae30-68c27e58717c)


![image](https://github.com/user-attachments/assets/9e1b7022-65ee-48ff-866c-5d214c72d96b)


The expected gain was greater than or equal to 10 V/V and the obtained gain is 12.1 V/V.

## AC Analysis :

![image](https://github.com/user-attachments/assets/dc1ca419-f975-4354-9beb-719d9b64841e)

![Screenshot 2025-03-22 162439](https://github.com/user-attachments/assets/344ca781-50ca-42e9-ba6b-70a3882a5dcc)


|Parameter      |Theory value  | Practical value |
|---------------|--------------|-----------------|
|Av(in dB)      | 20dB         | 24.6dB          |
|Av(in V/V)     | 10           | 12.1         |

##  For 1:3 Ratio#

## DC Analysis :

![cm3](https://github.com/user-attachments/assets/3ab0e50e-6f22-48e6-9dbf-ab3b6da0b614)

![cm3dc](https://github.com/user-attachments/assets/57ac7d3f-b80a-493e-8183-45ab45d82733)

## Transient Analysis :


![image](https://github.com/user-attachments/assets/052fb194-9467-4f1c-ae87-50dde51bd1ec)

The expected gain was greater than or equal to 10 V/V and the obtained gain is 13.167 V/V.

## AC Analysis :

![image](https://github.com/user-attachments/assets/7939bf4e-d11b-4964-8f94-75de8edcf727)


## PART B

Aim: Design the differential amplifier using the same design specification as Experiment-3.
Perform DC analysis,trasient and AC analysis.

### DC Analysis:

![image](https://github.com/user-attachments/assets/56c622ed-0860-4a7a-9cb7-f3974e9d1530)

![image](https://github.com/user-attachments/assets/9697229e-1a1a-4a4c-ba2a-5f339fbaccd3)

## Transient Analysis :

![image](https://github.com/user-attachments/assets/310c0e83-2375-4a25-9b68-6b8cdfe01c00)

![image](https://github.com/user-attachments/assets/87239f42-871d-4397-983a-0846c46a296d)

## AC Analysis:

![image](https://github.com/user-attachments/assets/5e734117-f0f4-4fcf-a7dd-2ce8648f617f)


![a5](https://github.com/user-attachments/assets/6f85826b-afc4-4928-956d-1dadf4af64e4)

# Inference :
The circuit functions as a differential amplifier, utilizing a current mirror to control the output (Vout), which responds to the voltage difference between V2 and V3. 
The PMOS current mirror (M1-M2) ensures stable current replication. This design is beneficial for analog signal processing and amplification,
as it incorporates an NMOS differential pair (M3-M4) for the amplification stage.




