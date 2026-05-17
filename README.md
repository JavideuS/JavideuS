# Javier Gonzalez Villasmil

  Robotics Engineering student focused on **autonomous systems, optimization, and machine learning**.
  Robotics freestyler building tech with real-world impact - "When you are going to change the world, don't ask for permission".

  ---

  ## 🏆 Awards

  **RoboHack 2026 — 1st Place**
  Built [argOS](https://github.com/JavideuS/argOS): a cloud-native intelligence layer that lets you command a quadruped robot in plain English from any browser, anywhere.

  ---

  ## Projects

  ### [Spooky](https://github.com/JavideuS/Spooky)
  Multi-robot path planning using **QUBO formulation**
  - Models coordination as an optimization problem with adaptive penalty design
  - >95% variable reduction through BFS-based preprocessing
  - Benchmarks classical vs quantum-inspired solvers with reproducible results
  - Published on arXiv: [2602.14799](https://arxiv.org/abs/2602.14799)

  **Tech:** Python, QUBO, Pennylane, D-Wave, NumPy

  ### [argOS](https://github.com/JavideuS/argOS)
  Cloud-native intelligence and browser UI layer for quadruped robots
  - Commands a robot dog in plain language from any browser, over the internet
  - LLM agent (Claude) with MCP tool access to navigation and perception
  - Real-time 3D lidar map streamed to your phone; YOLO11 object segmentation
  - Semantic memory with confidence decay, persisted across sessions via S3
  - Sits on top of DimOS — designed to support other navigation backends

  **Tech:** Python, ROS2, AWS (Bedrock, Transcribe, S3), FastAPI, WebGL

  ### [robotsito](https://github.com/JavideuS/robotsito)
  Hexapod robot with adaptive gait control
  - Inverse kinematics solver for 18-DOF leg configuration
  - Tripod gait pattern with sensor-based obstacle avoidance
  - Simulated in Gazebo and deployed on real hardware

  **Tech:** ROS2, C++, Gazebo

  ---

  ## Open Source Contributions

  ### [aries_ros](https://github.com/JavideuS/aries_ros)
  ROS2 wrapper for the Aries automated planner (Rust-based, PDDL/HDDL)
  - Compiles Aries via Cargo as part of the Colcon build with no separate install step
  - Supports durative actions; includes a utility to sanitize non-ASCII PDDL files

  ### [plansys2_aries_plan_solver](https://github.com/JavideuS/plansys2_aries_plan_solver)
  PlanSys2 plugin that swaps in Aries as the planning backend
  - Drop-in replacement for POPF/TFD, configured via YAML, with no PlanSys2 source changes needed
  - Includes worked PDDL examples and notes on durative action concurrency quirks

  **Tech:** C++, ROS2, PlanSys2, PDDL, Rust (Aries)

  ---

  ## ML

  ### [transformers_bridge](https://github.com/JavideuS/transformers_bridge)
  ROS2 ↔ HuggingFace transformers bridge for vision tasks
  - Outputs standard `vision_msgs/Detection2DArray`; designed to be subclassed by downstream perception stacks
  - Inference runs on a background thread so the ROS executor is never blocked
  - Allows customization of the inference pipeline through a YAML configuration file and a simple class inheritance structure.
  - Modify of draw class depending on the model used
  
  **Tech:** Python, ROS2, HuggingFace Transformers, Ultralytics YOLO, PyTorch
  
  ---
  
  ## Stack
  **Languages:** Python, C++
  **Robotics:** ROS2, Gazebo, PlanSys2, PDDL
  **ML / Perception:** Vision, HuggingFace Transformers, Ultralytics YOLO, PyTorch
  **Cloud:** AWS (Bedrock, Transcribe, S3), FastAPI
  **Optimization:** QUBO, Pennylane, D-Wave 
  **Tools:** Linux, Git, Docker

  ---
  
  ## Links
  [Portfolio](https://javideus.github.io) · [LinkedIn](https://linkedin.com/in/javideus) ·
  [arXiv](https://arxiv.org/abs/2602.14799)