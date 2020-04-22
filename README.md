# Time lapse

This project configures a [Raspberry Pi](https://www.raspberrypi.org) with the [camera module](https://projects.raspberrypi.org/en/projects/getting-started-with-picamera) to run as a time lapse camera.

## Prerequisites

The following assumptions are made:

* You have a Raspberry Pi with camera module.
* You have Raspbian installed.
* The Pi can access the internet.

## Installation

> **NOTE:** Read through `./bin/setup` to understand what the installation script does. It will **override** your `cron` configuration.

1. On your Raspberry Pi, clone this repository to a location of your choice. For example to the `~/Code` directory.

    ```sh
    mkdir ~/Code; # Create the "Code" directory
    git clone https://github.com/tmcinerney/timelapse.git; # Clone this repository
    ```
1. Navigate to the `timelapse` directory.

    ```sh
    cd timelapse
    ```
1. Run the `setup` command.

    ```sh
    ./bin/setup
    ```
1. Keep an eye on the output. If it succeeds you will be prompted to reboot for the camera module to work.

    ```sh
    sudo reboot
    ```
1. Once your Raspberry Pi has rebooted, your device should be configured to:
    * Capture a picture **every 2 minutes**.
    * Stitch together captured pictures into a video **daily at 8am**.
    * Both captured pictures and videos are located in `./output`.

## Usage

TODO

## References
* https://www.raspberrypi.org/documentation/usage/camera/raspicam/timelapse.md
* https://raspberrypi.stackexchange.com/questions/14229/how-can-i-enable-the-camera-without-using-raspi-config
