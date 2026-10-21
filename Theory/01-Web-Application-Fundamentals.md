# Web Applications — Fundamentals

## 1. Web Application

A **web application** is an application that is accessed through a web browser.

### Application Types

- **Desktop Applications:** Applications that are directly installed on a computer/system.
- **Web Applications:** Applications that are accessed through a web browser, generally using the internet.

### Examples of Web Applications

- [YouTube](https://www.youtube.com/)
- [Flipkart](https://www.flipkart.com/)
- [Amazon](https://www.amazon.in/)

---

## 2. Working of a Web Application

A web application mainly works through communication between a **client** and a **server**.

### Server

A server is responsible for making the web application accessible to users.

It also handles application processing and data storage. Storing and processing large amounts of data entirely on a user's local system is generally not practical.

A server can contain:

- Application/backend code
- Application data
- Database
- Business/application logic
- Processing operations

### Client

The **client** is usually a web browser such as Chrome, Edge, Firefox, or Safari.

The basic flow is:

```text
Client / Browser
       |
       | Request
       v
     Server
       |
       | Process Request
       v
     Server
       |
       | Response
       v
Client / Browser
```

### Request-Response Cycle

1. The client sends a request to the server.
2. The server accepts the request.
3. The server processes the request.
4. The server sends a response back to the client.
5. The client displays or uses the response.

---

# 3. Web Application Development

Web application development can broadly be divided into:

1. **Frontend**
2. **Backend**

---

## 3.1 Frontend

The **frontend** is the part of the application that the user interacts with through the browser.

It is responsible for the **user interface (UI)** and client-side behaviour.

### HTML

**HTML — HyperText Markup Language**

HTML is used to create the **structure or skeleton** of a web page.

Whatever is structurally present and displayed in a browser is built using HTML.

Examples:

- Headings
- Paragraphs
- Buttons
- Forms
- Images
- Links
- Tables

### CSS

**CSS — Cascading Style Sheets**

CSS is used to **style and design** a web page.

It controls things such as:

- Colors
- Fonts
- Spacing
- Layout
- Size
- Positioning
- Responsive design
- Animations

### JavaScript

**JavaScript** is used to add **logic, behaviour, and interactivity** to a web page.

It can perform operations on the browser/client side, such as:

- Handling button clicks
- Validating forms
- Updating webpage content
- Manipulating the DOM
- Making requests to servers
- Processing client-side logic

### Frontend Technologies

Some commonly used frontend technologies include:

- HTML
- CSS
- JavaScript
- React.js
- Tailwind CSS
- Angular

> Note: React.js, Angular, and Tailwind CSS are tools/frameworks/libraries built around or used with the core web technologies.

---

# 3.2 Backend

The **backend** is the processing part of a web application and generally runs on the server.

It handles:

- Application logic
- Business logic
- Data processing
- Database operations
- Authentication and authorization
- Communication with the frontend

### Application Logic

Application logic defines **how the application should behave** when it receives a request.

Backend applications can be developed using technologies such as:

- JavaScript / Node.js
- Java
- Python
- PHP
- C#
- And others

### Database

A database is used to store and manage application data.

Examples:

- MySQL
- MongoDB
- PostgreSQL
- Oracle Database

---

# 4. Client and Server

The client and server communicate using a **request-response model**.

```text
┌──────────────┐
│    Client    │
│ Web Browser  │
└──────┬───────┘
       │
       │ Request
       ▼
┌──────────────┐
│    Server    │
│              │
│ App Logic    │
│ Database     │
└──────┬───────┘
       │
       │ Response
       ▼
┌──────────────┐
│    Client    │
│ Web Browser  │
└──────────────┘
```

### Request-Response Steps

1. The **client sends a request** to the server.
2. The **server accepts and processes** the request.
3. The **server sends a response** to the client.

---

# 5. Technical Aspects of Request and Response

## 5.1 Request

A request contains information that tells the server what the client wants.

### 1. Server Address / URL

To send a request, the client needs to know where the request should be sent.

This is generally specified using a **URL (Uniform Resource Locator)**.

Examples:

```text
192.168.1.2
https://www.flipkart.com/
https://www.amazon.in/
```

A URL can identify the server and the specific resource/endpoint being requested.

### 2. Request Method

The **HTTP request method** indicates the purpose of the request.

Common HTTP methods include:

| Method | Common Purpose |
|---|---|
| `GET` | Retrieve data |
| `POST` | Send/create data |
| `PUT` | Replace/update data |
| `PATCH` | Partially update data |
| `DELETE` | Delete data |
| `OPTIONS` | Ask about supported communication options |

---

# 5.2 Response

The server sends a response back to the client after processing a request.

A response generally contains:

1. **Data / Response Body**
2. **Status Code**
3. **Status Message / Reason Phrase**

### Status Code

The status code tells the client what happened when the server processed the request.

HTTP status codes are grouped into five categories:

| Range | Category | Meaning |
|---|---|---|
| `100–199` | Informational | Request received / processing |
| `200–299` | Success | Request processed successfully |
| `300–399` | Redirection | Further action/redirection required |
| `400–499` | Client Error | Problem with the request/client side |
| `500–599` | Server Error | Problem while processing on the server |

### Common Status Codes

| Code | Meaning |
|---:|---|
| `200` | OK |
| `201` | Created |
| `202` | Accepted |
| `301` | Moved Permanently |
| `302` | Found / Temporary Redirect |
| `400` | Bad Request |
| `401` | Unauthorized |
| `403` | Forbidden |
| `404` | Not Found |
| `500` | Internal Server Error |
| `502` | Bad Gateway |
| `503` | Service Unavailable |

> **Important:** A `4xx` status generally indicates that the request could not be fulfilled because of something related to the client/request, while a `5xx` status generally indicates that the server encountered a problem while fulfilling a valid request.

---

# 6. Complete Web Application Flow

```text
                    WEB APPLICATION
                          |
            ┌─────────────┴─────────────┐
            │                           │
         FRONTEND                    BACKEND
            │                           │
     ┌──────┼──────┐              ┌─────┴─────┐
     │      │      │              │           │
    HTML   CSS  JavaScript    App Logic    Database
     │      │      │              │           │
     └──────┼──────┘              └─────┬─────┘
            │                           │
            ▼                           ▼
        CLIENT  ─────── Request ─────> SERVER
        Browser  <────── Response ───── SERVER
```

### Example

Suppose a user opens an online shopping website and searches for a product.

```text
1. User enters a search term
          ↓
2. Browser creates an HTTP request
          ↓
3. Request is sent to the server
          ↓
4. Backend receives the request
          ↓
5. Backend processes the search
          ↓
6. Backend communicates with the database
          ↓
7. Database returns matching products
          ↓
8. Server creates the response
          ↓
9. Response is sent to the browser
          ↓
10. Frontend displays the products
```

---

## 7. Key Takeaways

- A **web application** is accessed through a web browser.
- The **client** is usually the browser.
- The **server** handles application processing and data-related operations.
- **HTML** provides structure.
- **CSS** provides styling and layout.
- **JavaScript** provides logic and interactivity.
- The **backend** handles server-side processing and application logic.
- A **database** stores and manages application data.
- Clients communicate with servers using **requests and responses**.
- HTTP methods such as `GET`, `POST`, `PUT`, `PATCH`, and `DELETE` describe the purpose of requests.
- HTTP status codes communicate the result of a request.
on that application

client: a web browser -> will send a request on server -> server accepts the request -> server will process the request -> respond to the client


Development:
1. Frontend: UI screen
	     HTML: Hyper Text Markup Language: is used to create a skeleton/structure
		    Whatever is visible on the browser is created using html 

	     CSS: cascading style sheet :  style a web page

	     JAVASCRIPT: to perform any operation on the browser/client side 

	     React Js
	     Tailwind Css
		Angular


2. Backend: processing part -> server -> App Logic + Database 

	App Logic:JavaScript 
	Database: MySQL, Mongo DB


Client and Server
Request and response 

1. Client will send a request to server
2. Server will accept the request and will process it
3. Server will send the response to the client 

Technical Aspects of Request and Response:

Request:
1. If we have to send a request, then we need the address/url of a server
	ip address 192.168.1.2 / www.flipkart.com / www.amazon.in

2. Request Method: Purpose of the request -> GET POST PUT DELETE PATCH OPTIONS

Response:
1. Data will be there
2. Status: Using status a client is going to know what happened at the server side with the request. 
Server along with the data will always give the status also.

Status -> Code + Message
	  200 201 202 ... 299
	  300 301 302 ... 399
	  400 401 402 ... 499 failure is due to client
	  500 501 502 ... 599 failure due to server

	  200 OK
          400 BAD REQUEST , 401 UNAUTHORIZED
          500 INTERNAL SERVER ERROR 
