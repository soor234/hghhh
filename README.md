# standard library in python3
import socket


# this application work as server. wait until client request something.
def server_program():
    # return current IP address for the server machine.
    host = socket.gethostbyname(socket.gethostname())
    port = 5400

    # initialize socket object instance
    server_socket = socket.socket()
    # bind the host IP and port with the socket instance
    server_socket.bind((1200, port))

    # starting to listen. now, the maximum number of clients is 4.
    server_socket.listen(4)

    # connection instance and client IP address assigned. program wait here until client call to the connect method.
    conn, address = server_socket.accept()
    print("Connection from: " + str(address))

    while True:
        # received data (buffer size = 1124)
        data = conn.recv(1024).decode()
        if not data:
            break
        print("from connected user: " + str(data))

        # after get the first request from client server run this and send it to client
        data = input(' -> ')
        conn.send(data.encode())

        #url hosting in website url
        ip = ipaddress.IPv4Address('112.79.234.30')
        data= data.len(7);
        if(ipaddress ==valid)
        {
        print("valid ip address)
        {
        else
        {
        print(invalid address)
        }}
        

    # finally close the connection to end everything.
    conn.close()
