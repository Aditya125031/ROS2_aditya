# ROS 2 Learning Documentation

Contained herein are the concepts and details I have grasped during my study of **ROS 2**.

---

## 📘 What Did I Learn?

This overview highlights the key concepts I have learned up to this point.

---

## 🔁 Relearning C++

While I was already familiar with C++, a comprehensive review of its concepts was necessary.  
Before starting with the Ubuntu and ROS 2 setup, I decided to revisit C++ since it's fundamental to working with ROS 2. Refreshing my understanding helped me move forward with more confidence.

---

## 💻 Setting Up Ubuntu

- Learned how to **dual boot** a laptop with Ubuntu.  
- Created a **Ubuntu setup drive** to easily dual boot other devices in the future.

---

## 🚀 Installing ROS 2 Humble

- Upgraded and updated system packages  
- Set system locale to **UTF-8** for compatibility  
- Installed essential tools like `software-properties-common` and `curl`  
- Added the **ROS 2 repository** and imported its **GPG key** securely  
- Installed **ROS 2 Humble packages** on Ubuntu  
- Sourced the ROS 2 environment to enable command-line tools  

---

## 🐢 Launching My First Node – Turtlesim

### What I Learned Using ROS 2 Turtlesim:
- Ran the `turtlesim_node` to launch the simulation  
- Controlled the turtle using `turtle_teleop_key`  
- Listed active ROS 2 nodes and topics to monitor the system  
- Used `ros2 topic echo` to view real-time message data  

---

## 📊 rqt Tools

- Visualized node connections using **rqt_graph**  
- Called services and monitored output using **rqt_console**  
- Explored and edited node behavior via GUI plugins

---

## 🛠️ Building a ROS 2 Workspace

### What I Learned:
- Created and set up a workspace from scratch  
- Used terminal commands to create the workspace directory  
- Organized the directory structure properly (`src` folder, etc.)  
- Installed required dependencies using `rosdep`  
- Built the workspace using `colcon build`  
- Sourced the workspace to set up the environment  

---

## 📦 Creating a ROS 2 Package

- Used `ros2 pkg create` command to generate the package scaffold  
- Selected `ament_cmake` as the build type  
- Added custom source code files  
- Defined package dependencies in `package.xml` and `CMakeLists.txt`  
- Built the package within the workspace using `colcon build`  
- Sourced the workspace environment to use the new package  

---

## 🌀 Testing the Turtlesim Spiral

- Explored an existing **ROS 2 spiral movement implementation** using Turtlesim from GitHub  
- Created a ROS 2 workspace and added a custom package named `cpp_topic` to the `src` directory  
- Included `cpp_pub_spiral.cpp` and `cpp_sub_spiral.cpp` from GitHub  
- Updated `CMakeLists.txt` to include dependencies and define executables  
- Modified `package.xml` to include appropriate dependencies  
- Built the workspace and sourced the environment to test the nodes  

---
# 🧪 ROS 2 Random Number Publisher & Subscriber (Task 1)

## 📚 What I Learned

### 🟢 Creating a Random Number Publisher

- **Included Necessary Headers:**
  - `rclcpp` for core ROS 2 functionality
  - `random` for generating random numbers
  - `std_msgs` for standard message types like `Int32`

- **Defined a Publisher Node:**
  - Created a class inheriting from `rclcpp::Node`
  - Implemented a publisher to generate and publish random integers

- **Configured Build Files:**
  - Registered the publisher executable in `CMakeLists.txt`
  - Linked necessary libraries and installed the target

- **Built and Ran the Node:**
  - Built the workspace using `colcon build`
  - Sourced the workspace environment
  - Successfully ran the publisher node to publish random integers

### 🔵 Creating a Corresponding Subscriber

- **Similarity to Publisher Node:**
  - The subscriber node's structure closely mirrors that of the publisher node, making the development process more straightforward

- **Included Necessary Headers:**
  - `rclcpp` for core ROS 2 functionality
  - `std_msgs` for standard message types like `Int32`

- **Defined a Subscriber Node:**
  - Created a class inheriting from `rclcpp::Node`
  - Implemented a subscription to the topic published by the random number publisher
  - Developed a callback function to process incoming messages

- **Built and Ran the Node:**
  - Sourced the workspace environment
  - Successfully ran the subscriber node to receive and display random integers

## ⚠️ Challenges Encountered

### 🧩 Building Another Package

- Faced difficulties when building an additional package.
- Did not encounter issues with the Turtlesim Spiral, as the code was sourced from Git.
- Writing the `CMakeLists.txt` and `package.xml` files became a significant challenge.
- Compared my files with those from the Spiral package to identify inconsistencies. Upon finding discrepancies, I researched solutions and sought assistance.
- Overcame the challenges with some help from fellow interns.

### 🚀 Running the Nodes

- Initially believed that the `CMakeLists.txt` and `package.xml` files were correctly configured, as the workspace built without errors.
- Encountered issues when sourcing the files.
- Upon reviewing and comparing the files, realized there were mistakes in the project name, which caused the issues.

### 📤 Uploading the Code to GitHub

- Initially attempted to upload the entire workspace to Git, which resulted in errors, leading to the realization that uploading the entire workspace is not ideal.
- Considered uploading a zip file, as done previously in the Maze Rover project, but this approach was not favored by the mentor.
- Observed peers' repositories and decided to upload only the `src` folder containing the essential files.
- Still need to resolve the issue of uploading a folder to Git using the terminal, as Git encountered problems with the generated token.

### 📝 Writing the Markdown File

- For tasks completed before becoming an intern, the `README.md` file was plain text due to a lack of knowledge about Markdown.
- Recently learned some Markdown syntax; while not yet proficient, with assistance from Google and AI tools, managed to make it work.
- Aim to become proficient in creating these files through continued practice.

## ⚙️ Prerequisites

- Ubuntu 22.04  
- ROS 2 Humble installed  
- Basic knowledge of Python and C++  
- Familiarity with terminal commands  


## 📁 Project Directory Structure
task1_ws/

├── build/ # Build files generated by colcon

├── install/ # Installed files

├── log/ # Log files

└── src/

    └── num_topic/

        ├── package.xml # Package manifest

        ├── CMakeLists.txt # Build instructions

        └── src/

            ├── number_publisher.cpp # Publisher node
  
            └── number_subscriber.cpp # Subscriber node

## 📚 Resources Used

- [ROS 2 Tutorial by Kevin Wood](https://youtu.be/HJAE5Pk8Nyw)
- [ROS 2 Tutorial by Backend robotics ](https://youtu.be/0aPbWsyENA8)
- [ROS 2 Tutorial Series by Robotgeddon](https://www.youtube.com/watch?v=QfFnljTrRlQ&list=PLNw2RD-1J5YZbyWXCpas9zPJldfphPi4Q)
- [ROS 2 Docs](https://docs.ros.org/en/humble/index.html)
- [Articulated Robotics Tutorials](https://articulatedrobotics.xyz/tutorials/)


## ✅ Conclusion

This journey through ROS 2 helped me build a foundational understanding of:
- System setup and environment configuration
- ROS 2 node and package development
- Debugging and visualization tools (like rqt)
- Practical experimentation with Turtlesim and GitHub codebases

