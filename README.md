# recon and social engineering to gain access
# social engineering and wifi access

# methods

# 1.

ask if you could quickly use the wifi to call my mom its important "she is sick" or "i need her help" "urgency is important"

# 2.

can i please use the wifi quckly i just need to give "person" money "situation"


# network recon

# first access

ip a for subnet and private ip range

sudo nmap -sS -p- -f -D RND:10 --spoof-mac 0 -n -T3 -v --scan-delay 200ms -oA stealth_scan "ip/subnet"

# enumaration

# 1.
bash script for changing mac to avoid detection just tune it

#!/bin/bash
INTERFACE="wlan0"

while true; do
    ip link set $INTERFACE down
    MAC=$(printf '00:%02X:%02X:%02X:%02X:%02X' $((RANDOM%256)) $((RANDOM%256)) $((RANDOM%256)) $((RANDOM%256)) $((RANDOM%256)))
    ip link set dev $INTERFACE address $MAC
    ip link set $INTERFACE up
    echo "New MAC: $MAC"
    sleep 9000
done
# 2.

Use "OpenVas" or "Nessus" to scan network for vulnrabilties.





