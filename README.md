**rpi-leds** Set Raspberry Pi LEDs states on boot.

Of course, doing something in /etc/rc.local is simpler. But if we do it during
init, LEDs are set much much before end of boot process ;-) . 
