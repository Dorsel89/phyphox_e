# phyphox:e
## technical capabilities
Both voltage channels and the current measurement channel can be readout individually or successively. The maximum data rate depends on the number of used channels *n* and can be up to $\frac{4.26 Mhz}{n}$.
### voltage measurement
Number of Channels: 2  <br/>
Measurement Range: ±14V <br/>
Resolution (without oversampling): 12bit, ~7mV <br/><br/>
**live mode:** <br/>
measured data will be send continuously to phyphox. <br/>
**oscilloscope mode:** <br/>
After a trigger is fired, 360 measurement points will be stored on the microcontroller and send afterwards to phyphox. A trigger signal is generated as soon as a falling or rising edge above or below a selected voltage threshold is detected.

### current measurement
The ampere meter feature can be used in different gain modes. A low gain enables measurements between ±3A with a resolution of ~1mA. In high gain mode measurements between ±15mA with a resolution of 7μA.

### signal generator
The signal generator is able to generate constant voltages or simple functions (sine, cosine, triangular, sawtooth). <br/>

## phyphox-Experiments
phyphox experiments for the phyphox:e sensorbox can be found  [**here**](https://github.com/Dorsel89/phyphox_e_experiments)

## Configuration
The phyphox:e sensorbox can be configured to get the best possible results adapted to the experiment.<br/>
**voltage measurement:** The user can adjust *Oversampling (OS), Clock-Prescaler (CP) and Conversiontime (CT)* which determines the data rate and resolution.<br/>
```math
Conversiontime [s] = \frac{(CT+12.5) \cdot OS}{CP \cdot 64Mhz}
```
whereby the following values can be used:<br/>
CT = [2.5, 24.5, 92.5, 247.5, 640.5]<br/>
CP = [1, 2, 4, 8]<br/>
OS = [0, 2, 4, 8, 16, 64]<br/>
<!---
**current measurement:** The user can adjust *Gain (G), Oversampling (OS), Clock-Prescaler (CP) and Conversiontime (CT)* which determines the data rate and resolution.<br/>
--->

