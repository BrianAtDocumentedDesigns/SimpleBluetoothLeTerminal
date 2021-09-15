This is a fork of https://github.com/kai-morich/SimpleBluetoothLeTerminal

My hardware is ESP32-C3 based and that code does not support ESP32 so I managed to port it over and got it working with the esp32_spp_server.cpp demo which espressif provides.  (see https://github.com/BrianAtDocumentedDesigns/SimpleBluetoothLeTerminal/tree/ESP32_C3_SPP_Support). 

I am pretty sure the ESP32 spp server does not implement flow control so I set 

            writeCredits = Integer.MAX_VALUE;

as a sort of a kludge.

I know I am not much of a programmer but I thought I'd let you know in case you were interested in incorporating support for the popular ESP32 family into your code.

I will probably add flow control to the ESP32 code when I make some progress on my project.

Here is the readme from the https://github.com/kai-morich/SimpleBluetoothLeTerminal

==============================


# SimpleBluetoothLeTerminal

This Android app provides a line-oriented terminal / console for Bluetooth LE (4.x) devices implementing a custom serial profile

For an overview on Android BLE communication see 
[Android Bluetooth LE Overview](https://developer.android.com/guide/topics/connectivity/bluetooth/ble-overview).

In contrast to classic Bluetooth, there is no predifined serial profile for Bluetooth LE, 
so each vendor uses GATT services with different service and characteristic UUIDs.

This app includes UUIDs for widely used serial profiles:
- Nordic Semiconductor nRF51822  
- Texas Instruments CC254x
- Microchip RN4870/1
- Telit Bluemod

## Motivation

I got various requests asking for help with Android development or source code for my
[Serial Bluetooth Terminal](https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal) app.
Here you find a simplified version of my app.
