```bash
sudo apt update
sudo apt install portaudio19-dev
```

A
```bash
# 端末 A1: マイク → audio_a_out
source ~/ros2_ws/install/setup.bash
ros2 run audio_mic_pub_cpp mic_publisher_a_node

# 端末 A2: audio_b_out を再生
source ~/ros2_ws/install/setup.bash
ros2 run audio_mic_pub_cpp audio_player_a_node
```
B
```bash
# 端末 B1: マイク → audio_b_out
source ~/ros2_ws/install/setup.bash
ros2 run audio_mic_pub_cpp mic_publisher_b_node

# 端末 B2: audio_a_out を再生
source ~/ros2_ws/install/setup.bash
ros2 run audio_mic_pub_cpp audio_player_b_node
```