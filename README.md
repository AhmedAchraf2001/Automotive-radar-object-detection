# Automotive-radar-object-detection
Estimate speed, distance and angle of objects Based on Range Doppler spectrum and Range azimuth spectrum which obtained after Fourier transformation of radar signal.
</br>

> [!NOTE]  
> Full implementation is kept private, But you can look up at data preprocessing, visualization and model preformance attached in [Source/automotive-radar-object-detection.ipynb](https://github.com/AhmedAchraf2001/Automotive-radar-object-detection/blob/main/Source/automotive-radar-object-detection.ipynb) file.



### ADAS - Advanced Driver Assistance Systems to obtain information from the environment. These systems are based on 
1.	Camera 2.	Lidar 3.	Radar 4.	Ultrasound
 

### Why radar compared to cameras and lidars?
The radar offers additional insights alongside the lidar and camera. 
**Radar operates effectively in various weather and lighting conditions**, such as darkness, fog, or snow.
Radars are precisely measuring **distance, speed, and the arrival angle** of surrounding objects. 
Radars outperform other methods in speed estimation while **requiring lower computational and memory cost.**


</br>



<img align="center" alt="example" src="Docs/images/httpsgithub.comZhangAoCanadaRADDetblobmainimagestestset_samples.png.png">

<h6 align="center"> 
 
 [image](https://github.com/ZhangAoCanada/RADDet/blob/main/images/testset_samples.png) 

</h6>

### Range-Doppler spectrum in first image
**Description :** the spectrum is obtained after two successive Fourier transforms on radar signal.
represents the vehicle's environment based on the 
  -	Distance 
  -	Speed of each target.</br>


### Range-azimuth spectrum in second image
**Description :** the spectrum is obtained after three successive Fourier transforms on radar signal.
represents the vehicle's environment based on the
  -	Distance
  -	Angle of arrival of each target.</br>



</br>

## Estimation of distance, speed, and angle from spectra
By a bounding box on spectra these parameters could be estimated:
- **Extract the position (x, y) of bounding box**
  -	**x = range**
  -	**y = speed or angle**

then estimate those parameter using x, y and radar resoluation, equations attached below.


</br>
</br>

## Progress
### [2024-04-24] Update model archetic. use pytorch improve accuracy to 100% on validation set, Check [Source/training metrics.json](https://github.com/AhmedAchraf2001/Automotive-radar-object-detection/blob/main/Source/training%20metrics.json).
### [2024-04-15] Download tiny portion of data, preprocessing and building model 
### [2024-04-06] search about more resources about how data collected and built, read papers attached [here]()
### [2024-04-02] Plan to project, find data 

</br>
</br>

## My Contribuation
RNN-CNN Archeticheture has implemented to track the object on radar to specify many parameter like object is moving towards or away from car and detect object on spectra easily wheter it diffcult to specify where is the object using only on frame so i will implement rnn cnn model like human activity recognation.

</br>
</br>

## TO DO
- [x] Use detectron2 to build various models.
- [ ] Implement 3D object detector on Range-Doppler-Angle Tensor.
- [ ] Study this [article](https://www.plextek.com/a-programmers-introduction-to-processing-imaging-radar-data/) well, to implement object detector on cartesian space.

## References
Ao Zhang1, Farzan Erlik Nowruzi1, Robert Laganiere, 'RADDet: Range-Azimuth-Doppler based Radar Object Detection for Dynamic Road Users' vol. 39, no. 10, 2020. 
[https://doi.org/10.48550/arXiv.2105.00363](https://arxiv.org/abs/2105.00363)

