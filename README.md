# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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

#### Client side:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

#### Server side:
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
#### Client:

![Screenshot 2024-04-20 174016](https://github.com/KrishnaPrasad148/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147332763/12e2c4e7-b3b1-48e0-8406-55cb0404f334)

#### Server:

![Screenshot 2024-04-20 174119](https://github.com/KrishnaPrasad148/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147332763/b5ae2520-f2c9-4afc-a554-85d791c88bde)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
