#### asgi and wsgi is bot act act as bridges between web server and python web application 

# WSGI (web server gateway interface)

Wsgi : is stand for web server gateway interface and is sutable for synchronous programming or application

1. Wsgi is syncchronous handling one request at one time and blockeing acecutions untile processing is complete

2. HTTP : Wsgi spport only HTTP request and laking webSocket support

3. server :Gunicorn and mod_wsgi

4. wsgi is handle request individually usinf processes or threads(પ્રક્રિયાઓ અથવા થ્રેડો)

5. Protocol Support : HTTP/1.1

6. middleware : wsgi middleware is synchronous and they impacting performance in asynchronous application

## use case

1.REST api : API focusing CRUD opretions without real-time applications
2.Low-to-Moderate Traffic Applications,Low user, bloging web site etc


# ASGI (asynchronous server gateway interface)

Asgi : is a asynchronous server gateway interface is suitable for asynchronous applications. it support long lived application ,webSockets and other non-HTTP protocols

1. Asgi : is asynchronous handling multipuls requests at one time any whitout bloking any other request

2. Asgi is recommended long lived conneactions

3. HTTP : Thay support a both HTTP and websocket and real time application

4. server : Daphne and Uvicorn

5. Protocol Support:HTTP/1.1 , HTTP/2 , and websockets

6. middleware : asgi middleware is asynchronous it spport for asynchronous applications


### Use case:
1.Real-time Chat Applications: like wensocket for messaging platform,chatbots etc

2.Live Notifications Systems
3.Collaborative Tools: Google Docs-style applications requiring real-time synchronization use ASGI for seamless collaboration

4. Financeial trading Platforms :real time market data



# django overview

### 1.Django with wsgi
django not a wsgi is use as primary deployment platforms for handling synchronous web requests and Django treditionally use gunicorn they providing stability for conventional web applications

### 2. Django with Asgi
django intreduced asgi support version 3.0 .enabling asynchronous views and middleware. However, critical limitations exist:

### 3.ORM Limitations
Django's ORM is not fully asynchronous-safe and requires sync_to_async wrappers, which can introduce performance overhead

### 4. Asgi handleinf High concurrency is expecte

### Choose WSGI When:
Building traditional web applications or simple APIs

Performance for individual requests is critical

Team expertise is primarily in synchronous development

Simple deployment and maintenance are priorities

WebSocket functionality is not required

### Choose ASGI When:
Real-time features are essential (chat, notifications, live updates)

High concurrency is expected

WebSocket support is required

Building modern, interactive applications

Long-lived connections are needed

