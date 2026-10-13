# Javier Gonzalez Villasmil

Final-year Robotics Software Engineering student (URJC, Madrid) working on **multi-robot planning, quantum optimization and robot locomotion**.
Robotics freestyler building tech with real-world impact - "When you are going to change the world, don't ask for permission".

- **Now:** bachelor's thesis on a multimodal ground–aerial robot with assisted wall climbing, and a research fellowship at CAR-CSIC (VR training simulator in Unity)
- **Summer 2026:** research intern at Fraunhofer CML (Hamburg), quantum optimization and robotics
- **Paper:** [Scalable Multi-Robot Path Planning via QUBO](https://arxiv.org/abs/2602.14799) (arXiv, 2026)
- 🏆 **RoboHack 2026 at EPFL, 1st place** with [argOS](https://github.com/JavideuS/argOS)

---

## Multi-robot stack

Three repos that work together: one plans, one executes, one is the interface. Tested in NVIDIA Isaac Sim and on a fleet of three real AgileX Ranger Mini robots.

```
Spooky (global planner)  ->  clew (fleet execution on Nav2)  ->  argOS (browser interface)
```

### [Spooky](https://github.com/JavideuS/Spooky)
Multi-robot path planning as a QUBO, with quantum and classical solvers behind one API
- >95% variable reduction through BFS-based preprocessing; time-windowed solving for current hardware
- Run on real quantum hardware (IBM Quantum Platform, IQM Resonance), plus PennyLane QAOA and D-Wave annealing
- Classical ILP and CBS baselines, with a benchmark framework to compare them
- Published on arXiv: [2602.14799](https://arxiv.org/abs/2602.14799)

**Tech:** Python, QUBO, Qiskit, PennyLane, D-Wave Ocean, FastAPI

### [clew](https://github.com/JavideuS/clew)
ROS2 fleet coordinator that takes Spooky's plan to real robots
- Turns the global plan into per-robot release schedules around conflict zones
- Executes through each robot's own Nav2 stack, with stall and deadlock recovery

**Tech:** Python, ROS2, Nav2

### [argOS](https://github.com/JavideuS/argOS)
Browser interface to command robots in plain language (RoboHack 2026 winner)
- LLM agent with MCP tool access to navigation and perception
- Live 3D lidar map in the browser; semantic object memory from YOLO detections
- Fleet interface for Spooky and clew: shared map, multi-robot view and control (on the [`work`](https://github.com/JavideuS/argOS/tree/work) branch)

**Tech:** Python, FastAPI, MCP, AWS, WebGL, YOLO

---

## Hardware

### [robotsito](https://github.com/JavideuS/robotsito)
Quadruped robot of my own design, in development
- Mechanics in FreeCAD; inverse kinematics and gait control in C++/ROS2
- Gazebo simulation; first walking gait on the real robot (Oct 2026)

---

## ROS2 packages

Packages meant to drop into any ROS2 stack.

### [transformers_bridge](https://github.com/JavideuS/transformers_bridge)
ROS2 node for HuggingFace Transformers and Ultralytics YOLO detection models
- Outputs standard `vision_msgs/Detection2DArray`; inference on a background thread

### [aries_ros](https://github.com/JavideuS/aries_ros) and [plansys2_aries_plan_solver](https://github.com/JavideuS/plansys2_aries_plan_solver)
The Aries PDDL/HDDL planner for ROS2, and a drop-in PlanSys2 plugin that uses it

---

## Stack
- **Languages:** C++, Python, C
- **Robotics:** ROS2, Nav2, NVIDIA Isaac Sim, Gazebo, FreeCAD, PlanSys2
- **Planning & Optimization:** QUBO, ILP, CBS, QAOA, Qiskit, PennyLane, D-Wave Ocean
- **ML / Perception:** PyTorch, HuggingFace Transformers, YOLO, OpenCV
- **Tools:** Linux, Git, Docker, FastAPI

---

## Links
[Portfolio](https://javideus.github.io) · [LinkedIn](https://linkedin.com/in/javideus) ·
[arXiv](https://arxiv.org/abs/2602.14799)
