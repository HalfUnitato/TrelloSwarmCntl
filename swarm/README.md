# Tello EDU Swarm Control

- Tello 2.0 SDK

## Tello in AP Mode

all Tello drones need to be in AP mode

for each Tello drone:

1. connect to Tello-WiFi
2. exec ´python set-ap-mode.py -s [SSID] -p [PASSWORD]´

after that Trello will reboot and connect to the new WiFi-network

## Controlled Flight

´python planned-flight.py -f cmds-01.txt´

## Reset WiFi

1. turn the TELLO on until its flashing yellow rapidly
2. ress and hold the power button for 5-8s until the led goes off
3. then reconnect after it auto rebooting
4. edit the cmis-xx.txt file to your needs

```bash
# scan for available drenes
# scan:
#   number of drones
#   ip-adr "range"
scan 1 192.168.32.
battery_check 20
correct_ip
…
```
