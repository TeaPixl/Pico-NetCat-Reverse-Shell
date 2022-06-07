# Pico-NetCat-Reverse-Shell

The Pico `NetCat` Reverse Shell script uses a `Raspberry Pi Pico` as a USB `Rubber Ducky`

## What is a Rubber Ducky?

A Rubber Ducky is a hacking tool used to act as a `HID-compliant device` (like a keyboard) and injects a payload using it (Like in Mr.Robot!)

Check out [dbisu's Pico-Ducky](https://github.com/dbisu/pico-ducky) and [Hak5](https://shop.hak5.org/)

**NOTE, THIS IS ALL FOR EDUCATIONAL PURPOSES ONLY**
I am not held liable for any misuse of this script!

## Installation

To install the Payload, first you will need to install the [Pico-Ducky](https://github.com/dbisu/pico-ducky) [CircuitPython](https://circuitpython.org/) software.

1.Download the `CircuitPython` [.uf2](https://circuitpython.org/board/raspberry_pi_pico/) file and install it on your Pico.

2.Then you can download the `adafruit-circuitpython-bundle-7.x-mpy-YYYYMMDD.zip`
Extract the `adafruit_hid` folder from the `lib` folder of the downloaded file.
Put the `adafruit.hid` folder inside of the Pico's `lib` folder.

3. Then, save [this](https://raw.githubusercontent.com/dbisu/pico-ducky/main/duckyinpython.py) and save it as `code.py` and put it inside the Pico's root.

4. Finally, download the [payload.dd](https://github.com/TeaPixl/Pico-NetCat-Reverse-Shell/blob/main/payload.dd) file and save it as payload.dd on your Pico's root.

To create your own Payloads, you can use the [USB-Rubber-Ducky-Wiki](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Duckyscript) by [Hak5](https://shop.hak5.org/) and create your own `payload.dd` files and upload them to the Pico.

Here is a great video by [NetworkChuck](https://www.youtube.com/c/NetworkChuck/featured) showing how to install the `Rubber Ducky` [here](https://www.youtube.com/watch?v=e_f9p-_JWZw&ab_channel=NetworkChuck).

## Setup

In order to Reverse Shell a `Windows` Computer, you will want a [Linux](https://en.wikipedia.org/wiki/Linux) server listening to a specific port with `NetCat`
You will want to fill in the `IP-ADDRESS-HERE` and `PORT-HERE` with the port of your choice (preferably under 1000 to help avoid firewall detection) and the IP of your `Linux Server`

### On the Linux Terminal

```stty raw -echo; (stty size; cat) | nc -lvnp PORT-HERE```
And replace the `PORT-HERE` with the port of your choice

## Usage
Take the Bad USB and plug it into a computer you own while the `Linux server` is listening,
It will disable `Windows Security` temporarily and execute the script quickly.

Then it is safe to unplug your USB and go to your `Linux` machine
You should then have a fully interactive `Windows Terminal` with control over the computer!.

## Known Issues
Occasional unreliability and disconnection, cause is unknown
