# Sim-to-Real Framework for Autonomous Drone-Based Systems in Warehouses

**Author:** William Droin  
**Institution:** King’s College London  
**Program:** MSc in Robotics  
**Thesis Date:** August 15, 2024

## Abstract

This project presents a **Sim-to-Real framework** that enables autonomous drones to perform **safety audits in warehouse environments**. Leveraging NVIDIA's **Omniverse Isaac Sim**, the system simulates realistic warehouse environments where drones navigate and detect worker compliance (e.g., presence of safety vests). Through a combination of **ROS**, **Mavlink**, and **deep learning** models like **ResNet50**, the solution enables controlled, efficient, and scalable testing before deploying to real-world warehouses.

---

## � Objectives

- Develop a **virtual warehouse** environment from scratch.
- Integrate **autonomous drone control** using ROS and Mavlink.
- Implement **collision avoidance** and **waypoint navigation**.
- Create a **custom dataset** using Isaac Sim Replicator.
- Train and deploy a **computer vision model** to detect safety vest compliance.

---

## Tech Stack

- **Simulation**: NVIDIA Omniverse Isaac Sim, Pegasus Simulator
- **Drone Control**: ROS 2, Mavlink
- **Computer Vision**: Python, OpenCV, TensorFlow / PyTorch, ResNet50
- **Dataset Generation**: Isaac Sim Replicator
- **Communication Protocols**: ROS topics, MAVLink messages

---

## Setup & Installation

> Recommended: Ubuntu with NVIDIA GPU (VRAM ≥ 10GB)

1. **Clone the repository**  
```bash
git clone https://github.com/yourusername/drone-sim2real-framework.git
cd drone-sim2real-framework
```

2. **Set up Isaac Sim**  
   Download and install Isaac Sim through the [NVIDIA Omniverse launcher](https://developer.nvidia.com/omniverse).

3. **Install dependencies**  
```bash
pip install -r requirements.txt
```

4. **Launch the simulation**  
   Load the custom warehouse scene in Isaac Sim and start the simulation.

5. **Run the drone control system**
```bash
ros2 launch drone_control control.launch.py
```

---

## Safety Audit Demo

In this demo, an autonomous drone navigates through a warehouse and identifies workers based on their safety compliance (presence/absence of safety vests).

![Demo Diagram](docs/architecture.png)

---

## Performance

| Metric                       | Value (Simulated)        |
|-----------------------------|--------------------------|
| Drone Navigation Accuracy   | ~70% mission success     |
| Collision Avoidance         | <10% crash rate          |
| Computer Vision Accuracy    | 94.6% (Sim), 43% (Real)  |
| Inference Speed             | ~15ms / frame (63 FPS)   |
| VRAM Requirement            | ~9.1 GB (Optimized)      |

---

## Repository Structure

```
├── docs/                  # Diagrams & documentation
├── datasets/              # Synthetic training datasets
├── drone_control/         # ROS/Mavlink scripts
├── vision/                # Computer vision models
├── isaac_env/             # Virtual warehouse environment
├── requirements.txt
└── README.md
```

---

## Limitations & Future Work

- Improve **generalization to real-world data** via more diverse datasets.
- Extend to **multi-drone coordination** and **inventory tasks**.
- Optimize for **lightweight inference** on embedded drone hardware.

---

## Citation

If you use this work, please cite:
```
@mastersthesis{droin2024sim2real,
  title={Sim-to-Real Framework for Autonomous Drone-Based System in Warehouses},
  author={William Droin},
  school={King’s College London},
  year={2024}
}
```

---

## Acknowledgements

Thanks to **Nokia Bell Labs**, **Pr. Yansha Deng** **Dr. Toktam Mahmoodi**, and **Ryo Koblitz** for their invaluable support and contributions.

