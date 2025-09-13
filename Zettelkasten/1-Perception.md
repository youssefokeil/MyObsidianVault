# Perception Sensors
## Sensors:
Sensors consist of a transducer and an electronic circuit. 
1. **Transducer:** is defined as any device that converts a signal from one form to another. A lot of times we refer to "Electrical Transducers",  which converts physical quantities into electrical outputs or signals. It's usually electro-mechanical, electronic or electric. Transducers are the things that interact directly with the environment.
2. **Electrical circuit:** takes the electrical signal from the sensor, does some signal conditioning & then turns it to a digital signal.
### External Perception Sensors:
they acquire data from the vehicle's/robot's environment, then it is transformed into meaningful information such as occupancy grid map, road characteristics & 3D position from different traffic agents.

External Perception sensors performance can vary according to the operating outdoor environment conditions. A lot of factors come into play:
- Dynamic Range; ratio of largest to smallest measurable signal in radars
- Resolution; number of pixels in an image.
- Frame rate; the rate at which data is acquired, measured in frames per second.
## Cameras:
Cameras are the primary visual input device in an autonomous vehicle. They capture rich, detailed imagery of the environment. 
### How they capture data?

**Sensor**: Digital Cameras use CCD (Charge-coupled devices) or the standard and more popular CMOS (complementary metal-oxide-semiconductor) that are sensitive to light, by letting the light in, the lens captures the light and using thsensore photoelectric effect it turns it into an electronic signal proportional to the intensity of light detected at each point of the lens. 
**Pixels:** the image sensor is composed of tiny light-sensitive elements, the more there are of those the better resolution we get. Image resolution is usually measured in Mega Pixels (MP).

### Type of data captured:
The data captured is visible light reflected on objects of interest. This is very important for detecting lane markings, pedestrians and traffic lights.

### Data Processing Requirements:
cameras don't work well under:
- Poor lighting conditions: tunnels and at night
- Bad weather conditions: fog, snow and rain obscure objects of interest.
- Depth estimation: they're very poor for depth perception.
- Data Load: image processing is very computationally expensive and introduces latency.

## LiDARs:
short for Light Detection And Ranging, this is used to solve the problem of depth estimation in autonomous vehicles.

### How they capture data?
LiDAR sensors emit pulsed laser beams and measures how long each beam takes to bounce back after hitting the object. This data is they used to model a "3D point cloud" that is a detailed representation of the environment. 

### Type of data captured:
is the reflected laser beams reflected from objects. which is used for:
- Distance to objects: precision is down to centimeters
- Height and depth: it's important to understand terrain & curbs
- Scene geometry: outlining the physical objects of the environment

### Data Processing Requirements:
- needs real-time processing as it generates massive datasets in small amount of time.
- Accuracy is deeply impacted by rain, fog and snow.

## Radars:
stands for radar detection and ranging.

### How they capture data?
they emit radio waves from a transmitter and wait for it to bounce back from objects. It then measures the frequency shift and the time it took for it to bounce back. To calculate distance, relative speed and direction of motion.

### Type of data captured:
the radio waves reflected from objects, that is useful for 
- tracking moving vehicles; as the doppler effect can give us a hint about the moving vehicles by measuring frequency shift.
- collision avoidance.

### Data processing requirements:
- Clutter in dense environments; in urban areas with many reflective surfaces it is difficult to isolate signals.
- Radars know how far and how fast a thing is going, but it can't know what the thing is.
- It returns a lot of false positives as metallic objects can cause a problem called "ghost objects" due to the multiple reflective paths returned.

![[Pasted image 20250904161336.png]]
*Cameras, LiDARs & Radars*
# Stereo Vision
By comparing information about a scene from two vantage points, 3D information can be extracted by examining relative positions of objects in two panels. This is very similar to human vision and how humans process environments. 

1. **Setup:** cameras are positioned with known separation (baseline), and known parameters (focal length and optical center).
2. **Disparity Map:** we find corresponding pixels between the two images. Then we measure the horizontal pixel differences (or the disparity) between the images.
3. **Depth map:** we use the disparity map and the parameters we have to build a copy of the original image but instead of every pixel representing a color, every pixel encodes distance information. This is called a "depth map". 
$$Z = \frac{bf}{d}$$
$$ \text{Z : depth}$$
$$\text{b : baseline, the distance between the two cameras} $$$$  \text{f : focal length of the cameras }$$
$$\text{d: disparity between the two images }$$
4. **3D Reconstruction:** we then use the depth map to make a 3D reconstruction of both images. 


# Machine Learning
- What are neural networks? How do they learn?
- How can neural networks be used to aid with processing sensor data for environment perception?
### Neural Networks:
are computational objects based on biological neural networks. The neural network is made up of neurons and weights. We have:
- **input neurons**, which receive various information from the outside world. 
- **output neurons**, thaccomodatee return the information learnt.
- **hidden neurons**, in deep learning we have additional neurons called hidden neurons and they do additional processing and communication for the model to learn the thing needed.
![[Pasted image 20250904051420.png|]]
- the weights on each line or edge from one neuron to another encodes the "importance" of the node to another. 
- for earlier hidden neurons, the model usually learns simpler patterns, but as we go further in the model the model learns more complex data and encodes it.
### How do they learn?
- to predict or to "run" the neural network, you pass input at the input units.
- by passing the input, we got an output from the model. 
- we then usually have a correct output "in supervised learning scenarios", so we compare the "prediction" of our model to the true labels
- we then run a loss function, to measure the difference between the prediction and true labels.
- we then measure how much each neuron contributed to the this "loss", by running gradients (a bit similar to derivatives).
- we then do backpropagation, where we take those gradients and adjust neurons and "optimize" them so that their contributions are more aligned towards the outputs we have.

### How can neural networks be used for perception?
Deep-learning and neural networks are really good for automatic feature extraction. Instead of demanding from engineers to manually manipulate data to accommodate environmental conditions for example, we can train our models multiple times with the correct labels and let the model learn what want it to learn. 

Neural networks can also be very useful for object detection as we can use some tweaks on the traditional neural networks, by using things like CNNs (convolutional neural networks) & YOLO (you only look once) models that show promising results in object detection and image segmentation (splitting images to segments of relative similarity).