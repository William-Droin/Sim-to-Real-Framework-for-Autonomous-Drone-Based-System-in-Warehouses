# Sim-to-Real Framework for Autonomous Drone-Based Systems in Warehouses

**Author:** William Droin  
**Institution:** King’s College London  
**Program:** MSc in Robotics  
**Thesis Date:** August 15, 2024
# Sim-to-Real Framework for Autonomous Drone-Based Warehouse Safety Audits

## Project Overview
This repository presents a comprehensive Sim-to-Real framework designed for deploying autonomous drones to perform safety audits in warehouse environments. The system is developed to detect compliance with safety regulations, particularly the presence or absence of safety vests worn by workers, leveraging computer vision integrated with drone navigation systems.

---

## Technical Summary

### Choice of Tools

**Simulation Environment:**
- Nvidia Omniverse's Isaac Sim selected for its superior visual fidelity, extensive robotic support, and suitability for Sim-to-Real transitions.
- The Isaac Sim environment facilitates realistic drone simulations, significantly reducing risks and costs associated with real-world drone testing.

**Quadcopter:**
- Pegasus Simulator is employed for realistic drone modeling, allowing integration with ROS and Mavlink protocols.

**Communication Protocol:**
- Combined use of ROS and Mavlink:
  - ROS: Low-level interaction and streaming video feed from the drone's onboard cameras.
  - Mavlink: High-level drone control, particularly effective for waypoint-based navigation.

**Collision Avoidance:**
- Integrated depth camera streamed via ROS, analyzed by a Python script to detect and avoid obstacles dynamically.

**Navigation Protocol:**
- Hybrid waypoint system combined with automatic collision avoidance.
- Utilizes PID controllers to balance navigation accuracy and collision avoidance effectiveness.

**Computer Vision:**
- Nvidia Replicator module automates synthetic dataset generation, significantly speeding up the data collection process.
- Supports integration with major deep learning frameworks like TensorFlow and PyTorch.

### Creation of the Virtual Environment
- Warehouse environment constructed from the ground up using Nvidia Isaac Sim assets.
- Detailed, realistic warehouse layout including hand-placed elements like shelves, boxes, and safety markers to reflect real-world warehouse complexity.

### Computer Vision Model Selection and Implementation

**Model Architecture:**
- ResNet50 CNN selected for its effective balance between computational efficiency and accuracy.

**Model Adaptation:**
- Modified final fully connected layer to distinguish between two classes (safety vest compliance vs. non-compliance).
- Transfer learning utilized from ImageNet pretrained weights.

**Data Preprocessing:**
- Image resizing, normalization, and augmentation for improved model robustness.

**Training Details:**
- Dataset of 16,000 synthetic images.
- Training parameters: Batch size of 24, trained over 10 epochs using Adam optimizer (learning rate: 0.001).

**Inference and Post-processing:**
- Real-time frame processing at approximately 63 FPS, capable of live video stream analysis.
- Implemented temporal smoothing to mitigate transient misclassifications.

### Results

**Simulation Optimization:**
- Achieved substantial performance improvements using DLSS technology, optimized loading via Nucleus server, and memory usage reduction through simplified 3D assets.

**Drone Control Performance:**
- Best results obtained with balanced weights between collision avoidance and waypoint navigation, achieving approximately 70% successful mission completion.

**Computer Vision Performance:**
- High accuracy (94.6%) during training with synthetic data.
- Effective real-time processing capabilities with frame inference time ~15.82 ms.
- Lower accuracy on real-world images (approximately 43%) indicating the need for more diverse training data.

**Scalability:**
- Framework supports multiple drones under simplified conditions; adjustments required for real-time, multi-drone scenarios.

---

## Future Directions
- Enhancing dataset diversity for improved real-world generalization.
- Further refinement of drone navigation algorithms for higher mission accuracy and efficiency.

---

For detailed analysis, results, and methodologies, please refer to the full thesis documentation provided in this repository.

## Acknowledgements

Thanks to **Nokia Bell Labs**, **Pr. Yansha Deng** **Dr. Toktam Mahmoodi**, and **Ryo Koblitz** for their invaluable support and contributions.

