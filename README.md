# AI Traffic Management

An intelligent traffic signal control system using computer vision and machine learning to dynamically optimize traffic flow.

## Abstract

Urban traffic congestion is a pressing issue that worsens with the rise of vehicular density in cities. Traditional traffic management systems, based on fixed signal timings, lack the adaptability needed to handle the dynamic and often unpredictable nature of traffic flow.

This project introduces an AI-based traffic signal control system that leverages real-time video data from CCTV cameras to dynamically optimize traffic signal timings based on actual traffic conditions. By integrating computer vision techniques and machine learning models, the system can calculate traffic density in real-time and adjust traffic signal timings to reduce waiting times, fuel consumption, and pollution. The project aims to improve urban traffic management by providing a smart, adaptive, and scalable solution.

## Features

- **Real-time Vehicle Detection**: Uses YOLO (You Only Look Once) to detect and classify vehicles including cars, bikes, buses/trucks, and rickshaws
- **Traffic Density Calculation**: Calculates real-time traffic density based on vehicle count and type
- **Dynamic Signal Timing**: Adjusts green signal duration based on traffic density
- **Simulation Environment**: Includes a custom-built simulation for testing and visualization
- **High Accuracy**: Achieves over 99% detection accuracy during normal conditions

## Problem Statement

The rapid growth in vehicular density in urban areas necessitates a more responsive and adaptable traffic management system. Current traffic control methods, based on fixed-time or manual systems, are incapable of efficiently managing the ever-changing traffic conditions, leading to:

- Prolonged waiting times
- Wasted fuel
- Increased air pollution
- Stress for commuters

## Proposed System

The system consists of several key components:

### 1. Real-Time Traffic Flow Monitoring
- Live video feed analysis from existing CCTV cameras
- Vehicle detection and classification using YOLOv3

### 2. Traffic Density Calculation
- Real-time processing of vehicle counts
- Density estimation based on vehicle types and counts

### 3. Signal Time Estimation Using Machine Learning
- ML-based prediction of optimal green signal duration
- Training on simulated traffic data

### 4. Dynamic Signal Adjustment
- Real-time control of traffic signals
- Adaptive timing based on current traffic conditions

## System Architecture

![image](https://github.com/user-attachments/assets/ca7b1df6-a1ed-432c-a3ef-826026c1a55e)


## Implementation

### Vehicle Detection Module

The project uses YOLO (You Only Look Once) for vehicle detection, which provides the desired accuracy and processing time. A custom YOLO model was trained to detect various vehicle classes including cars, bikes, heavy vehicles (buses and trucks), and rickshaws.

![image](https://github.com/user-attachments/assets/119af7ad-8e73-4d08-9263-cac34c84de32)


### Signal Switching Algorithm

The algorithm calculates green signal times based on:
- Number of vehicles of each class
- Time added due to lag during start-up
- Average speed of each class of vehicle
- Minimum and maximum time limits to prevent starvation

### Simulation Module

A custom simulation was developed using Pygame to visualize and test the system. It includes:
- 4-way intersection with traffic signals
- Various vehicle types with different speeds
- Turning vehicles for realistic traffic simulation
- Signal timing display and vehicle count statistics

![image](https://github.com/user-attachments/assets/94347fd6-6151-4b4b-9640-babd79967cbb)


## Results

### Performance Metrics

The system demonstrates impressive performance:
- **Vehicle Detection Accuracy**: Over 99% during normal conditions, 89% during adverse conditions
- **Wait Time Reduction**: 20-30% at busy intersections compared to static systems
- **Overall Improvement**: 23% increase in the number of vehicles crossing the intersection

![image](https://github.com/user-attachments/assets/041ab68a-0940-4792-bf68-b0f6f779bf1f)


### Advantages Over Existing Systems

- **Cost-Effective**: Uses existing CCTV infrastructure
- **Low Maintenance**: No additional hardware on roads (unlike pressure mats)
- **Highly Accurate**: Uses advanced computer vision algorithms
- **Adaptive**: Responds to real-time traffic conditions
- **Scalable**: Can be deployed across multiple intersections

## Future Work

The project can be expanded to include additional functionalities:

1. **Traffic Violation Detection**: Identify vehicles running red lights or changing lanes improperly
2. **Accident Detection**: Detect accidents or vehicle breakdowns at intersections
3. **Multi-Intersection Synchronization**: Coordinate signals across multiple intersections
4. **Emergency Vehicle Priority**: Automatic detection and prioritization of emergency vehicles

## Technical Requirements

### Hardware
- CCTV cameras for video capture
- Edge computing devices or servers for processing

### Software
- Python
- YOLOv3 for object detection
- OpenCV for video processing
- TensorFlow for machine learning models

## Source Code

The repository includes:
- Vehicle detection module
- Signal switching algorithm
- Simulation environment
- ML model training code

## Conclusion

The proposed system sets the green signal time adaptively according to traffic density at the signal and ensures that the direction with more traffic is allotted a green signal for a longer duration compared to directions with less traffic. This system reduces unwanted delays, congestion, and waiting time, which in turn reduces fuel consumption and pollution.

## References

1. TomTom World Traffic Index, 2019
2. Khushi, "Smart Control of Traffic Light System using Image Processing," CTCEEC, 2017
3. A. Zaid, Y. Suhweil and M. A. Yaman, "Smart controlling for traffic light time," IEEE, 2017
4. Renjith Soman, "Traffic Light Control and Violation Detection Using Image Processing," IOSR-JEN, 2018
5. Siddharth Srivastava et al., "Adaptive traffic light timer controller," IIT KANPUR

---

For additional details, please refer to the full documentation or contact the project maintainers.
