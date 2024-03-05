# STM32_Diff_Pressure_Sensor
Read Diff_Pressure Sensor MPXV7007DP module via 12C Serial Communication 

In this Project , I use MPXV7007DP sensor moudule to read Diff Pressure data ...
- No libraries has been used in this project  ( Only Datasheets and schamatics of the moudule and the IC )
- The Sensor have only one register ( Device + Address register in one)
- I use Error handler to test in each step
- I2C has been used to transmit the sensor data
- the pull up resistor has been added according to datasheet values " 4.7kohm "
- The scaling has been done using datasheet formula in 'P' terms
- The Equationes givin are deals with data as voltage and the module provide Digital output to I2C
- The raw data reacived from I2C are digital
- We convert the binary raw data to Vout data to engineer it with another formula to scaling it to get meaningful values
- I did a Multimeter test for the voltage for the diff_pressure reading
- The sensor has two nozzels for P1 and P2 to get thier Avg P (Diff Pressure)
- In the code the union data structure has been used to minapulate recived raw bytes :) "insted and better than shiffting << 8 ..etc"

## Sensor I2C Seiral Communication 
  ![Screenshot 2024-03-04 133404](https://github.com/SumayyahAli/STM32_Diff_Pressure_Sensor/assets/66629518/b51cd8cd-d2b8-435b-829a-f7a1897330f2)

## Values in Scale
<img width="672" alt="image" src="https://github.com/SumayyahAli/STM32_Diff_Pressure_Sensor/assets/66629518/85574c8d-c6be-4444-a636-0048b32791ba">

  ## Results
![Screenshot 2024-03-05 202654](https://github.com/SumayyahAli/STM32_Diff_Pressure_Sensor/assets/66629518/26529f56-0905-46b2-b3bc-7cd1d745f1fa)
<img width="491" alt="Screenshot 2024-03-05 230345" src="https://github.com/SumayyahAli/STM32_Diff_Pressure_Sensor/assets/66629518/47f51a4f-b0cb-43dd-a45c-ccb3912666e9">


