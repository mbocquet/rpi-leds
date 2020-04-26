**rpi-leds** Set Raspberry Pi LEDs states on boot.

## Install

Copy rpi-leds.default in /etc/default/rpi-leds :
`cp rpi-leds.default /etc/default/rpi-leds`
Adapt it to your needs.
Copy rpi-leds script in /usr/local/sbin :
`cp rpi-leds /usr/local/sbin`
Ensure its executable.
Copy rpi-leds.service into /etc/systemd/system :
`cp rpi-leds.service /etc/systemd/system`
Reload systemd :
`systemctl daemon-reload`
Enable service : `systemctl enable rpi-leds.service`

start service to apply LED behaviour now :
`systemctl start rpi-leds.service`

Of course, doing something in **/etc/rc.local** is simpler. But if we do it during
init, LEDs are set much much before end of boot process ;-) . 
