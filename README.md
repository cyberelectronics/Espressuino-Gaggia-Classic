# Espressuino-Gaggia-Classic
**Espressuino – DIY PID, Bluetooth and Preheat Coil on Gaggia Classic**

This is a multifunctional Homemade PID controller ([more info here](http://www.cyberelectronics.org/?p=315)), based on Arduino, connected to my Gaggia Classic espresso machine. If you are interested in a [Raspberry PI project, take a look at here](http://int03.co.uk/blog/project-coffee-espiresso-machine/).
Added LCD and Bluetooth support and some modifications to the software of [BBCC (BareBones Coffee Controller) project by Tim Hirzel](http://playground.arduino.cc/Main/BarebonesPIDForEspresso) and to the [TC4 Android App by Brad](http://code.google.com/p/tc4-shield/downloads/detail?name=TC4%20Android%20App_2_1.zip&can=2&q=) ( Thank you! )

1) Espressuino on Gaggia Classic Test 1: https://youtu.be/K2JoDAo2rsk
2) Flush, Preinfusion and Power Save Mode test: https://youtu.be/HFyjEgGiXRI
3) Temperature stability under Double Shot extraction - 1 : https://youtu.be/e0fRFWRKpoE
4) Temperature stability under Double Shot extraction - 2 : https://youtu.be/jn9fyt5EzsA
5) Automatic Descale Function: https://youtu.be/AEIfKNq4NL8
6) Two different User / Grinder Timer settings: https://youtu.be/gyKxrWVTUnU
7) Volumetric Learn Mode: https://youtu.be/x6J6yWfXBuo
8) AutoBackflush Mode: https://youtu.be/8K8InC9s4Uk
9) Gaggia Classic shot: https://youtu.be/Rh2tWsEHFF8
10) Test Software v3.0: https://youtu.be/T8bxvw2_thg
11) Bluetooth Demo using Galaxy S2: https://youtu.be/Yxo30Qk1L_w
12) Mazzer Major Retention: https://youtu.be/KnSpcn5ZBDM

**Functions:**

