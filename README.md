# YoloBot_src ROS2 Package

This repository contains the YoloBot_src ROS2 package, which subscribes to the `/camera/image_raw` topic, performs inference using YOLOv8, and publishes the inferred results.
## Video Demo

[Watch the video](https://www.youtube.com/watch?v=u3AINTM3tSE)

Click above to watch the video demonstration of the project.
## Dependencies

This package depends on the `bot_spawn` ROS2 package, which can be found at [https://github.com/Kaivalya192/bot_spawn](https://github.com/Kaivalya192/bot_spawn). Make sure to clone and install the `bot_spawn` package before using YoloBot_src.

Additionally, ensure that you have the `ultalytics` Python package installed. You can install it using pip:

```bash
pip3 install ultalytics
```
## Installation

### Create Workspace
Create a workspace folder named `ros2_ws`.

### Clone Repository
Clone this repository into the `src` folder of your ROS2 workspace (`ros2_ws/src/`).

```bash
git clone https://github.com/Kaivalya192/YoloBot_src.git
```
## Build

Navigate to the root of your workspace (`ros2_ws/`) and build the packages using the following command:

```bash
colcon build
```
## Source Setup Script

After successful build, source the setup script to add the package to your ROS2 environment:

```bash
source install/setup.bash
```
## Setup

Before running the package, make sure to launch the `bot_spawn` package, which provides the necessary robot model and camera topics. You can follow the instructions in the `bot_spawn` README.md for setup.

## Usage

To launch the YoloBot_src package, make sure that the `bot_spawn` package is running and publishing `/camera/image_raw`. Then, execute the following command:

```bash
ros2 launch YoloBot_src launch_yolov8.launch.py
```
This command will start the YOLOv8 inference node, which subscribes to `/camera/image_raw`, performs inference, and publishes the results.

## Notes

- Ensure that your system meets the requirements for running YOLOv8 inference.
- Adjust the configuration parameters as needed in the launch file or source code.
- For any issues or improvements, feel free to open an issue or pull request on GitHub.

## License

This project is licensed under the MIT License, which means you are free to use, modify, and distribute the code as long as you include the original license file.
