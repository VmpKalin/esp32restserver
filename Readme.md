# Setup
    pip3 install -U platformio
    pio project init --board esp32cam --project-option="framework=espidf"
    
# Run virt env:
    python3 -m venv venv
    source venv/bin/activate

# Build the project
    pio run

# Upload to ESP32-CAM
    pio run --target upload

# Monitor serial output
    pio device monitor


# Installation of esp-idf
    sudo apt update
    sudo apt install git wget flex bison gperf python3 python3-pip python3-venv cmake ninja-build ccache libffi-dev libssl-dev dfu-util libusb-1.0-0

# Create directory and clone
    mkdir -p ~/esp
    cd ~/esp
    git clone --recursive https://github.com/espressif/esp-idf.git

# Go to esp-idf directory
    cd esp-idf

# Checkout stable version
    git checkout v5.1.2
    git submodule update --init --recursive

# Install ESP-IDF tools
    ./install.sh

# Export environment
    . ./export.sh

