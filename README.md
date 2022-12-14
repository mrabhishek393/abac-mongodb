# Enabling Attribute-based Access Control in NoSQL Databases
 
Team Members :- 

Aaidan Ram Meghwal - 191CS101

Abhishek Singh - 191CS103

Bhumik Naveen - 191CS216

## Steps to setup ruby and Mongodb  and run project on your system :- 

1. Download and install ruby. [rubyinstaller](https://rubyinstaller.org/)
2. Run the following command `gem install bundler` in the main directory to install all the related dependencies.
 3. Download and install Mongodb [mongodb](https://www.mongodb.com/try)
4. Create a new database in Mongodb.
5. Create two new Mongodb collections employee and inventory and insert a single row in each collection.

In employee: {"_id":"8942e04f3a64bb33f893dOde","department":"HR","salary":"100000"}

In inventory: {"_id":"7524e04f3a64bb89f893dOde","item":"card","qty":"18"}

6. Run the following command in the main directory →                               `ruby  lib/mongo-abac.rb`


## Files : -


1. mongo-abac.gemspec → contains all the modules needed to run the project, hence should be installed beforehand.
2. mongo-abac.rb → main file which needs to be run.
3. ca.pem → contains the certificate of the user.
4. pk.pem → contains the public key of CAA.
5. encrypted_key.txt → contains the encrypted key of the user generated by CAA. The cipher used is AES in the CBC mode with a 256-bit key encryption.
6. encrypted_ua.txt → contains the encrypted attributes of the user generated by CAA.
7. config.json → contains the configuration for rules and attributes.
8. user_attributes.json → contains the attributes of authorized users.
9. object_attributes.json → contains the attributes of object user is trying to access.
10. policy.json → contains the abac policy rules by which a user is given access or not is decided.
11. wire.rb → contains the code to interact to mongodb and perform actions such as find, insert, delete, update,etc.
12. auth.rb → to authenticate the users using certificate and keys.
13. proxy.rb → contains the main logic to intercept and evaluate the message that client has sent to the mongodb.
14. mongo-proxy folder → it contains the proxy library of ruby to set up the proxy.


