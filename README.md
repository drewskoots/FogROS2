# FogROS2
Run the docker by 
```
FOGROS_REPO=~/Desktop/FogROS2
docker run -it --rm \
    -v "${FOGROS_REPO}/examples":/opt/ros2_ws/src/fogros2_examples \
    -v "${FOGROS_REPO}/launch":/opt/ros2_eloquent/src/ros2/launch \
    keplerc/ros2:latest /bin/bash
```
then run the test examples
```
cd /opt/ros2_ws/
colcon build --allow-overriding fogros2_examples
. /opt/ros2_ws/install/setup.bash
ros2 launch fogros2_examples talker.launch.py
```