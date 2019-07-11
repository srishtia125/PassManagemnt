Pass Management Assignment

This assignment is designed on spring-boot framework and in-memory database H2 database.

Installation
Download the zip file and unzip it or 
Clone the source code/download from folder and unzip
git clone https://github.com/srishtia125/PassManagemnt.git

Go to the checked out source code and start the server locally (Server will start on port 8080 , make sure no other is using the same port)
path :  \PassManagemnt\leisure-pass-demo\leisure-pass-demo

command: mvn spring-boot:run

Once the server is started,
http://localhost:8080/swagger-ui.html#/

APIs
# Add new customer /cutomer
returns customer details

# Add new Vendor /vendor
returns vendor details

# Add new Pass /pass
This Api returns the pass details.
customernotfoundexception is thrown when wrong customer  is provided 
vendornotfoundexception is thrown when wrong vendorid  is provided 

# Renew exisisting Pass /renew/{passId}
This Api returns the pass details with pass status as Active.

Test Cases
Execute mvn test command to run test cases:

test if passnotfoundexception is thrown when wrong passid  is provided 
test if passcancelledexception is thrown when wrong pass is in cancelled status 
test if pass is renewed and active status is returned using passid

# Cancel exiisting Pass /cancel/{passId}
This Api returns the pass details with pass status as Cancelled

Test Cases
Execute mvn test command to run test cases:

test if passnotfoundexception is thrown when wrong passid  is provided 
test if passcancelledexception is thrown when pass is in cancelled status 
test if pass is cancelled and cancelled status is returned using passid

# validate  Pass /validate
This Api returns the pass details as ACTIVE if valid pass exists


Test Cases
Execute mvn test command to run test cases:

test if passnotfoundexception is thrown when wrong passid  is provided 
test if passcancelledexception is thrown when wrong pass is in cancelled status 
test if pass is renewed and active status is returned using passid
