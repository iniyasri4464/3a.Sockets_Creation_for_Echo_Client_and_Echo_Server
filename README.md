# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Name : Iniyasri.S
## Register number : 212223230081
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## client
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
clientMessage=c.recv(1024).decode()
c.send((clientMessage.encode()))
```
## server 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
msg=input("client>")
s.send(msg.encode())
print("server>",s.recv(1024).decode())
```
## OUPUT
## client
![image](https://github.com/iniyasri4464/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/152419072/f4305d4e-eae9-4ce2-8a00-9cb516f0c5ad)
## server
![image](https://github.com/iniyasri4464/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/152419072/11aaf712-38f6-4655-a4f6-0ad5fa795056)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
