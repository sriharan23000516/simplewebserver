# EX01 Developing a Simple Webserver
## Date: 15.03.2024

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
from http.server import HTTPServer, BaseHTTPRequestHandler
content = 
<html>
	<head>
		<title>
			SoftWare Companies
		</title>

	</head>
	<body bgcolor= "skyblue" align="center">
		
		<table align="center" border="5" cellspacing="6" cellpadding="5">
			<caption>Top Five Revenue Generating Software Companies</caption>
			<tr>
				<th> S.No </th>
				<th> Company Name </th>
				<th> Revenue </th>
			</tr>
			<tr>
				<td> 1 </td>
				<td> Microsoft </td>
				<td> $86.8 </td>
			</tr>
			<tr>
				<td> 2 </td>
				<td> Oracle </td>
				<td> $67.1 </td>
			</tr>
			<tr>
				<td> 3 </td>
				<td> SAP </td>
				<td> $50.9 </td>
			</tr>
			<tr>
				<td> 4 </td>
				<td> Walmart </td>
				<td> $49.9</td>
			</tr>
			<tr>
				<td> 5 </td>
				<td> Google </td>
				<td> $40.9 </td>
			</tr>
			</table>
	</body>

</html>
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()

```

## OUTPUT:
![web](https://github.com/Thamizhjo/simplewebserver/assets/123891476/26ae3d5a-7182-412b-aab8-de9ac4cf2f60)
![web 1](https://github.com/Thamizhjo/simplewebserver/assets/123891476/a71a2840-42a6-4fe1-90b9-36464b1110e9)

## RESULT:
The program for implementing simple webserver is executed successfully.
