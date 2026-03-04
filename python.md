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

## Brute Force Logic

    # Simulated password to crack
    real_password = "secret123"

    # Our "Dictionary" of guesses
    wordlist = ["password", "admin", "123456", "secret123", "football"]

    # Loop through the list
    for guess in wordlist:
        if guess == real_password:
            print(f"Success! Password found: {guess}")
            break
            else:
            print(f"Failed attempt: {guess}")

## File Heandling [File I/O]

    # python can be used to perform operations on a file. (read & write data)

    ### Types of all files
    # 1. Text Files : .txt, .docx, .log etc.
    # 2. Binary Files : .mp4, .mov, .png, .jpeg etc.

    ### Open, read & close File [Note_:_We_have_to_open_a_file_before_reading_or_writing.]

#### Basic Syntext              
    f = open("file_name", "mode")
    data = f.read()
    f.close()

    [**mode**]
    r : read mode(default)
    w : open fo writing, truncating the file first
    x : crate a new file and open it for writing
    a : open for writing, appending to the end of the file if it exists
    b : binary mode
    t : text mode(default)
    + : open a disk file for updating (reading and writing)

#### Reading a file 

Example : 

    f = open("example.txt", "r")
    data = f.read()
    data = f.read(5)    [It will read only 5 letter]
    data = f.readline()   (it will read one line at a time)

#### Writing to a file

##### write

Example: 

    f = open("example.txt", "w")
    data = f.write("You add input here")

##### append

Example: 

    f = open("example.txt", "a")
    data = f.write("You add input here")


