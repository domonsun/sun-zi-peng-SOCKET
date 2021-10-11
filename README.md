# sun-zi-peng-SOCKET
#coding: utf-8

import socket
s=socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
s.connect(('127.0.0.1',8888))
print('I am connecting the scrvcr!')
for data in ['aBch','f服务d','h7Tq','.']:
    s.sendto(data.encode(''utf-8),('127.0.0.1',8888))
    str1 = s.recv(1024).decode('utf-8')
    print('the original string is:',data'\tthe processed string is:',str1)
s.close()
