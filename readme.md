# scenes

## Jetson
- A demo scene to demonstrate rosbridge on Windows11/WSL

On Wsl side:
- Install ROS 2 Humble
    - https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html#set-locale
    - Test that it works with talker/listener
    
- Install Ros Bridge
    - `sudo apt install ros-humble-rosbridge-server`
    
- Start ROS 2 Bridge
    - `ros2 launch rosbridge_server rosbridge_websocket_launch.xml`
    
 On Windows 11
    - Install Isaac Sim (tested with 4.1.0 and 4.2.0)
    - Start Isaaac Sim with following settings
        - When the Isaa Sim App Selector comes up:
            - The "ROS Bridge Extenstion" Dropdown has "omni.isaac.ros2_bridge"
            - The "Use Internal ROS2 Libraries" has "humble
            - Note: 
               - There is a UI bug. 
               - So these are very difficult to select as the selections get overwritten by a notification. 
               - You don't see them immediately, when you do they are quite small"
               - You have to click around in the area to find them.
               - But it can be done!
               
     -  If the ROS bridge has been started in WSL it should now load without error messages
     - Now load the jetson.usd scene - you should get a tree and a Jetson bot on the standard blue gridded floor
     - Hit the Play button (triangle) on the far left.
     - The jetson should fall to the floor.
     
     
 Back to WSL
     - Run `ros2 topic pub /jetbot_cmd_vel geometry_msgs/Twist '{linear: {x: 0.2, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 0.3}}'`
               
           
## Rollaball.usd 
- Work on `https://www.youtube.com/watch?v=nTrnCZuG8bU`
