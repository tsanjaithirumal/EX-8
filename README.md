# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

### DATE :26-04-2023

### AIM :

# To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

### ALGORITHM :
## 1.Import the necessary modules in python
## 2.Create a socket connection to using the socket module.
## 3.Send message to the client and receive the message from the client using the Socket module ## in server.
## 4.Send and receive the message using the send function in socket.


### PROGRAM :
### CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
 ```
### SERVER:
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


### CLIENT OUTPUT :
![image](https://github.com/tsanjaithirumal/EX-8/assets/119393916/65e4104b-2c80-4032-94eb-bdad9f76b048)

### SERVER OUTPUT :
![image](https://github.com/tsanjaithirumal/EX-8/assets/119393916/5beaae69-3230-4872-9b12-6cd4c1603887)

### RESULT:

## Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
