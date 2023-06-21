## CyberKnights Robotics
### FRC Team 195

CyberKnights Robotics is a FIRST Robotics Competition high school robotics team. This program allows students to learn and engage in real-world engineering and deisgn, mentored by industry professionals.

Since the FRC 2022 season, our team has focused on developing a ROS ecosystem. If you are interested in looking at our pre-ROS code, you can checkout our FRC 2021 and earlier repositories.


## Robot Code Software Development Timeline

- 2015 - LabVIEW (RoboRIO)
- 2017 - C++ (RoboRIO)
- 2018 - Java (RoboRIO)
- 2022 - ROS/C++ (Jetson), C++ (RoboRIO)
- 2023 - ROS/C++/Python (Jetson), C++ (RoboRIO)
- 2024 - ROS2/C++/Python (Jetson), C++ (RoboRIO)

Our current goal is to make ROS accessible to all teams within 5 years. Currently, ROS ecosystems need significant software development capabilities. Our hopes are to simplify this so that a team can get up and running with a basic ROS ecosystem that controls their robot in under a day.


## Autonomous Control

Currently our robot autonomous modes use an action-based library to simplify the creation of these autos. Actions can be reused, configured, and adjusted through their parameters and the robot can execute them sequentially or concurrently. This framework concept is based on the autonomous actions from FRC Team 254.
Since the 2023 season, we've switched to a Python autonomous controller and action system in order to make development easier for students. Because our ecosystem is based on ROS, each robot subsystem is controlled independently, and because of this, we do not take any performance loss from using python instead of a compiled language such as C++ (because the code for the subsystems that are timing critical actually IS C++).

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
