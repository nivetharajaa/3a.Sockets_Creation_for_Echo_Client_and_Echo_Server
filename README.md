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
### CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
### SERVER
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
### CLIENT
![310374821-5a77e26b-9b29-4ba4-9aa6-4adb0fc01d7a](https://github.com/nivetharajaa/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/120543388/ad53ffa7-b621-4e0d-94ab-2c661201805b)
### SERVER
![310374844-e40feed6-52e8-419f-91c7-ca530494c6da](https://github.com/nivetharajaa/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/120543388/8cee4d39-9cc6-4d9f-8600-d0993fb62c70)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
