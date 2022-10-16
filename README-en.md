<div align="left">
 Русский язык: <a title="Русский" href="README.md"><img src="https://upload.wikimedia.org/wikipedia/commons/f/f3/Flag_of_Russia.svg" height="11px"/>
</div>

# USB Port Tester.
![alt text](https://github.com/g42/USB-Tester/blob/main/images/tester_2.4-sch-2.png)

This tester combines two functions:
* Checking the data lines of a USB port for the presence of a short circuit or low resistance.
* Indication of device initialization, via the USB bus.

The tester shows initialization even in the absence of image output but with a working CPU, PCH, RAM, and BIOS. 
If the video system, screen, or video output channel is faulty, the tester will show initialization. It also allows you to test system boards without assembling the device and connecting the screen.

When connecting the tester to the port of a switched-off device with normal line resistance, the tester remains in sleep mode until power appears on the USB bus. When power appears, the INIT indicator starts blinking slowly. After successful initialization and polling of the USB bus, the tester emits a short beep and the INIT indicator starts blinking rapidly.

After initialization, the NUM LOCK status is duplicated by the SHORT indicator. This allows you to make sure that the USB is working correctly: switch the NUM LOCK mode from the keyboard - the tester will show whether the mode is currently active. No special drivers are required — the tester emulates a standard HID keyboard.

By default, the tester emulates the periodic pressing of the CAPS LOCK button, which allows you to control the "hang" of the device by the flickering of the caps indicator on the keyboard. 
You can disable blinking caps by pressing the button on the tester. Pressing again emulates keyboard input. Press the button again to return to the caps flashing mode.

Checking for the line resistance is performed automatically when the tester is connected to the USB connector. If there is a short circuit, the tester emits a continuous beep and the "SHORT" indicator lights up. This allows you to quickly perform primary diagnostics of a hub (PCH) or, for example, a U-series processor with a built-in hub. At the same time, there is a small delay before the indication (less than 1 second). This is necessary to charge the parasitic capacity of the line and exclude a false alarm. At normal line resistance, the tester remains in sleep mode. The indicators are not involved in this case.

Since, in most cases, there is no power supply voltage on the faulty USB ports, the tester has a built-in battery, which is necessary for measuring the resistance on the signal lines. Its charging is possible from any suitable PSU or device if there is a 5V on the USB connector. The full charge time is about 1 hour. In the non-working state (when the tester is not connected anywhere), the charge is not consumed. There is an indication of the battery charge. To check, press the button on the tester. 1 short beep and 1 flashing INIT will follow if the battery charge is normal. Either 3 short beeps and 1 blinking SHORT if the battery is low. If there is no reaction to the button, then the battery is in a deep discharge state or the tester is faulty. When the battery is low, incorrect measurements are possible.

The tester's protective shell is intended to protect the tester and the device against ESD. Also, there is a USBLC6 protection IC.

The width of the tester is 17 mm, which allows you to use nearby USB connectors to connect other devices.

For any questions, please contact by email <a href="mailto:20kohm@gmail.com">20kohm@gmail.com</a>