# Serverless User Management App

This Serverless application provides user management functionalities, including user registration, login, and car management operations. Users can perform actions such as creating, deleting, editing, and retrieving information about cars.

## Table of Contents

- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
- [User Management](#user-management)
    - [Register](#register)
    - [Login](#login)
- [Car Management](#car-management)
    - [Create Car](#create-car)
    - [Delete car by ID](#delete-car)
    - [Get Car by ID](#get-car)
    - [Get Car List](#get-all-cars)
    - [Edit Car by ID](#edit-car)


## Getting Started

### Prerequisites

- Node.js
- Serverless Framework
- AWS account and AWS CLI configured

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Harut-dev/user-management-serverless.git

2. Install dependencies:
    ```bash
   cd user-management-serverless
   npm install
   
3. Deploy the Serverless application:
    ```bash
   serverless deploy

## User Management

### Register
To register a new user, make a POST request to the registration endpoint:
```bash 
curl -X POST https://your-api-gateway-url/user/signup -d '{"email": "your_gmail@gmail.com", "password": "your_password"}'
```

### Login
To log in, make a POST request to the login endpoint:
```bash 
curl -X POST https://your-api-gateway-url/user/login -d '{"email": "your_gmail@gmail.com", "password": "your_password"}'
```


## Car Management

### Create Car
To create a new car entry, make a POST request to the create car endpoint:
```bash 
curl -X POST https://your-api-gateway-url/car/create -H "Authorization: Bearer your_access_token" -d '{"license_plate": "your_license_plate", "model": "your_model", "brand": "your_brand"}'
```

### Edit Car by ID
To edit information about a car, make a PUT request to the edit car endpoint:
```bash 
curl -X PUT https://your-api-gateway-url/car/edit/{id} -H "Authorization: Bearer your_access_token" -d '{"license_plate": "your_license_plate", "model": "your_model", "brand": "your_brand"}'
```

### Get Car by ID
To retrieve information about a specific car, make a GET request to the get car endpoint:
```bash 
curl -X GET https://your-api-gateway-url/car/get/{id} -H "Authorization: Bearer your_access_token" 
```

### Get Car List
To get a list of all cars, make a GET request to the get all cars endpoint:
```bash 
curl -X GET https://your-api-gateway-url/car/list -H "Authorization: Bearer your_access_token" 
```

### Delete car by ID
To delete a car, make a DELETE request to the delete car endpoint:
```bash 
curl -X DELETE https://your-api-gateway-url/car/delete/{id} -H "Authorization: Bearer your_access_token" 
```