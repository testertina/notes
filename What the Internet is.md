# What the Internet is

The internet: computers linked together.

The websites: webpages linked together using links.

Intranet: Local network

## Making requests

Application layer: Apps written in computer languages.
Transport Layer: TCP, the delivery of the information.
Network layer: IP (internet protocol) the way information is made.
Data Link layer: Wifi/Ethernet
Physical layer: Cables transfers data using binary.

Google search will go from app layer to physical layer, get the answer and then do the trip from app layer to physical layer again to return the answer to the user.

Client requests to server, server responds to client.

Client-side = browser = JS
Server-side = computer = Ruby


### What requests can we make of a server?

CRUD: Create, Read, Update, Delete.

Requests have a url and verb. i.e. get google.com
Request: get i.e. Nneji in google.com
Patch partially changes something.
Put completely changes something.

Request: restful routes.

index | get | /todos
show | get | /todos/:id
create | post | /todos
update | put/patch | /todos/:id
delete | Delete | /todos/:id

### HTTP

How to send information on the internet.

Verbs: Get, Post, Delete, Put and Patch.

### DNS

Each domain name is assigned an IP address, when google.com is typed into the browser it finds the IP address associated with that domain name and calls the webpage.


## MVC
Model e.g. argos gremlin (gets data)
View e.g. makes the data pretty
Controller e.g. manages the data collection

defines how we write our code.

When request returns a JSON or XML from server it is API. Updates a part of page.
When request returns HTML its a webapp. Reloads page.

user input goes into server (below)

router 

controller

model (which goes to the databse outside of the server)

controller

view

user recieves

Server can have multiple controllers, view and models.

```
# get request to / then run "Hello World!"
get "/" do
	"Hello Tina!"
end
```

```
# To return HTML instead of just text.
get "/" do
	"<h1>Homepage</h1>"
end
```
