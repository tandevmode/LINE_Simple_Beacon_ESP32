# LINE_Simple_Beacon_ESP32
Arduino code for LINE Simple Beacon work with ESP32

This is fixed version of original source from
https://engineering.linecorp.com/ja/blog/detail/149/?fbclid=IwAR19FZud8YY5wNpAYfeQ9gvV3DI6bG8xOb95T8dFc8IkR6E6XM12EWUN4DI

## FIXED
* Stack overflow in MAX_BLE_ADVERTISING_DATA_SIZE declare.
* Fix static void updateSimpleBeaconDeviceMessage(char dm[], int dmsize) to support full length of device message(13 byte).

## Prerequisites
* [Create a channel on the LINE Developers console](https://developers.line.me/en/docs/line-login/getting-started/)
* [Install Arduino IDE](https://www.arduino.cc/en/main/software)

## Setup
* Install ESP32s Boards Manager
    * Preferences > Additional Boards Manager URLs > add
    ```
    'https://dl.espressif.com/dl/package_esp32_index.json'
    ```
    * Tools > Boards Manager > search 'esp32' > Install
* [Issue LINE Simple Beacon Hardware ID](https://admin-official.line.me/beacon/register)

## Steps
* Update Hardware ID
* Adjust the signal length
* Upload the code to hardware