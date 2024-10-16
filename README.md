# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
Name: AMIRTHAVARSHINI V
REGISTER NUMBER:212223040014
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
Client:
![Screenshot 2024-10-16 140740](https://github.com/user-attachments/assets/998e6dd4-c523-47dd-ba1b-7b56d276c370)


Server:
![Screenshot 2024-10-16 140756](https://github.com/user-attachments/assets/d93dc9d1-8a88-4def-be3e-44c523b7e18c)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
