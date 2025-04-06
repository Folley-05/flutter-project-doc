# 📡 REST API Documentation – Domotique Server

This file documents all available HTTP endpoints exposed by the server.  
API version: `v1`  
Base URL: `http://localhost:8080/api/v1/`

---

## Overview of Routes

| Method | Route                        | Description                                 |
|--------|------------------------------|---------------------------------------------|
| GET    | `/hello`                     | Test endpoint to receive a hello message    |
| GET    | `/test`                      | Returns a welcome message                   |
| GET    | `/temperature`               | Accepts and returns a raw JSON body         |
| POST   | `/houselist`                 | Lists all available houses                  |
| POST   | `/roomlist/<idHouse>`        | Lists rooms in the given house              |

---

##  GET `/hello`

### Description
Returns a simple message.  
Used to verify that the server is up.

### Response
```text
Hello, World!
