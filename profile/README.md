# 로빛 최종 프로젝트 organization

깃 커밋 컨벤션: [참조 링크](https://velog.io/@archivvonjang/Git-Commit-Message-Convention)

# alias 설정 
```
alias dy="cd ~/colcon_ws && colcon build --packages-select && source install/setup.bash && ros2 launch dynamixel_hardware_interface dynamixel_hardware.launch.py"
alias ik="cd ~/colcon_ws && colcon build --packages-select ik_walk && source install/setup.bash && ros2 run ik_walk ik_walk"
alias tu="cd ~/colcon_ws && colcon build --packages-select tune_walk && source install/setup.bash && ros2 run tune_walk tune_walk"
alias imu="cd ~/colcon_ws && colcon build --packages-select ebimu && source install/setup.bash && ros2 launch ebimu e2box_imu_9dofv4.launch.py"
alias mo="cd ~/projects/Humanoid-Motion-Teacher && source /opt/ros/jazzy/setup.bash && ./build/Humanoid_Motion_Teacher"
alias vision="cd ~/colcon_ws && colcon build --packages-select robot_vision && source install/setup.bash && ros2 launch robot_vision robot_vision.launch.py"
alias insta="cd ~/colcon_ws && colcon build --packages-select insta360_usb_cam && source install/setup.bash && ros2 launch insta360_usb_cam usb_cam.launch.py"
alias local="cd ~/colcon_ws && colcon build --packages-select localization && source install/setup.bash && ros2 launch localization localization.launch.py"
alias gc = "cd ~/colcon_ws && source /opt/ros/jazzy/setup.bash && source ~/colcon_ws/install/setup.bash && ros2 launch gamecontroller gamecontroller.launch.py"
alias ta = "cd ~/colcon_ws && source /opt/ros/jazzy/setup.bash && colcon build --symlink-install && source install/setup.bash && source /opt/ros/jazzy/setup.bash && ros2 launch task_planner task_planner.launch.py"
alias na="cd ~/colcon_ws && colcon build --packages-select robit_navigation && source install/setup.bash && ros2 launch robit_navigation robot.launch.py"
```
# 모든 패키지 다운로드
```
git clone -b jazzy https://github.com/ROBOTIS-GIT/DynamixelSDK.git
git clone -b jazzy https://github.com/ROBOTIS-GIT/dynamixel_interfaces.git

gh repo list Robit-humanoid-final-project --limit 500 --json nameWithOwner --jq '.[].nameWithOwner' | xargs -n 1 gh repo clone
```

# dynamixelSDK, interfaces
```
git clone -b jazzy https://github.com/ROBOTIS-GIT/DynamixelSDK.git
git clone -b jazzy https://github.com/ROBOTIS-GIT/dynamixel_interfaces.git
```

# Build
```
cd ~/colcon_ws
source /opt/ros/jazzy/setup.bash
colcon build --symlink-install
source install/setup.bash
```

# 단축어 정리

단축어에 빌드 명령어 포함 되어있습니다. 

dynamixel_hardware_interface
```
dy
```

ik_walk
```
ik
```

ebimu
```
imu
```
