# Vizor.Sendframe

[![Release](https://img.shields.io/github/v/release/VizorAX/sendframe)](https://github.com/VizorAX/sendframe/releases)
[![License](https://img.shields.io/github/license/VizorAX/sendframe)](LICENSE)

> **Vizor.Sendframe** includes both `vizor.sendframe.exe` and `vizor.recvframe.exe` for efficient, low-latency video streaming over a network using HEVC and hardware acceleration.

---

🌟 **Key Features**
-------------------

- 📡 **Low-Latency Video Streaming**: Achieve real-time streaming over the network with minimal delay.
- 🎯 **Configurable Parameters**: Customize output dimensions, bitrate, and network settings.
- ⚡ **HEVC with Hardware Acceleration**: Leverages NVIDIA NVENC for encoding on compatible GPUs and Windows DXVA2 for decoding to ensure efficient video compression and streaming.

📥 **Download and Installation**
-------------------------------

### **Requirements**

- **Operating System**: Windows 10 or later (Untested on other Windows versions)
- **Graphics Requirements**:
  - **Streamer**: Requires an NVIDIA GPU with NVENC support.
  - **Receiver**: Requires Windows with DirectX Video Acceleration (DXVA2) support.
- **Disk Space**: At least 200 MB of free space

### **Dependencies**

- **FFmpeg**: Included in the release bundle.
- **SDL2**: Included in the release bundle.

### **Installation Steps**

1. **Download the Latest Release**: Get the executable from the [Releases](https://github.com/VizorAX/sendframe/releases) page.
    
2. **Extract the Package**:
    - Unzip the downloaded package to your preferred directory. The required DLLs are included in the same directory.
    
3. **Run the Executables**:
    - **To Stream Frames**: `vizor.sendframe.exe <streamer_port> <receiver_address> <receiver_port> <output_width> <output_height> <bitrate>`
    - **To Receive Frames**: `vizor.recvframe.exe <receiver_port> <streamer_address> <streamer_port> <window_width> <window_height>`

4. **Launch the Application**:
    - After running the commands, the executables will handle the frame streaming and reception as per the provided parameters.

📖 **Usage Examples**
---------------------

### Streaming Frames
```bash
vizor.sendframe.exe 5000 192.168.1.100 6000 1280 720 500000
```
- Streams frames from port `5000` to the receiver at address `192.168.1.100` on port `6000` with output dimensions `1280x720` and a bitrate of `500000`.

### Receiving Frames
```bash
vizor.recvframe.exe 6000 192.168.1.50 5000 1280 720
```
- Receives frames on port `6000` from a streamer at address `192.168.1.50` on port `5000`, displayed in a window of size `1280x720`.

🛠️ **Troubleshooting**
-----------------------

If you encounter issues, try the following:

- **Check for Updates**: Ensure you have the latest version from the [Releases](https://github.com/VizorAX/sendframe/releases) page.
- **Verify Hardware Compatibility**: Make sure your hardware meets the requirements (NVIDIA GPU for the streamer, DXVA2 support on Windows for the receiver).
- **Verify Parameters**: Double-check command-line arguments for correctness.
- **Ensure Stable Connection**: Make sure your network connection is stable, and if possible, use ethernet cables instead of wireless networks to minimize latency and packet loss.
- **Contact Support**: Reach out to [sansorich@gmail.com](mailto:sansorich@gmail.com) with details of your issue.

📄 **License**
--------------
This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for more details.

📧 **Contact**
--------------

- **Rodrigo R. S. Sorgato**: [LinkedIn](https://www.linkedin.com/in/rrssorgato) | [Email](mailto:sansorich@gmail.com)
