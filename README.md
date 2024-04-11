# Automotive-radar-object-detection
Estimate speed, distance and angle of objects Based on Range Doppler spectrum and Range azimuth spectrum which obtained after Fourier transformation of radar signal.

</br>
</br>

### ADAS - Advanced Driver Assistance Systems to obtain information from the environment. These systems are based on 
1.	Camera
2.	Lidar
3.	Radar
4.	Ultrasound


### Why radar compared to cameras and lidars?
The radar offers additional insights alongside the lidar and camera. 
**Radar operates effectively in various weather and lighting conditions**, such as darkness, fog, or snow.
Radars are precisely measuring **distance, speed, and the arrival angle** of surrounding objects. 
Radars outperform other methods in speed estimation while **requiring lower computational and memory cost.**


</br>

•	Range-Doppler spectrum
range-Doppler spectrum is obtained after two successive Fourier transforms on the data received by the radar.
represents the vehicle's environment based on the 
•	Distance 
•	Speed 
of each target.

In the figure below, 2 pedestrians are present in the radar field at 
22m and 26m respectively and at a speed of 1 m/s and -1 m/s respectively. 
A positive speed means the target is getting closer and a negative speed otherwise.



•	Range-azimuth spectrum

The range-azimuth spectrum is obtained after three successive Fourier transforms on the data received by the radar. 
It allows a representation of the vehicle's environment based on the 
•	Distance
•	Angle of arrival
of each target. 
In the figure below (same sequence as previously), 2 pedestrians are present in the radar field at 22m and 26m respectively and at angles of 17° and -5° relative to the radar respectively.

•	Estimation of distance, speed, and angle from spectra

Based on the distance, speed, and angle resolution of the radar
It is possible to estimate these parameters for a given target directly on the spectrum. 
By a bounding box these parameters could be estimated:
	Extract the position (x, y) of the maximum value in a bounding box 
o	x = range
o	y = speed or angle

Let Rres, Dres, and Ares respectively be the resolution in distance, speed, and angle. 
1px = Rres, Dres or Ares.

SO:
Distance = Rres*x
Velocity = (64/2-y) * Dre           (on the range-Doppler spectrum of size 256x64)
Angle = (256/2-y) * Ares            (on the range-Azimuth spectrum of size 256x256)



## Algorithm
**Description :** 


## My Contribuation



</br>

## References
Ao Zhang1, Farzan Erlik Nowruzi1, Robert Laganiere, 'RADDet: Range-Azimuth-Doppler based Radar Object Detection for Dynamic Road Users' vol. 39, no. 10, 2020. 
[https://doi.org/10.48550/arXiv.2105.00363](https://arxiv.org/abs/2105.00363)

