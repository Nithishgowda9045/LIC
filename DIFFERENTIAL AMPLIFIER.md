# EXPERIMENT NO-3

## Aim:
Design and Analyze the differential amplifier circuit for the following specifcations and Perform DC analysis,Transient Analysis,Frequency response and extract parmeter
Vdd=2.2v , p<=2.2mv , Vicm=1.2v, Vocm=1.25v , Vp=0.4v

#### Differential Amplifier:
differential amplifiers consist of two transistors M1 and M2, whose sources are joined together. If two transistor are connected to the different voltage input then there current across M1 and M2 are different due to gate voltage.If in case the voltage supply at gate terminal is same then the current through the M1 and M2 are same.That it is called Common Mode input voltage DF. the MOSFET should not go to the Triode region. It should be in Saturation Region.


![WhatsApp Image 2025-03-03 at 21 39 40_2da0c6ee](https://github.com/user-attachments/assets/3e57e557-4608-4d2c-8b6c-e63036b2573e)


## circuit 1:
![Screenshot 2025-03-03 192533](https://github.com/user-attachments/assets/b482c24b-09c1-4771-aa54-161bfe5fb5be)

## Procedure:

1.Open the LTspice software, merge the library file for getting accurate values of NMOS.

2.Select the components which are needed to us like for circuit 1 we need 1.9k & 0.4k resistor,2 CMOSN, three voltage sources(1.2v,2.2v),ground from the components list.

3.Lets do the DC Analysis first  we get .op so aftef changing length and width it we will get the values of it, thet will displayed.

4.After that lets take Transient analysis and set stop time into  5m cycle so in input and output waveforms in 5 complete cycle, so here we get and seperate and combined waveforms.

5.For AC analysis, we should do some changes like converting DC SOURCE to sine waveform (1.2,0.05,1k),after that select the AC simulation from the given options of simulation after giving values of (Decade,20,0.1,1t). So we will get a output after placing node to output waveform .

## DC ANALYSIS:

![image](https://github.com/user-attachments/assets/07bbe991-2a96-486c-b2f9-c85e31a18147)

we have to vary the width and length of both the mosfet to get desired value.
we got L=180nm and W=6.4u 

![image](https://github.com/user-attachments/assets/a36c069e-9561-44f2-8a21-cb5efd204db8)

Here in dc analysis we got the vout as expected and id1 and id2 we got the same 

Id1 = 0.49mA

Id2 = 0.49mA

Vocm = 1.25V

vocm2 = 1.25 V

# Transient analysis:

![cr1 wave](https://github.com/user-attachments/assets/6d3ca542-dc6e-4d6b-bf96-dfa6f9c4fe8e)

Vout = 1.32 - 1.18 V
   Vin = 1.2 - 1.15 V​
   Gain = Vout / Vin
 = (1.32 - 1.18) / (1.25 - 1.15)
 = 1.4 
 Gain in dB = 20 * log (1.4)
  = 2.92 dB

# AC analysis:

TO perform AC analysis we have to  edit simulation command


![image](https://github.com/user-attachments/assets/dc2837e9-e4ed-4b65-9d6e-72631a9e1c03)


![cr1 ac](https://github.com/user-attachments/assets/849dd9c9-5d52-40c4-87a6-8c2595a9b90b)


# Circuit-2:



![Screenshot 2025-03-03 183413](https://github.com/user-attachments/assets/6ae5a8d0-0934-4fba-afa1-a6fa7bfc714d)

# DC analysis:

![image](https://github.com/user-attachments/assets/70cb5d3a-cbd1-4581-9900-61cfd7bcbe61)

![image](https://github.com/user-attachments/assets/f06f81b7-4898-45be-a861-393599695b97)

# Trasient analysis:
 ![Screenshot 2025-03-02 130322](https://github.com/user-attachments/assets/9ae919cf-f16c-4df7-ac50-e22cc623c2f2)

 Vocm = 1.44 -1.04
  Vin = 1.2 - 1.15 V
  Gain = vocm / Vin
 = (1.44 - 1.04) / (1.2 - 1.15)
 = 4
Gain in dB: 20 log (4)
 =12.04

 
 # AC analysis:

  <img width="959" alt="image" src="https://github.com/user-attachments/assets/75f328de-9ee0-4011-ab77-b6078fc720c0" />
  

  # Circuit-3:

  
  Now replace the R3 resister with a Mosfet:
    Given vp=0.4v and wkt vt=0.36v we got  0.76v (gate voltage)
 

![image](https://github.com/user-attachments/assets/71e22afb-f8af-47c9-8ef8-a9fa0c4f6720)

# DC analysis:

![image](https://github.com/user-attachments/assets/a91e4d1c-d7da-4b8a-95e0-ae5f20408821)

 ![image](https://github.com/user-attachments/assets/81c43495-d8fa-4ad6-9362-3f147be90533)

 # Transient analysis:

 AC amplitude 1 for one mosfet and 0 gor other mosfet 
  ![Screenshot 2025-03-02 123127](https://github.com/user-attachments/assets/431d7132-e2fb-4870-b625-a5334a2e9a9d)

# AC analysis:

<img width="959" alt="image" src="https://github.com/user-attachments/assets/56a10839-f8b8-40e4-8c2f-a01d9dda29f3" />

# DC sweep :

 we have to  edit simulation command

![image](https://github.com/user-attachments/assets/733f9b22-3036-4720-986a-49a226f99cc9)

<img width="959" alt="image" src="https://github.com/user-attachments/assets/15f102e5-5ba4-40c5-965c-3c6d8668217b" />

# Result:
  -circuit 1:
     The DC analysis shows that the MOSFETs operate in saturation with equal drain currents . 
     The transient response confirms proper differential .  
     The AC analysis moderate gain and common-mode rejection. 
 -circuit 2:
     Replacing the resistor with a current source improves bias stability.  
     The transient response is more stable.  
     The AC analysis shows increased gain and bandwidth compared to Circuit-1.  
-Circuit-3:  
     The DC analysis, the MOSFET-based current source regulates the tail current effectively.  
     The transient response maintains signal accuracy with improved performance.  
     The AC analysis shows higher gain and bandwidth.  
     The DC sweep analysis validates expected output variations.  

# Inference:  

 Resistor: High bandwidth, low gain, low CMRR.  
 Current source: High gain, high CMRR, slightly lower bandwidth.  
 NMOS (CMOSN): Highest gain.  

 Best Configuration to need:  
1. High bandwidth → Resistor  
2. Maximum gain→ NMOS (CMOSN)  
3. Better CMRR→ Current source or NMOS (CMOSN)






  


