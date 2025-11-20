
<p align="center">
  <a href="https://github.com/Sysmic-Robotics/engine">
    <img src="https://i.imgur.com/vU1zy4V.png" alt="Engine" width="150"/>
  </a>
  <a href="https://github.com/Sysmic-Robotics/insight">
    <img src="https://i.imgur.com/LN4MGdz.png" alt="Insight" width="150"/>
  </a>
  <a href="https://github.com/Sysmic-Robotics/strategy">
    <img src="https://i.imgur.com/rt4mUG8.png" alt="Strategy" width="150"/>
  </a>
</p>

<h1 align="center">CondorSSL</h1>

<p align="center">
  <strong>CondorSSL</strong> is a modular and extensible software suite designed for the <br/>
  <a href="https://ssl.robocup.org/" target="_blank"><strong>RoboCup Small Size League (SSL)</strong></a>.
</p>

<p align="center">
  It integrates three core components: <strong>Insight</strong> (Frontend UI), <strong>Engine</strong> (Low-level control), and <strong>Strategy</strong> (AI decision-making).
</p>

# What is this?

CondorSSL is a system that enables omnidirectional robots to play a soccer match (football match). The system is divided into three main components: two programs (Engine and Insight) and a collection of scripts (Strategy).

* **1. Engine** (https://github.com/Sysmic-Robotics/engine): This program contains the low-level logic responsible for basic robot autonomy and system communication.
    * **Autonomous Driving:** Uses path planning and control algorithms to enable the robots to move reliably and efficiently between two points.
    * **Communication:** Handles data exchange, allowing the system to receive data from the robots and the vision system, and to send commands to the robots and the referee box.
    * **API:** The API is the core of the system through which all data and commands pass. It features multiple interfaces to ensure easy debugging and seamless access to principal features, such as autonomous driving.

* **2. Insight:** This program is built primarily for debugging, monitoring, and setup purposes. Its principal features include:
    * **Visualization:** It is critical to visualize the program's perception of the field, as it often differs from the real world. This feature displays robot coordinates and the paths they are **currently tracking**.
    * **Plots & Metrics:** Allows users to check performance metrics like velocity and energy levels, and to run experiments.
    * **Manual Control & Scripting:** Provides tools for user interaction, such as playing Lua control scripts, manually controlling a robot with a joystick, sending direct instructions (e.g., move to a point), or removing a robot from the vision system's tracking.

* **3. Strategy:** Strategy is not a single program but a collection of scripts and high-level logic that enables the robots to play the game effectively. Its features define robot behavior at various levels:
    * **Skills:** Basic, atomic robot movements and actions, such as Go to Ball, Mark a Robot, and Kick.
    * **Tactics:** Coordinated robot movements and defensive/offensive formations, such as passing plays and strategic defense.
    * **Game Flow:** The overall logic dictating how robots should behave according to official referee rules and game states (e.g., **STOP**, **HALT**, **PLAY**, **OUR KICK OFF**, and **THEIR KICK OFF**).

# Validation

We are happy to share that CondorSSL was successfully validated during the **RoboCup 2025 in Salvador** .

<p align="center">
  <a href="https://youtu.be/rncd2WXzMhY?feature=shared" target="_blank">
    <img src="https://img.youtube.com/vi/rncd2WXzMhY/0.jpg" alt="CondorSSL RoboCup 2025 Validation" width="600"/>
  </a>
</p>
