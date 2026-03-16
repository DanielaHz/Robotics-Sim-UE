# Research Notes: Robotics Simulation in Unreal Engine

## 1. Company Overview 

![image](/images/All3.jpg)

All3 is transforming how buildings are conceived, developed, and delivered. We combine AI-powered design with robotic prefabrication and on-site assembly to build custom architecture at the cost and speed of mass production.

## 2. Role Analysis
focused on building a **deterministic, physics-accurate simulation platform** for **multi-robot construction assembly**. You will develop **high-performance Unreal-based systems that replicate real-world robotic behaviour and enable large-scale autonomy testing**.


### 2.1 What other platforms exist for robotics simulation?

- Isaac Sim (NVIDIA)
- Gazebo (Open Source)
- Unreal Engine (Epic Games)


## 2.2 Interesting companies and projects
- https://github.com/iamaisim/ProjectAirSim
- https://github.com/google-deepmind/mujoco
- https://www.generalrobotics.company/post/airgen
- https://cesium.com/
- https://www.blackshark.ai/
- https://github.com/OpenSim2Real

### 2.3 What could be the critical challenges of this system?

- The built‑in physics engines (Chaos and PhysX) may lack the precision required for accurate mechanical simulation.
    - **Chaos Physics:** A lightweight physics solver intended to replace PhysX once fully production‑ready.
    - **PhysX:** Currently used by default for physical simulation and collision calculations in Unreal Engine.
- Achieving high‑precision robotics simulation may require integrating a custom physics engine.
    - **Bullet SDK:**  Bullet Physics SDK: real-time collision detection and multi-physics simulation for VR, games, visual effects, robotics, machine learning etc. We are developing a new differentiable simulator for robotics learning, called Tiny Differentiable Simulator, or TDS. The simulator allows for hybrid simulation with neural networks. It allows different automatic differentiation backends, for forward and reverse mode gradients. 
    - **ODE: Open Dynamics Engine:** ODE is an open source, high performance library for simulating rigid body dynamics. It is fully featured, stable, mature and platform independent with an easy to use C/C++ API. It has advanced joint types and integrated collision detection with friction. ODE is useful for simulating vehicles, objects in virtual reality environments and virtual creatures. It is currently used in many computer games, 3D authoring tools and simulation tools.

- Efficient 3D asset management is critical. Unreal provides solid tooling for this, but the overall performance and workflow depend heavily on the structure and complexity of the simulation scenarios.

## 3. Tasks 

- Building a scalable, headless, deterministic simulation platform for multi-robot on-site construction assembly.

- Simulating coordinated robotic systems operating in shared physical space. Including manipulation, contact, constraints, tolerances, and assembly sequencing;

- Implementing physically grounded sensor models (LiDAR, cameras, IMUs) to support autonomy and perception development;

- Designing high-performance data bridges between Unreal Engine and external C++/Python robotics stacks to enable large-scale scenario testing and AI validation.

## 4. Relevant Concepts

### 4.1 Deterministic Simulation:
Deterministic simulations are computational models that produce identical outputs every time they are run, provided the input parameters and initial conditions remain the same

### 4.2 Multi-robot construction assembly:

### 4.3 Large-scale autonomy testing:

### 4.4 High-performance Unreal-based systems:

## 5. Questions

### 5.1 Technical 

- Why did you choose Unreal Engine over Isaac Sim or Gazebo, given that Isaac Sim is purpose-built for robotics and already integrates ROS2?

- What's your approach to determinism — are simulations expected to be bit-exact reproducible, or is behavioural consistency sufficient?


### 5.2 Understanding the Role & Scope

- You mentioned open roles that match my profile — are you envisioning this as a research-heavy position, an engineering role, or a mix of both? Egnineering posirion to work in the real role


- Would I be joining an existing simulation effort, or is this more of a greenfield build?

#### Unreal side as well

- Capabilits light art, simulating cameras perspective and orthographics perception, 
simulating their, stereo cameras.

- Extremely large cad models
reinforcement learning and trainig so on 

- How much ownership would someone in this role have over technical decisions?


### 5.3 Team & Ways of Working

- What does the team you're building look like right now — size, backgrounds, how people collaborate day to day?

### 5.4 Company Direction

- Where is All3 in its journey right now — are you in active deployments, still in R&D, or somewhere in between?

- What's driving the urgency to grow the simulation team at this point?

### 5.5 Project and goals 
- What does a successful simulation platform look like in 6 and 12 months for you?
- What are the biggest unsolved problems in your current simulation or testing workflow?
- How many robots and how complex are the assembly scenarios you need to simulate at scale?


### 5.6 Company Overview (Bullet Points)
- Construction company delivering end‑to‑end projects

- Works on commercial and residential buildings

- Mission: reduce emissions, shorten construction time, and lower costs

- Distinctive approach:

    - Build a central core

    - Add cross‑sections/modules

    - Assemble the rest of the building efficiently (prefabrication‑style)

####  Team & Technology
- ~35 employees

- Dedicated simulation team

- Produces photorealistic images and camera‑based simulations

- Future goal: build a frontend to render full building models

- Tech stack includes:

- Embedded Linux, Ubuntu, Docker containers

- the team bigger simulation test

- conquerence and atomic.

- events

- parallel simulate x robots, you dont think cuda lenguage, to paralelize objects 

## 6. Challenges (Opportunities)

- Interactive/rich behaviour form agents in sim
- Manipulator/contact rich robotics
- Quicker Creation of environments 
    - How to leverage 3DGS more effectively 
    - USD Support
    - Optimize and convert  Phtomogrammetry to real-time sim 
    - Procedural generation 
    - Ground detail at large scale
    - Generative AI integrations for rapid asset/scene creation
- Sensor accuracy - how important?
- Physics-based sensors (LIDAR, IR, RADAR and other EO)
    - Physics based reflections, IR imagery 
    - Emulation of accurate noise in sensors

## Resources 

- https://www.youtube.com/watch?v=JmxuRn1Jk18&t=877s
- https://developer.nvidia.com/isaac/sim
- https://www.youtube.com/watch?v=PT07H4BXdfY
- https://sourceforge.net/projects/bullet-physics-sdk.mirror/
- https://cyberbotics.com/doc/reference/ode-open-dynamics-engine
- https://www.ode.org/
- https://www.faro.com/en/Resource-Library/Article/What-is-Lidar
- https://www.linkedin.com/pulse/world-building-autonomous-systems-nvidia-omniverse-unreal-engine-uu7vc/?


