**NOTE: Always use the significant figures of the least precise piece of data given**
Every measurement will have a certain level of uncertainty.
$$x \pm \Delta x $$
$$\text{Measured/Calculated Value} = \text{Absolute Uncertainty}$$
##### Analogue Measuring
When using analogue measuring device, (eg. a ruler) the uncertainty is normally half of the instrument's resolution (the smallest increment). 
However, if using something like a ruler, you measure the start and the end, both of which has uncertainties, therefore for a ruler, or example, the uncertainty 
- eg. in a ruler, usually the resolution is 1mm, therefore the uncertainty is 0.5mm for one point therefore .
- so if you measure something as about 32.35cm, it would be expressed as 32.35cm ± 0.05cm
- the ±0.05 is called the 'Absolute Uncertainty'
##### Digital Measuring
For a digital instrument, the uncertainty is usually written, if not the resolution is used.
- eg. if a balance's resolution is 0.1g, and we don't know, if we measure 23.6g it would be 23.6g ± 0.1g

## Calculating Uncertainties
Uncertainty across repeated measurements "nums" = 
$$mean(\text{nums}) \pm \frac{range(\text{nums})}{2}$$
make sure that the mean of nums is the **same significant figure** as the Absolute Uncertainty, so if the mean is 68.78g and the Absolute Uncertainty is 0.6g, it will be $$68.8g\pm0.6g$$

## Accuracy vs Precision
I always get these messed up
#### Accuracy
- 'How close you are to the real value'
- how close the mean/final result is to final value
- does not need values to be close to each other
#### Precision
- 'How close the measured values are to each other' 
- low uncertainty
- does not need to be close to real value

## Fractional Uncertainty
$$\text{let}\,l = 32.35cm \pm 0.05cm$$
$$\text{Absolute Uncertainty} = \Delta l = 0.05cm$$
$$\text{Fractional Uncertainty} = \frac{\Delta l}{l} = \frac{0.05}{32.35}cm=0.0015cm$$
$$\text{Percentage Uncertainty} = \frac{\Delta l}{l} = \frac{0.05}{32.35}cm=0.15\%$$
NOTE: Fractional Uncertainty CANNOT be expressed in the form of a FRACTION, you can only use DECIMALS or maybe PERCENTAGES.
## Propagating Uncertainties
### Adding and Subtracting
Just add the uncertainties togather.
$$\Delta(A\pm B) = \Delta A + \Delta B$$
eg. $$(50 \pm 0.1g) - (15\pm 0.1g) = 35 \pm 0.2g $$

## Multiplying and Dividing
Calculate Fractional uncertainty of each individual variable
Sum the fractional uncertainties together, then you can calculate the absolute uncertainty using the sum
$$\frac{\Delta (AB)}{AB} =  \frac{\Delta A}{A} + \frac{\Delta B}{B}$$

eg.
$$ V = 5.35\pm 0.02v , I = 25.3\pm 0.8 mA$$
$$R = 5.35/0.0253 = 211.5$$
$$\frac{\Delta R}{R} = \frac{\Delta V}{V} + \frac{\Delta I}{I}$$
$$\frac{\Delta R}{211.5} = \frac{0.02}{5.35} +\frac{0.8}{25.3}$$
$$\Delta R = 7.478\ohm$$
$$R = 211 \pm 7\ohm (\text{1 s.f})$$
## Constants
what if we have a constant? like π? or even 2?
There is no effect on the **Fractional Uncertainty**, but the Absolute Uncertainty might change

$$n(A\pm\Delta A) = n(A) \pm n(\Delta A)$$
eg. if you measure 10 rotations of smth:
you get $$11.2\pm 0.3s$$
$$\frac{11.2\pm 0.3}{10} =\frac{11.2}{10}\pm \frac{0.3}{10}s = 1.12 \pm 0.03s$$
## Graphs
### Error Bars
When you plot a data point on your graph, you must show the range of values between which the point could be. To do that you use error bars.

![[error_bars.svg]]
