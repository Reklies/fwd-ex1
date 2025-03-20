# EX01 Developing a Simple Webserver
## Date:20/03/2025

NAME : Reklies J

REG NO: 212223110041


## AIM:
 To develop a vibrant webserver that serves colorful HTML pages showcasing and explaining the TCP/IP Protocol Suite protocols.

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
~~~
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """

<!DOCTYPE html>

<html lang="en">

  <head>

  <meta charset="UTF-8">
  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <title>My Attractive Website</title>
  
  <style>
  
    /* Global Styles */
    body {
    
      margin: 0;
      font-family: 'Arial', sans-serif;
      
      background: #f5f5f5;
      color: #333;
      
      line-height: 1.6;
    }

    
    
    /* Header Section */
    header {
    
      background: linear-gradient(135deg, #6a11cb, #2575fc);
      
      color: #fff;
      
      padding: 60px 20px;
      
      text-align: center;
    }
    
    header h1 {
    
      margin: 0 0 10px;
      
      font-size: 2.5rem;
    }
    
    
    header p {
    
      margin: 0;
      
      font-size: 1.2rem;
    }
    
    /* Navigation */
    
    nav {
      background: #333;
    
      padding: 10px 20px;
      
      text-align: center;
    }
    
    
    nav a {
    
      color: #fff;
      
      text-decoration: none;
      
      margin: 0 15px;
      
      font-weight: bold;
    }
    
    
    nav a:hover {
    
      color: #f5f5f5;
    }
    
    
    /* Main Content Container */
    
    .container {
    
      max-width: 1000px;
      
      margin: 20px auto;
      padding: 0 20px;
    }
    
    
    section {
    
      margin: 40px 0;
    }
    
    
    /* Card Style for Content Sections */
    
    .card {
    
      background: #fff;
      border-radius: 8px;
      
      padding: 20px;
      
      margin-bottom: 20px;
      
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
    
    
    .card h2 {
    
      margin-top: 0;
    }
    
    
    /* Footer Section */
    footer {
    
      background: #333;
      
      color: #fff;
      
      text-align: center;
      
      padding: 20px;
    }
    
    
    /* Responsive Adjustments */
    @media (max-width: 600px) {
    
      nav a {
      
        margin: 0 10px;
        
        font-size: 0.9rem;
      }
      
      
      header h1 {
      
        font-size: 2rem;
      }
      
    }
    
  </style>
</head>
<body>
  
  <header>
    
    <h1>Welcome to My Website</h1>
    
    <p>Simple, Clean &amp; Responsive Design</p>
  
  </header>
  
  <nav>
   
    <a href="#">Home</a>
    
    <a href="#">About</a>
    
    <a href="#">Services</a>
    
    <a href="#">Contact</a>
  </nav>
  
  <div class="container">
    
    <section>
    
      <div class="card">
      
        <h2>About Us</h2>
        <p>This is a simple website created using HTML and CSS. The layout is clean, attractive, and responsive—perfect for showcasing your content.</p>
      </div>
    </section>
    <section>
      <div class="card">
    
        <h2>Our Services</h2>
        
        <p>We offer high-quality web design and development services to help your business stand out online. Our approach focuses on simplicity and user-friendliness.</p>
      </div>
    </section>
  </div>

  
  <footer>
  
    <p>&copy; 2025 My Attractive Website</p>
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
~~~

## OUTPUT:

![Screenshot 2025-03-18 112153](https://github.com/user-attachments/assets/cfadae8e-34f8-4cb3-a137-65b0fd4c53bd)

![Screenshot 2025-03-18 112133](https://github.com/user-attachments/assets/cc6a5231-a258-4a5e-9844-658935927af9)


## RESULT:
The program for implementing simple webserver is executed successfully.

