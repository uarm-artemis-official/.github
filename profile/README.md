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

## Step 3: Environment Setup

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

### Download Docker ROS2 Humble Image and Deploy

- **For Windows, macOS, and Linux Users**:
  1. Open a terminal and run the following command to download and run the ROS2 Humble Docker image:

     ```
     docker run -it --rm --privileged --name ros2_humble_container -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev:/dev -v $(pwd)/ros2_ws:/ros2_ws uarm/ros2:humble
     ```

  2. This will start a Docker container with the ROS2 Humble environment.

### Enable Docker to Run turtlesim with a Graphical Interface

- **For Windows, macOS, and Linux Users**:
  1. Ensure that your X Server is running (macOS users may need additional setup).
  2. In the terminal where you're running the Docker image, execute the following command to run turtlesim:

     ```
     ros2 run turtlesim turtlesim_node
     ```

     This will start turtlesim and display the graphical interface.

## Step 4: IDE Setup

Now, let's set up your Integrated Development Environment (IDE) to make it easier for you to write and debug code.

### Download VS Code

- **For Windows, macOS, and Linux Users**:
  1. Download and install [Visual Studio Code](https://code.visualstudio.com/).

### Download Necessary VS Code Extensions

- **For Windows, macOS, and Linux Users**:
  1. Open VS Code.
  2. Install the following extensions:
     - C/C++
     - ROS 2
     - Docker
     - Remote - Containers

### Configure VS Code Docker Extension

- **For Windows, macOS, and Linux Users**:
  1. In VS Code, click the "Remote Explorer" icon in the lower left corner.
  2. Click "Containers" and select the ROS2 Humble Docker container you created earlier.
  3. Click "Attach to Container."

Now, your VS Code is connected to the Docker container, allowing you to program within the container.

## Step 5: Run Docker Image and Write Code

You are now ready to write and run ROS2 code within the ROS2 Humble Docker environment.

### Run the Docker Image

- **For Windows, macOS, and Linux Users**:
  1. Open VS Code.
  2. In VS Code, click the "Remote Explorer" icon in the lower left corner.
  3. Click "Containers" and select the ROS2 Humble Docker container you created.
  4. Click "Attach to Container."
  5. Open a terminal within VS Code.
  6. Navigate to your ROS2 workspace directory:

     ```
     cd /ros2_ws
     ```

  7. You can now program in ROS2 within the container.

### Create a ROS2 Package and Write Code

- **For Windows, macOS, and Linux Users**:
  1. In VS Code, open a terminal.
  2. In the terminal, run the following command to create a new ROS2 package:

     ```
     ros2 pkg create my_package --build-type ament_cmake --node-name my_node
     ```

     This will create a new ROS2 package called "my_package."

  3. Open the package using VS Code and start writing your ROS2 code.
  4. Write a basic publisher and subscriber program and run it within the container.

You have now successfully set up your development environment and can start writing and running ROS2 code. If you encounter any issues at any step, feel free to seek assistance. Enjoy your time with the UARM C&S team!
