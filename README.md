# pythonProject37


#server
import socket
while True:
    try:
        s = socket.socket()
        s.bind(("0.0.0.0", 1337))
        s.listen()

        print("you got listing!")

        cs, c_addres = s.accept()
        cs.send("hii to the server!".encode())
        massge = (cs.recv(2048).decode())
        print(massge)
        #s.send((cs.recv(2048).decode).encode())
        s.send(massge(2048).encode())


    except:
        massge == "exit"
        break
    finally:
        cs.close()
        s.close()
