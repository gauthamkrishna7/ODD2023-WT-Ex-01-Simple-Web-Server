# Ex-01-Simple-Web-Server
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
 from http.server import HTTPServer,BaseHTTPRequestHandler

 content='''
< !doctype html>
 <html>
 <head>
 <title> My Web Server</title>
 </head>
 <body>
 <h1>Top Five Web Application Development Frameworks</h1>
 <h2>1.Django</h2>
 <h2>2. MEAN Stack</h2>
 <h2>3. React </h2>
 <h2>4. Ruby</h2>
 <h2>5. Spring</h2>
 </body>
 </html>
 '''

 class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

 print("This is my webserver") 
 server_address =('',8080)
 httpd = HTTPServer(server_address,MyServer)
 httpd.serve_forever()
```
## OUTPUT:
![serveroutput](https://github.com/gauthamkrishna7/ODD2023-WT-Ex-01-Simple-Web-Server/assets/141175025/7758986d-596c-4299-b681-fd5f70cf82a2)
![clinetouput](https://github.com/gauthamkrishna7/ODD2023-WT-Ex-01-Simple-Web-Server/assets/141175025/01b90c7e-41f5-47c2-b4bc-733e243c68ff)


## RESULT:
The program for implementing simple webserver is executed successfully.
