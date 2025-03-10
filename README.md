# recon and social engineering to gain access


# social engineering



# network recon

first access
ip a for subnet and private ip range
sudo nmap -sS -p- -f -D RND:10 --spoof-mac 0 -n -T3 -v --scan-delay 200ms -oA stealth_scan "ip/subnet"
