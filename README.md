# FR1-micro - Waveshare ESP32-S3-Touch-LCD-1.47 with libFRX

This project demonstrates using libFRX with the Waveshare ESP32-S3-Touch-LCD-1.47 board.

## Features

- **SD Card Access**: Write and read files using libFRX's SD card module
- **Audio Support**: Configured for the onboard MEMS microphone and DAC
- **I2C Support**: Ready for I2C device communication
- **jescore Integration**: Full command-line interface support

## Setup

### Prerequisites

1. Install PlatformIO
2. Clone this repository
3. Ensure libFRX is accessible (configured as a git dependency)

### Building and Uploading

```bash
cd FR1-micro
pio run -t upload
```

### Monitoring

```bash
pio device monitor
```

## Demo Program

The demo in `src/main.cpp` shows basic libFRX SD card operations:
- Initialize jescore and SD card
- Create/write/read/delete files
- List directory contents
- Proper error handling and cleanup

## Configuration

See `PIN_DEFS.md` for detailed pin definitions and `platformio.ini` for build configuration.

## Board Specifications

- **MCU**: ESP32-S3
- **Flash**: 16MB
- **PSRAM**: 8MB
- **Display**: 1.47" 172x320 RGB LCD with touch
- **SD Card**: SDMMC interface
- **Audio**: MEMS microphone + DAC
- **Connectivity**: WiFi + Bluetooth 5.0

## Troubleshooting

- **SD Card**: Ensure proper insertion, FAT32 format, check connections
- **Audio**: Verify I2S connections and sample rate settings
- **Compilation**: Check `platformio.ini` for correct module enables and pin definitions

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contributing

Contributions are welcome! Please open issues or pull requests for any improvements or bug fixes.
