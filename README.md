# OpenCart_API_Testing

- This is an API collection, including test validations for the OpenCart Web Application APIs related to cart functionality, and it includes APIs for different Cart functionalities (Add product, Edit Cart, Delete Product from Cart). This collection was created using the Postman tool. 
  
- Test validations are added in the test tab of the Postman tool itself, which utilizes the Chai.js library for testing. All APIs are chained using variables defined at either the Environment level or on the collection level in the tool.

# Installation
Before installing anything, ensure that Node and npm are installed on the local system.
To run the collection on the local system and generate reports, these two packages need to be installed:
## Install Newman:
```
npm install -g newman
```
## Install Newman reporter: 
```
npm install -g newman-reporter-html
```
## Run this before running the collection with your IP address and port:
```
set BASEURL=http://your_IP:your_Port/opencart/upload/index.php?route=
```
=> Now, to **run** the collection **locally** on your system, replace <<collection-name.json>> with name of the collection and run this command: 
```
newman run <<collection-name.json>> --env-var "baseUrl=%BASEURL%"
```
=> To generate **HTML reports**, again replace <<collection-name.json>> with name of the collection and run this command:
```
newman run <<collection-name.json>> -r html --env-var "baseUrl=%BASEURL%"
```
Comment: BaseUrl was an env variable in Postman itself, so we need to set this variable separately when we have to run the collection.
