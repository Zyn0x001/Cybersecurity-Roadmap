## Socket Programing 

    import socket

    target_ip = "127.0.0.1" # Localhost
    ports = [21, 22, 80, 443]

    for port in ports:
    # 1. Create a socket object (The Phone)
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

    # 2. Set a timeout so we don't wait forever
    s.settimeout(1)

    # 3. Try to connect (The Dial)
    result = s.connect_ex((target_ip, port))

    if result == 0:
        print(f"Port {port} is OPEN")
    else:
        print(f"Port {port} is CLOSED")
    
    # 4. Hang up

    s.close()
