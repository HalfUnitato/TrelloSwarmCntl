# Tello EDU Swarm Control

- Tello 2.0 SDK

## Tello in AP Mode

all Tello drones need to be in AP mode

for each Tello drone:

1. connect to Tello-WiFi
2. exec ´python set-ap-mode.py -s [SSID] -p [PASSWORD]´

after that Trello will reboot and connect to the new WiFi-network

## Controlled Flight

´python planned-flight.py -f cmd_files/cmds-01.txt´

## Reset WiFi

1. turn the TELLO on until its flashing yellow rapidly
2. press and hold the power button for 5-8s until the led goes off
3. then reconnect after it auto rebooting

## Cmd-Files

```bash
## scan for available drones
# scan:
#   number of drones
#   ip-adr "range" (optional)
scan 1 192.168.32.

## make battery-check
# if battery-lvl is below -> abort
battery_check 20

## assignes serialnumber to ip
correct_ip
…

## assign serialnumber to drone-command-nr
0=0TQZGANED0021X
1=0TQZGANED0020C

## drone command
# '*' = all
# 'x' = drone-command-nr
*>takeoff
x>takeoff
```
