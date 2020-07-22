Accelerate SSH connection speed and upload and download files through Ptinyvpn.

#server start:  
./ptinyvpn -s -l0.0.0.0:8096 -f20:10 -k "603aM8l1uStJ2Aj" --sub-net 10.22.22.0 --tun-dev tun100 --report 10 --mode 1

#client start:  
./ptinyvpn -c -r44.55.66.77:8096 -f20:10 -k "603aM8l1uStJ2Aj" --sub-net 10.22.22.0 --tun-dev tun100 --report 10 --mode 1 --keep-reconnect


#Server:Test client Ping values  
ping 10.22.22.2

#Client:Test server Ping values  
ping 10.22.22.1

#Server SSH transfer files  
scp -r /root/scripts/udp2/psocks5 root@10.22.22.2:/root


#client SSH transfer files  
scp -r /root/scripts/udp2/psocks5 root@10.22.22.1:/root

#

