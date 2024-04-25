# Automotive-radar-object-detection
Estimate speed, distance and angle of objects Based on Range Doppler spectrum and Range azimuth spectrum which obtained after Fourier transformation of radar signal.
</br>

> [!NOTE]  
> Full implementation is kept private.



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

### Range-Doppler spectrum
**Description :** the spectrum is obtained after two successive Fourier transforms on radar signal.
represents the vehicle's environment based on the 
  -	Distance 
  -	Speed of each target.

### Range-azimuth spectrum
**Description :** the spectrum is obtained after three successive Fourier transforms on radar signal.
represents the vehicle's environment based on the
  -	Distance
  -	Angle of arrival of each target. 

</br>

## Estimation of distance, speed, and angle from spectra
By a bounding box on spectra these parameters could be estimated:
- **Extract the position (x, y) of bounding box**
  -	**x = range**
  -	**y = speed or angle**

then estimate those parameter using x, y and radar resoluation, equations attached below.





## Progress
### [2024-04-24] Update model archetic. use pytorch improve accuracy to 100% on validation
### [2024-04-15] Download tiny portion of data, preprocessing and building model 
### [2024-04-06] search about more resources about how data collected and built, read papers attached [here]()
### [2024-04-02] Plan to project, find data 


## My Contribuation
RNN-CNN Archeticheture has implemented to track the object on radar to specify many parameter like object is moving towards or away from car and detect object on spectra easily wheter it diffcult to specify where is the object using only on frame so i will implement rnn cnn model like human activity recognation.
</br>

## References
Ao Zhang1, Farzan Erlik Nowruzi1, Robert Laganiere, 'RADDet: Range-Azimuth-Doppler based Radar Object Detection for Dynamic Road Users' vol. 39, no. 10, 2020. 
[https://doi.org/10.48550/arXiv.2105.00363](https://arxiv.org/abs/2105.00363)

