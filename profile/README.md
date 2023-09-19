# UARM C&S Student Onboarding Guide

Welcome to the UARM Computer & Software (C&S) team! Here are the steps you need to complete to ensure a smooth start to your learning and projects. Please follow these steps, and if you encounter any issues, don't hesitate to ask for help.

## Step 1: Join Our Social Platforms

First, join our Discord community, which serves as our primary communication and collaboration tool.

- **For Windows, macOS, and Linux Users**:
  1. Open your web browser and go to the following link: [UARM C&S Discord](https://discord.gg/hwFU94jgQG).
  2. On the Discord page, click "Join Server," then enter your username and email to create a Discord account if you don't already have one.
  3. Locate "RoboMaster NA Discord" within our server and join: [RoboMaster NA Discord](https://discord.gg/cCpbSZTAbS).

## Step 2: Fill Out the On-boarding Form

Please complete our On-boarding form to help us better understand your background and interests.

- **For Windows, macOS, and Linux Users**:
  1. Open your web browser and go to the following link: [On-boarding Form](https://forms.gle/tyk36Nxgo9joBvxp7).
  2. Fill out all required fields in the form and ensure you provide accurate information.
  3. Submit the form to complete the registration process.

## Step 3: Installing OpenCV with Visual Studio Code on Windows, macOS, and Linux

We will guide you through the process of setting up a C++ development environment with OpenCV and using Visual Studio Code as your integrated development environment. We'll cover the installation steps for Windows, macOS, and Linux.

For members preferred Python, the only command you need is "pip install opencv-python" and that's it!

### Prerequisites

Before you begin, ensure you have the following prerequisites:

- A computer running either Windows, macOS, or Linux.
- An internet connection to download necessary software.
- Visual Studio Code (VS Code) installed on your system. You can download it from [VS Code's official website](https://code.visualstudio.com/).
- Basic familiarity with your operating system's terminal or command prompt.

### Installing C++ Compiler

#### Windows

1. For Windows, we recommend using the [Microsoft Visual C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/). Download and install the build tools, which include the C++ compiler.

#### macOS

1. On macOS, you can use the default C++ compiler, which is part of Xcode. Install Xcode from the App Store if you haven't already.

#### Linux

1. On Linux, you can install the GNU C++ Compiler (g++) using your distribution's package manager. For example, on Ubuntu, run:

   ```bash
   sudo apt-get update
   sudo apt-get install g++
   ```

### Installing OpenCV

#### Windows

1. Download the pre-built OpenCV library for Windows from the [official OpenCV website](https://opencv.org/releases/).
2. Follow the installation instructions provided on the website to set up OpenCV on your Windows machine.

#### macOS

1. Install OpenCV on macOS using the package manager Homebrew. Open a terminal and run:

   ```bash
   brew install opencv
   ```

2. After installation, you can find the OpenCV headers and libraries in `/usr/local/include/opencv4` and `/usr/local/lib`, respectively.

#### Linux

1. On Linux, you can use your distribution's package manager to install OpenCV. For example, on Ubuntu, run:

   ```bash
   sudo apt-get install libopencv-dev
   ```

2. This will install the OpenCV development package, which includes headers and libraries.

### Setting Up Visual Studio Code

1. Open Visual Studio Code.
2. Install the "C/C++" extension by Microsoft to enable C++ development in VS Code. You can find this extension in the VS Code marketplace.
3. Install the "CMake Tools" extension by Microsoft to simplify CMake-based project configuration if you plan to use CMake for your projects.

### Creating a C++ Project

1. Open VS Code.
2. Create a new folder for your C++ project.
3. Inside the project folder, create a new C++ source file (e.g., `main.cpp`).

### Writing and Building Your C++ Code

1. Write your C++ code in `main.cpp`. Make sure to include <opencv2/opencv.hpp>.
2. Create a `CMakeLists.txt` file in the project folder to configure your C++ project. Here's a basic example:

   ```cmake
   cmake_minimum_required(VERSION 3.10)

   project(YourProjectName)

   find_package(OpenCV REQUIRED)

   add_executable(YourExecutableName main.cpp)

   target_link_libraries(YourExecutableName PRIVATE ${OpenCV_LIBS})
   ```

3. Open the project folder in VS Code.
4. Use the "CMake: Configure" and "CMake: Build" commands from the Command Palette to configure and build your project.

### Running Your C++ Code

1. After a successful build, you can run your C++ binary program from within VS Code.

Congratulations! You have set up a C++ development environment with OpenCV and Visual Studio Code on Windows, macOS, or Linux. You are now ready to develop C++ applications with OpenCV using VS Code as your IDE.

## Step 4: ROS2 Environment Setup (Optional)

**NOTE: Since our main focus is to develop CV algorithms, as long as club members can develop code for vision independently, the lead can put the code directly into the ROS2 framework. Therefore, the decision for this year is that configurinng ROS2 environment locally is no longer mandatory and you are free to skip the following steps.**

Now, let's prepare your development environment. Below are the steps to install Docker and configure the ROS2 Humble Docker environment.

### Install Docker

- **For Windows Users**:
  1. Download and install [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop).
  2. Launch Docker Desktop and ensure it's running in the system tray.

- **For macOS Users**:
  1. Download and install [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop).
  2. Launch Docker Desktop and ensure it's running in the menu bar.

- **For Linux Users**:
  1. Install Docker and Docker Compose using the methods provided by your Linux distribution.
  2. Start the Docker service.

### Download Docker ROS2 Humble Image and Deploy & Enable Docker to Run ROS2 with a Graphical Interface

- **For Windows, macOS, and Linux Users**:
  1. Follow up the tutorial for [Setting up the ROS2 Docker](https://www.youtube.com/watch?v=qWuudNxFGOQ).

You have now successfully set up your development environment and can start writing and running ROS2 code. If you encounter any issues at any step, feel free to seek assistance. Enjoy your time with the UARM C&S team!
