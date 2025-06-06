# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL
## AIM
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
import socket
s = socket.socket()
s.bind(("localhost", 8000))
s.listen(5)
c, addr = s.accept()
while True:
    i = input("Enter a data: ")
    c.send(i.encode())
    ack = c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break

## OUPUT:
![330068105-569c3c4a-1361-49b8-9c1d-4646aaed6139](https://github.com/user-attachments/assets/42b85998-ec5d-4d91-9fe7-9e7bbae85161)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed
