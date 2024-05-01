# 3b.CREATION FOR CHAT USING TCP SOCKETS

### NAME:- ESWANTH KUMAR K
### REG NO:- 2122230400046

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## Server:;
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT:
## Client:
![image](https://github.com/eswanth2005/3b_CHAT_USING_TCP_SOCKETS/assets/164656722/e971a6f9-601c-450e-8a1c-d4ece2e42d5d)

## Server:
![image](https://github.com/eswanth2005/3b_CHAT_USING_TCP_SOCKETS/assets/164656722/4bb1f1d3-32a2-4e47-92eb-b550434d580c)

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
