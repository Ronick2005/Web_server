# Developing a Simple Webserver

# AIM:

Name: Ronick Aakshath P\
Ref./Reg. No.: 22007303

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
<h2>Name: Ronick Aakshath P</h2>
<h2>Ref./Reg. No.: 22007303</h2>
<h3>List of Web Frameworks:</h3>
<ul>
<li>Django<img src="https://raw.githubusercontent.com/github/explore/7456fdff59816d37ef383a6c8f32a26ff7332db2/topics/django/django.png" style="width:100px;height:100px"></li>
<li>Flask<img src="https://miro.medium.com/max/800/1*Q5EUk28Xc3iCDoMSkrd1_w.png" style="width:100px;height:100px"></li>
<li>Node.JS<img src="https://cdn.pixabay.com/photo/2015/04/23/17/41/node-js-736399__480.png" style="width:100px;height:100px"></li>
<li>Angular JS<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Angular_full_color_logo.svg/1200px-Angular_full_color_logo.svg.png" style="width:100px;height:100px"></li>
<li>Laravel<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Laravel.svg/985px-Laravel.svg.png" style="width:100px;height:100px"></li>
<li>Ruby on Rails<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Ruby_On_Rails_Logo.svg/1200px-Ruby_On_Rails_Logo.svg.png" style="width:200px;height:100px"></li>
</ul>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
```

# OUTPUT:
![output_img](output_img.png)
# RESULT:

The program is executed succesfully
