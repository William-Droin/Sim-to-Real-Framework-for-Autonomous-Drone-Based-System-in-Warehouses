# Sim-to-Real Framework for Autonomous Drone-Based Systems in Warehouses

**Author:** William Droin  
**Institution:** King’s College London  
**Program:** MSc in Robotics  
**Thesis Date:** August 15, 2024  
**Link to thesis:** [Final report (mark: **87%**)](Sim-to-Real-Framework-for-Autonomous-Drone-Based-System-in-Warehouses-Final-Report.pdf)
# Sim-to-Real Framework for Autonomous Drone-Based Warehouse Safety Audits

# Sim-to-Real Framework for Autonomous Drone-Based Warehouse Safety Audits

---

## Project Overview

The **Sim-to-Real Framework** is an advanced, integrated solution aimed at revolutionizing warehouse safety management by deploying autonomous drone systems for routine safety audits. It seamlessly combines cutting-edge simulation technology (Nvidia Omniverse's Isaac Sim) with state-of-the-art drone navigation and real-time computer vision to ensure compliance with essential safety regulations—specifically focusing on detecting the presence of safety vests on warehouse personnel. 

This framework addresses multiple operational challenges, providing:

- A highly realistic virtual environment enabling comprehensive drone training scenarios
- Automated collision avoidance systems to ensure safe navigation in complex warehouse spaces
- Robust real-time safety compliance monitoring leveraging deep learning and computer vision
- Scalability for potential multi-drone operations in expansive facilities

---

## Technical Highlights

### Choice of Tools

- **Simulation Environment**: Nvidia Omniverse Isaac Sim (for realistic drone and environment simulations)
- **Quadcopter Simulation**: Pegasus Simulator for detailed drone modeling
- **Communication Protocols**: Hybrid ROS (low-level control, video streaming) & Mavlink (high-level control)
- **Collision Avoidance**: Real-time obstacle detection using depth cameras and ROS integration
- **Navigation System**: PID-controlled waypoint navigation balanced with proactive collision avoidance
- **Computer Vision**: Custom dataset generation with Nvidia Replicator, adaptable to TensorFlow and PyTorch frameworks

### Virtual Warehouse Environment Creation

- Custom-built virtual warehouse leveraging Nvidia's extensive asset library
- Detailed realism including manually arranged elements like storage racks, packages, and safety indicators to mimic real operational environments

### Computer Vision Model Implementation

- **Architecture**: ResNet50 CNN (known for its robust and efficient image recognition capabilities)
- **Adaptation**: Customized output layer specifically for detecting safety compliance
- **Data Preprocessing**: Enhanced dataset realism with image augmentation techniques
- **Training**: 16,000 synthetic images over 10 epochs, employing transfer learning
- **Real-time inference**: Achieved ~63 FPS, supported by temporal smoothing for reliability

---

## Results and Performance

### Simulation Optimization

- Significant frame-rate improvement (~86% increase using DLSS)
- Load time optimization (~70% faster using Nvidia Nucleus and Cache)
- Reduced memory footprint, supporting broader hardware compatibility

### Drone Control

- Optimal drone navigation achieved with balanced collision avoidance and waypoint accuracy
- Successful mission completion rate around 70%

### Computer Vision

- High synthetic dataset accuracy (~95%) during initial training
- Real-time inference capable (processing in ~15.82 ms/frame)
- Identified critical need for diverse real-world data for improved accuracy (current real-world accuracy ~43%)

### Scalability

- Demonstrated potential for scaling to multi-drone operations under simplified simulation conditions
- Further optimizations required for seamless multi-drone performance in complex real-world scenarios

---

## Future Directions

- Expanding the synthetic dataset to include diverse scenarios for better real-world performance
- Further enhancing drone navigation algorithms for precision and efficiency
- Multi-drone coordination to expand operational capabilities

---

**For comprehensive insights, detailed methodologies, and complete results analysis, explore the full documentation provided in this repository.**

## Acknowledgements

Thanks to **Nokia Bell Labs**, **Pr. Yansha Deng** **Dr. Toktam Mahmoodi**, and **Ryo Koblitz** for their invaluable support and contributions.

