## Dependencies:
```Shell
pip install grpcio
pip install grpcio-tools
pip install pygame
pip install protobuf==3.20.*

# Build proto:
cd ~/[your ws]/src/oav_utils/scripts
python3 -m grpc_tools.protoc -I ./interface --python_out=. --grpc_python_out=. ./interface/rpi-motor.proto
```

## SSH Interface
# Jetson
ssh user@192.168.2.101
```Shell
ros2 launch oav_utils jetson_launch.py
```

# Raspberry
ssh pi@192.168.2.103
```Shell
python3 RPIMotorService.py
```

# Laptop
ssh pi@192.168.1.11
```Shell
git clone https://github.com/soyhorteconh/omni_ros2.git
```
