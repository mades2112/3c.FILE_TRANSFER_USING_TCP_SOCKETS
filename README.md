# 3c.CREATION FOR FILE TRANSFER USING TCP SOCKETS
## AIM
To write a python program for creating File Transfer using TCP Sockets Links
## ALGORITHM:
1. Import the necessary python modules.
2. Create a socket connection using socket module.
3. Send the message to write into the file to the client file.
4. Open the file and then send it to the client in byte format.
5. In the client side receive the file from server and then write the content into it.
## PROGRAM
CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
SERVER:
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
## OUTPUT
CLIENT:

![Uploading 313486071-30ff104d-40e6-45a6-8b6c-225ed5948653.png…]()


SERVER:

![313486054-f9990833-595a-48ce-9674-6b3ed0c7ae95](https://github.com/mades2112/3c.FILE_TRANSFER_USING_TCP_SOCKETS/assets/152461996/7850c618-64c9-4d60-ae83-03d178c6ffd2)

## RESULT
Thus, the python program for creating File Transfer using TCP Sockets Links was 
successfully created and executed.
