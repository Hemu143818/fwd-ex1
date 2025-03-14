# EX01 Developing a Simple Webserver
## Date:14-03-2025
## Name:KUNATI HEMANTH YADAV
## Reg : 212224100033
## AIM:
To develop a simple webserver to serve html pages and display the simple layout .

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:

```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Skyline Solutions</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f0f0f0;
        }
        header, footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 15px 0;
        }
        main {
            padding: 20px;
            background: white;
            margin: 20px auto;
            border-radius: 8px;
            max-width: 800px;
            box-shadow: 0 0 5px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <header>
        <h1>Skyline Solutions</h1>
        <p>Innovating Technology in New York & San Francisco</p>
    </header>

    <main>
        <h2>About Us</h2>
        <p>Skyline Solutions is a leading tech company providing cutting-edge web solutions to clients across New York and San Francisco. Our mission is to empower businesses through innovative digital experiences.</p>
        
        <h2>Services</h2>
        <ul>
            <li>Web Development</li>
            <li>Cloud Computing</li>
            <li>Artificial Intelligence Solutions</li>
            <li>Data Security & Analysis</li>
        </ul>
    </main>

    <footer>
        <p>&copy; 2025 Skyline Solutions | Serving New York & San Francisco</p>
    </footer>
</body>
</html>



"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()


```

## OUTPUT:
![image](https://github.com/user-attachments/assets/0d66fe7b-a581-4f8e-be9f-1ef5ec4b70c6)

![image](https://github.com/user-attachments/assets/43a27518-2189-42db-aed2-038cce1afb69)




## RESULT:
The program for implementing simple webserver is executed successfully.

