#To run this collection locally, Newman needs to be installed first, and then to generate the HTML report, we need to install the Newman reporter.

#Newman: It's a command-line tool created by Postman, which allows you to run and test collections from the command line

Install Newman: **npm install -g newman** 
Install Newman reporter: **npm install -g newman-reporter-html**

Here in this repo, I have defined the baseURL as an environment variable in Postman itself to secure my IP address and port, so before running the collection, directly set the baseURL like this: 

=>Run this before running the collection with your IP address and port: **set BASEURL=http://your_IP:your_Port/opencart/upload/index.php?route=**

=> Now, to **run** the collection **locally** on your system, run this command: 

**newman run <<collection-name.json>> --env-var "baseUrl=%BASEURL%"**

=> To generate **HTML reports** run this command:

**newman run <<collection-name.json>> -r html --env-var "baseUrl=%BASEURL%"**

