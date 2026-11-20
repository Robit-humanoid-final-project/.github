# 로빛 최종 프로젝트 organization

깃 커밋 컨벤션: [참조 링크](https://velog.io/@archivvonjang/Git-Commit-Message-Convention)

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
