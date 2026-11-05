# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## SEVER:
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
## CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
  msg=input("Client > ") 
  s.send(msg.encode()) 
  print("Server > ",s.recv(1024).decode())
```
## OUPUT
<img width="1330" height="730" alt="image" src="https://github.com/user-attachments/assets/620fcc16-59da-49e7-876d-509d7ffe56ca" />

<img width="1336" height="769" alt="image" src="https://github.com/user-attachments/assets/7b8683aa-ff83-485c-b519-fb0046a97d6e" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
