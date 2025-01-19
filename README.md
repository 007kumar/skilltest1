
Cloud and Containers
Microservices on EC2


# Microservices Project

This project consists of four microservices: Gateway Service, Order Service, Product Service, and User Service. 
Each service is containerized using Docker and can be managed using Docker Compose.

## Project Structure

Microservices
  ├── gateway-service
  │   ├── Dockerfile
  │   ├── app.js
  │   └── package.json
  ├── order-service
  │   ├── Dockerfile
  │   ├── app.js
  │   └── package.json
  ├── product-service
  │   ├── Dockerfile
  │   ├── app.js
  │   └── package.json
  └── user-service
      ├── Dockerfile
      ├── app.js
      └── package.json

## Prerequisites

- Docker
- Docker Compose
- Node.js

## Setup

Create your docker-compose.yml in Root directory under Microservices
and Dockerfile user all the four servcies i.e. gateway-service,  order-service,  product-service and user-service

1. **Clone the repository**:
   ```bash
   git clone https://github.com/007kumar/skilltest1.git
   cd Microservices
2. Install Dependencies
   ```bash
   npm install
Build and start all services   
#Building and Running Services Individually for all the 4 services (Need to run below commands while we are in main project directory i.e. Microservices)
```bash

#Gateway Service
cd gateway-service
sudo docker build -t gateway-service .
sudo docker run -d -p 3003:3003 --name gateway-service gateway-service

#order Service:
cd order-service
sudo docker build -t order-service .
sudo docker run -d -p 3002:3002 --name order-service order-service

#product service:
cd product-service
sudo docker build -t product-service .
sudo docker run -d -p 3001:3001 --name product-service product-service

#user Service
cd user-service
sudo docker build -t user-service .
sudo docker run -d -p 3000:3000 --name user-service user-service
```

later it can be tested using curl command and also on browser (Please make sure you have allowed all the ports in security groups)
curl http://Public-IP:3003
curl http://Public-IP:3002
curl http://Public-IP:3001
curl http://Public-IP:3000












