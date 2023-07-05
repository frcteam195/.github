## CyberKnights Robotics
### FRC Team 195


### CyberKnights Robotics has moved to GitLab as of the start of July 2023. You can find our new projects here: [https://gitlab.team195.com/cyberknights](https://gitlab.team195.com/cyberknights)












CyberKnights Robotics is a FIRST Robotics Competition high school robotics team. This program allows students to learn and engage in real-world engineering and deisgn, mentored by industry professionals.

Since the FRC 2022 season, our team has focused on developing a ROS ecosystem. If you are interested in looking at our pre-ROS code, you can checkout our FRC 2021 and earlier repositories.

<details>
  <summary><h2>Robot Software Development Timeline</h2></summary>
  
- [2015 - LabVIEW (RoboRIO)](https://github.com/frcteam195/FRC2015)
- [2016 - LabVIEW (RoboRIO)](https://github.com/frcteam195/FRC2016), [LabVIEW (Kangaroo - Vision Only)](https://github.com/frcteam195/KnightVision-FRC-2016)
- [2017 - C++ (RoboRIO), C++ (NVIDIA Jetson - Vision Only)](https://github.com/frcteam195/FRC2017)
- [2018 - Java (RoboRIO), LabVIEW (Driver Station Computer - Vision Only)](https://github.com/frcteam195/FRC2018)
- [2019 - Java (RoboRIO), Limelight 2 Vision](https://github.com/frcteam195/FRC2019)
- [2022 - ROS/C++ (NVIDIA Jetson), C++ (RoboRIO), Limelight 2+ Vision](https://github.com/frcteam195/2022_ROS_Robot)
- [2023 - ROS/C++/Python (NVIDIA Jetson), C++ (RoboRIO), Limelight 3 Vision](https://github.com/frcteam195/2023_FRC_Robot)
- [2024 - ROS2/C++/Python (NVIDIA Jetson), C++ (RoboRIO), Limelight 3 Vision](https://github.com/frcteam195/2024_FRC_Robot)

Our current goal is to make ROS accessible to all teams within 5 years. Currently, ROS ecosystems need significant software development capabilities. Our hopes are to simplify this so that a team can get up and running with a basic ROS ecosystem that controls their robot in under a day.
</details>

<details>
  <summary><h2>Autonomous Control</h2></summary>

Currently our robot autonomous modes use an action-based library to simplify the creation of these autos. Actions can be reused, configured, and adjusted through their parameters and the robot can execute them sequentially or concurrently. This framework concept is based on the autonomous actions from FRC Team 254.
Since the 2023 season, we've switched to a Python autonomous controller and action system in order to make development easier for students. Because our ecosystem is based on ROS, each robot subsystem is controlled independently, and because of this, we do not take any performance loss from using python instead of a compiled language such as C++ (because the code for the subsystems that are timing critical actually IS C++).
</details>

<details>
  <summary><h2>Autonomous Planning</h2></summary>

Our team has developed a Python path planning interface to help students easily create paths and deploy them to our robot. This tool, called the [PathCobbler](https://github.com/frcteam195/PathCobbler), creates json syntax files that describe a path for the robot to follow. For the upcoming season, we are planning to create full autonomous json files. These will include the Actions to run through our Action framework so that the PathCobbler interface can be used to create an entire autonomous mode visually.
</details>

<details>
  <summary><h2>ROS</h2></summary>

Our team is focused on developing a ROS ecosystem robot. ROS stands for Robot Operating System, which is a service/framework that helps different controller processes communicate with each other and also can simplify performing complex functions (such as localization, mapping, etc.). Each subsystem on our robot is controlled by a separate node. These nodes communicate with one another through ROS in order to fully control the robot. Part of the simplification of this process is our CKRIOPassthru software. This is RoboRIO firmware that is a companion project that allows the RoboRIO to be controlled from the ROS ecosystem running on the Jetson and has two way communication for things like Joysticks, Motors, etc. When using our ROS projects, the [CKRIOPassthru](https://github.com/frcteam195/CKRIOPassthru) project is required to be running on the RoboRIO.

If you're interested in getting started with ROS, you can checkout our [ros_dev](https://github.com/frcteam195/ros_dev) and [2023_FRC_Robot](https://github.com/frcteam195/2023_FRC_Robot) repositories on an Ubuntu 22.04 machine. With both of these repositories in the same parent directory, cd into the containing directory and run the following command:
```
./ros_dev/run_container.sh
```
This will launch a Docker container with the packages necessary to develop for ROS. Now that you're inside the container, run
```
./ros_dev/mkrobot.sh clone
./ros_dev/mkrobot.sh build
./ros_dev/mkrobot.sh launch
```
This sequence of commands will clone all dependencies for the 2023_FRC_Robot project, build all of the projects, and then launch these projects locally for debugging/testing.
</details>

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
