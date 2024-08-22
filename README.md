# SimpleConcurrentWebServer

## Overview
SimpleConcurrentWebServer is a basic multi-threaded web server built in Java. It serves HTML, CSS, JavaScript files, and image files encoded in Base64. The server supports multiple concurrent client requests and can also handle POST requests to save text data to a file.

## Features
- **Concurrent Request Handling**: Utilizes a thread pool to manage multiple client connections simultaneously.
- **File Serving**: Serves HTML, CSS, JavaScript, and image files (PNG, JPG, JPEG) directly from the local disk.
- **Base64 Image Encoding**: Converts image files to Base64 for embedding in HTML responses.
- **POST Request Handling**: Accepts and processes POST requests to save data to a text file on the server.

## Project Structure
```
SimpleConcurrentWebServer/
│
├───src/
│   ├───main/
│   │   ├───java/
│   │   │   └───edu/
│   │   │       └───escuelaing/
│   │   │           └───arep/
│   │   │               └───ASE/
│   │   │                   └───app/
│   │   │                       └───SimpleWebServer.java
│   │   └───resources/
│   │       ├───index.html
│   │       ├───style.css
│   │       ├───script.js
│   │       ├───image.png
│   │       └───... (other resources)
│   └───test/
│       └───java/
│           └───edu/
│               └───escuelaing/
│                   └───arep/
│                       └───ASE/
│                           └───app/
```


## How to Run

1. **Ensure You Have Java Installed**:
   - Make sure you have JDK installed on your system. You can check your Java version by running:
     ```bash
     java -version
     ```

2. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo/SimpleConcurrentWebServer.git
   cd SimpleConcurrentWebServer
   ```

3. **Compile the Source Code**:
   - Compile the Java source files using the `javac` command:
     ```bash
     javac -d bin src/main/java/edu/escuelaing/arep/ASE/app/SimpleWebServer.java
     ```

4. **Run the Web Server**:
   - After compiling, start the web server by running:
     ```bash
     java -cp bin edu.escuelaing.arep.ASE.app.SimpleWebServer
     ```

5. **Access the Web Server**:
   - Open your web browser and navigate to:
     ```
     http://localhost:8080
     ```
   - The server will serve files located in the `src/main/resources/` directory.

6. **Stop the Server**:
   - To stop the server, press `Ctrl + C` in the terminal where the server is running.

## Configuration
- **Web Root Directory**: The server serves files from the `src/main/resources/` directory by default.
- **Port**: The server listens on port `8080` by default.
- **Thread Pool**: The server uses a thread pool with a fixed size of 10 threads to handle concurrent requests.

## What Was Built
This project includes the following built-in functionalities:
- A simple HTTP server capable of handling GET requests for various file types (HTML, CSS, JavaScript, images).
- POST request handling to save text data into files on the server.
- Concurrent handling of client requests using Java threads.
- Base64 encoding for images embedded in HTML responses.
![image](https://github.com/user-attachments/assets/63a4532c-34d3-45f4-b30f-9c373c505ee3)
![image](https://github.com/user-attachments/assets/83e7b049-55b5-415f-94be-0dc0403f5a90)
![image](https://github.com/user-attachments/assets/311325fb-3abc-45a0-b5ec-164b547aaf4c)
![image](https://github.com/user-attachments/assets/4be3a49f-712b-4cea-937c-b396e81bd338)


## Key Differences from Sequential Servers
- **Concurrent Handling**: Unlike sequential servers that process one request at a time, this server can handle multiple requests concurrently, improving performance and responsiveness.
- **Non-Blocking I/O**: The server's non-blocking I/O allows it to continue accepting and processing new connections while handling ongoing requests.
- **Improved User Experience**: With concurrent request handling, users experience less delay and better responsiveness when accessing the server.

## Author
This project was developed by Juan Esteban Ortiz https://github.com/juaneortiz1.
