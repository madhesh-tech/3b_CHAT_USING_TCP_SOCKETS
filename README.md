# 3b.CREATION FOR CHAT USING TCP SOCKETS
# Name : MADHESH I
# Reg No: 212224220055
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
CLIENT 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
SERVER
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
## OUPUT
<img width="1699" height="1071" alt="Screenshot 2025-10-03 085635" src="https://github.com/user-attachments/assets/c66b32a4-8894-4a77-900d-053b96cc5579" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
