Install Newman: **npm install -g newman** 
Install Newman reporter: **npm install -g newman-reporter-html**

=>Run this before running the collection with your IP address and port:

**set BASEURL=http://your_IP:your_Port/opencart/upload/index.php?route=**

=> Now, to **run** the collection **locally** on your system, run this command: 

**newman run <<collection-name.json>> --env-var "baseUrl=%BASEURL%"**

=> To generate **HTML reports** run this command:

**newman run <<collection-name.json>> -r html --env-var "baseUrl=%BASEURL%"**

Comment: BaseUrl was an env variable in Postman itself, so we  need to define when we have to run the collection.
