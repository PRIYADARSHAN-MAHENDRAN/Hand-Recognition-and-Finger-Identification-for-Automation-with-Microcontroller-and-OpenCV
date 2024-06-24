# Hand-Recognition-and-Finger-Identification-for-Automation-with-Microcontroller-and-OpenCV

This project uses a webcam and Mediapipe to recognize hand gestures and control various appliances like TV, fan, etc., connected to an Arduino board through relays. The gestures are detected using computer vision techniques, and specific gestures trigger the corresponding appliances.

## Features

- Detect hand gestures using a webcam
- Control appliances connected to an Arduino board based on recognized gestures
- Simple integration with Mediapipe for hand detection and gesture recognition

## Requirements

- Python 3.x
- OpenCV
- Mediapipe
- PyFirmata
- Arduino board with relays connected to digital pins

## Setup

1. **Clone the Repository**
    ```sh
    git clone https://github.com/PRIYADARSHAN-MAHENDRAN/Hand-Recognition-and-Finger-Identification-for-Automation-with-Microcontroller-and-OpenCV/tree/main
    ```

2. **Install Python Dependencies**
    ```sh
    pip install opencv-python mediapipe pyfirmata
    ```

3. **Connect Arduino Board**
    - Connect relays to digital pins 13, 12, and 11.
    - Connect the Arduino board to your computer and note the COM port (e.g., COM4 on Windows or /dev/ttyUSB0 on Linux).

4. **Update `controller.py`**
    - Ensure the `comport` variable matches your Arduino's COM port.
    ```python
    comport = 'COM4'  # Update this to match your Arduino's COM port
    ```

## Usage

1. **Run the Main Script**
    ```sh
    python main.py
    ```

2. **Hand Gestures**
    - Show different hand gestures to control the appliances:
      - **One Finger**: Turn on Appliance 1 (e.g., TV)
      - **Two Fingers**: Turn on Appliance 2 (e.g., Fan)
      - **Three Fingers**: Turn on Appliance 3 (e.g., Light)
      - **Four Fingers**: Turn off all appliances

## Code Overview

### `main.py`

Handles the webcam feed, hand detection, and gesture recognition. It uses Mediapipe for hand landmarks detection and OpenCV for video processing.

### `controller.py`

Defines the `control_appliances` function to control the relays based on recognized gestures. It uses PyFirmata to communicate with the Arduino board.

### Example

![Hand Gesture Controlled Appliances](path/to/screenshot.png)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Mediapipe](https://github.com/google/mediapipe) by Google
- [OpenCV](https://opencv.org/)
- [PyFirmata](https://github.com/tino/pyFirmata)

