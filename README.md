# esp32-s
Repository to study ESP32 board functionalities.

![ESP-WROOM-32](./esp32-wroom-pinout)

## Get Started with ESP-IDF

- [Install, build and flash](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html)

- Proccedure to build and flash (in a nutshell):
```
cd ~/esp
cp -r $IDF_PATH/examples/get-started/blink .

cd ~/esp/blink
idf.py set-target esp32
idf.py menuconfig (choose GPIO2, please!)

idf.py build
ls /dev/tty*
idf.py -p /dev/tty/USB0 flash monitor
Ctrl+] (exit the program)
```

### :exclamation::boom: Issues
-  [Permission denied tty](https://github.com/esp8266/source-code-examples/issues/26)
```
groups
sudo usermod -a -G tty yourname
sudo usermod -a -G dialout yourname

... and you have to logout/login to get group addition happens.
```
or type:
``` bash
sudo chmod a+rw /dev/ttyUSB0
```

# Support Material - Videos
- [Get started with ESP-IDF](https://www.youtube.com/watch?v=7-hJGuJMrY0) (linha de comando)
- Get started with ESP-IDF VS Code Extension 
  - [Pedro Minatel](https://www.youtube.com/watch?v=yvbeDSDY73Y) (more complete)
  - [Fabio Souza](https://www.youtube.com/watch?v=rxMg_zxO0q0) (more objective)
