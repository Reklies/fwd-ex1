# EX01 Developing a Simple Webserver
## Date:14-03-2025
## NAME : BOOBESH PM
## REG NO: 212222233001
## AIM:
To develop a simple webserver to serve html pages and to create a simple web page

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
    <title>Simple Webpage</title>
</head>
<body>
    <header>
        <h1>Welcome to My Simple Webpage</h1>
    </header>
    
    <main>
        <p>This is a simple HTML page to demonstrate basic structure.</p>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
        </ul>
        <p>Thanks for visiting!</p>
    </main>

    <footer>
        <p>&copy; 2025 Simple Webpage</p>
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
![Screenshot 2025-03-14 141043](https://github.com/user-attachments/assets/e23e0608-9d24-4844-9481-29019912ada4)


## RESULT:
The program for implementing simple webserver is executed successfully.