- [Bluetooth Support](http://youtu.be/Yxo30Qk1L_w) (HC-06 module, v3.1)
- [Manual or Automatic mode](http://youtu.be/DuDwQY8FdDg)
   * **Manual:**  Start (Stop) the pump manually for max. 99 seconds or Volume in ml (+ Preinfusion)
   * **Automatic:** The pump will start automatically when the temperature reach the set value (Duration in Seconds or (Volume) = Preinfusion + (Shot value) )
- [Time or Volumetric Mode](http://youtu.be/Kw45bSvZ_xM) (TIM / VOL, v3.0)
- Espresso and Steam temperature settings
    * **Espresso temperature:**  min. 60°C  –  max. 110°C
    * **Steam temperature:**      min. 100°C  –  max. 155°C
- [Grinder Timer function](http://youtu.be/_HfGKKBOd9I) (1 > 40 seconds, using SSR,  v1.6)
- [AutoFlush function](http://youtu.be/HFyjEgGiXRI) (v1.8)
- [Power Save Mode](http://youtu.be/HFyjEgGiXRI) (default 30 minutes, v1.8)
- [Automatic Descale Function](http://youtu.be/AEIfKNq4NL8) (default 1 cycle with 15 minutes delay, v1.9)
- [Set 2 different User preferences](http://youtu.be/gyKxrWVTUnU)
- [Set 2 different Grinder Timer parameters](http://youtu.be/gyKxrWVTUnU) (0.1 sec interval, v2.0, Grinder T2 available only when AutoFlush is deactivated, same button used)
- [Automatic Software Pressure Control:](http://youtu.be/ySqIIzoYjFY)    min. 8.0bar – max. 15bar (v1.5)
- [AutoFill -up function](http://youtu.be/-6zXfB7G6B4) for the boiler, while steaming (for longer steam possibility – v1.5)
- 3 Way Electrovalve control (v1.7)
- PID controll for heater (real time P – I – D tuning, using BBCC Plotter)
- Pump controll
- Improved Pressure measurement ( 0 > 15bar, using pressure transducer 0.5V > 4.5V, v1.8 )
- [Improved Preinfusion function](http://youtu.be/HFyjEgGiXRI) (duration settings  0 > 20 cycle, delay must be included)
- 2 buttons (shared) for different Shot duration settings ( Time Mode, 1 > 60 seconds, v3.0 )
- 2 buttons (shared) for different Volume settings ( in Volumetric Mode, 5 > 250ml, v3.0)
- [Learn Mode (Volume)](http://youtu.be/x6J6yWfXBuo) for 2 (shared) different buttons (v3.0)
- [AutoBackflush Mode](http://youtu.be/8K8InC9s4Uk) (for cleaning GroupHead and 3 way valve, v3.0)
- display different Volume Units (number of pulses from volumetric sensor or ml, v3.0)
- display Shot duration in Volumetric Mode (seconds, v3.0)
- Espresso counter (any extraction longer than 15 seconds, will increment this counter v3.0)
- [Delay for Preheat Group Head](http://www.youtube.com/watch?v=DrznD0hoHtQ) ( 0 > 99 minutes – v1.2 )
- Buzzer (Sound ON / OFF from menu – v1.1 to v1.4)
- Backlight Control (not implemented in software, removed from v3.0 due to HW changes)

**Protections:**   

- short or unconnected thermistor pins ( “Terr” message on the display, push buttons and SSRs  are blocked until problem solved and system restarted).
- in Manual and Volumetric Mode, after 99 seconds the pump will turn Off automatically.
- Power Save Mode, will Turn Off the Heater after a preset period (default 30 minutes)

**Documentation for connecting to Gaggia Classic :**
- For SW v3.0 and HW v1.2 (or above):
   - [Controller PID Espressuino Doc_v1.6 ( Romanian )]()
   - [Controller PID Espressuino Doc_v1.6 ( Hungarian )]()
- For older SW and HW:
   - [Controller PID Espressuino Doc_v1.5 ( Romanian )]()
   - [Controller PID Espressuino Doc_v1.5 ( Hungarian )]()
- Circuit Diagram :
  - Espressuino v1.2  —  Changelog
  - Espressuino v1.1  
- Arduino and Android (for v3.1) Source Code :
  - Espressuino v3.1  — BT Support + Excel File
  - Espressuino v3.0  — Changelog
  - Espressuino v2.0
  - Espressuino v1.9
  - Espressuino v1.8
  - Espressuino v1.7   

**P4 Connector pinout:**

1. Power Supply Input  (+7V to +12V)
2. GND ( – Common Ground, connected to DB9 Shield)
3. Vcc OUT (+5V Common)
4. SSR Heater (to SSR LED – input)
5. Vcc OUT (+5V NC for DB9 connector)
6. SSR Pump (to SSR LED – input)
7. Vcc OUT (+5V NC for DB9)
8. Temp. sensor input (to thermistor)
9. Vcc OUT (+5V NC for DB9)
10. Pressure transducer input (to pressure transducer output (0.5V to 4.5V))

**P2 Connector pinout:**

1. GND (NC for DB9)
2. AREF (NC for DB9)
3. ADC6 (NC for DB9)
4. Volumetric Sensor (to pulse output)
5. SSR Grinder (to SSR LED + input)
6. SSR EValve (to SSR LED + input)
7. RX (HC-06 Bluetooth TX)
8. TX (HC-06 Bluetooth RX)

**Push Button functions in firmware v3.0 or higher :**

- S1 – ” SET // AV2/AT2 ” – enter Settings Mode and Set Value // AutoVolume2/Time2 Mode
- S2 – ” ST / SP / – // AV1/AT1″ – Start / Stop / Decrement // AutoVolume1/Time1 Mode
- S3 – ” TIM / VOL / + // GRD2\AFL” – Time/Volume/Incr. // Grinder2 or AutoFlush Mode
- S4 – ” STM / ESP // GRD1″ – Steam / Espresso // Grinder1 Mode
// – available when longpress

**Other functions available at startup (keep pressed then turn ON the espresso machine):**

- S1 – “Bckf” – Start AutoBackflush Mode
- S2 – “Dscl” – Start Automatic Descale Mode
- S3 – “User2” – Load User 2 preferences
- S4 – “User1” – Load User 1 preferences
- S1 AND S2 – “Learn” – Start Volume Learn Mode
- S3 AND S4 – “Reset” – Reset Espresso Counter to 0

**Push Buttons functions in firmware below < v3.0 :**

- S1 – ” SET ” – enter Settings Mode and Set Value
- S2 – ” ST / SP / – ” – Start (Pump) / Stop (Pump) / Decrement
- S3 – ” A / M / + ” – Auto (Mode) / Manual (Mode) / Increment
- S4 – ” STM / ESP ” – Steam (Mode) / Espresso (Mode)

  
