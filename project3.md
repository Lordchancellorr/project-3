## Lordchancellor's Documentation of Project 3

## Implementation of Instructions in Step 1: Project 3
- In this project, I will be implementing a web solution based on MERN stack in AWS Cloud. MERN Web stack consists of the following components: MongoDB, ExpressJS, ReactJS,Node.js. follow the steps below for better understanding
- I ran the following commands on my terminal after connecting my virtual machine on AWS cloud: Please note that it is advisable you use Ubuntu Version 20.04 for the implementation of this project to get positive and effective result. After a succesful connection of my virtual machine, i ran:
- `sudo apt install`
- `sudo apt update`
- `sudo apt upgrade` it looks exactly like this-
 ![sudo apt upgrade](./images/sudo%20apt%20upgrade.PNG)
- To get the location of the Nodejs from Ubuntu Repositories, I ran: [Node js](curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -) 
![curl status](./Images/curl%20status.PNG)

- I Installed nodejs with this command_ `sudo apt-get install -y nodejs`
 ![installation nodejs](./Images/nodejs%20installation.PNG)
- `node -v ` (The output will be the node version)
- `npm -v` [The output will be the npm version]
- Now we need to setup the application code. it is advisable you create a new directory for the todo project. I ran `mkdir Todo` and follow the prompt steps. In my Todo directory, I ran `npm init` to initialise it, a new file named package.json was created.(it contains information about your app and the dependencies it needs to function well), I filled in the neccessary details and then typed yes.
## Implementation of Instructions in Step 2
- As earlier explained, MERN stack consists of some components one of which is Expressjs. to install that, I ran:
- `npm install express`
- Then create a new file with: `touch index.js` 
We need to install the dotenv module. Run `npm install dotenv`- See the image below for better description of the expected output. 

![Dotenv installation](./images/npm%20installation%20dotenv.PNG)
-  I opened the index.js file with this comand -`vim index.js`
 ![Port 5000](./images/Port%205000.PNG)
 inside the file, extract the codes in the picture below and paste it accordingly. 
 ![Index.js](./images/vim%20index.js)
To confirm if my server works, I ran: `node index.js` and the image below was my output - 
- Please endeavor to edit your inbound rules in the security groups and set it to TCP, port 5000 in other to be able to access it on the web using your public IP address like this, http://<PublicIP-or-PublicDNS>:5000(Please edit with your correct Public IP/DNS address). In my browser, I pasted the link. The image below was displayed on my screen.
 ![Express](./images/Welcome%20to%20Express.PNG)
 In other for my Todo application to be able to create a new task, display list of all tasks and delete tasks that are not relevant. I followed the following steps:To create a new directory, I ran `mkdir routes` change your directory to routes, and create a new file inside that routes directory the name it api.js. (some codes were pasted here).
## Implementation of Instructions in Step 3-5
- Another component of MERN stack is MongoDB. But first We will install the Mongoose software by running `npm install mongoose` Then create a new directory with `mkdir models` the change directory to models inside which we create a file with `touch todo.js` (Some commands were pasted here and saved accordingly). We nset up a MongoDB database after creating an account. check the images below for proper steps:
 ![Mongo Database](./images/Setting%20up%20MongoDB%20Database.PNG) 
 ![M.G DB](./images/Continuation.PNG)
 I created a new cluster and connected to the cluster. 
-I set up the connection security
- I chose a connection method and made sure the Driver is on Nodejs and version 3.6 or later. To add my connection string to my application code, copy the already generated code and pasted it in my .env file /Create the .env file in the Todo directory. I  updated <username>, <password>, <network-address> and <database> according to my setup
- There was a modification to the index.js file and the codes were replaced with a new one after which we confirmed if the database was connected successfully. Run `node index.js` The image below was the output:
 ![Successful database connection](./images/Successful%20database%20connection.PNG)
-  Postman was used to test the API and after setting it up, the image below was the output:
![post and Get Request](./images/Post%20andGet%20request.PNG)

![post output](./images/Postman%20Output.PNG)
- The react app was installed with this code on the terminal ` npx create-react-app client` and concurrent( A dependency) was installed with `npm install concurrently --save-dev` 
![Installation of Concurrent](./images/Installation%20of%20Concurrent.PNG) 
  and  nodemon `npm install nodemon --save-dev` 
- Package.json (In the client directory) was configured and completely modified. After creating the src and components directory each with files and respective codes, Axios was instaalled with this command on the terminal `npm install axios`  With multiple modifications to the sub files in src and components directory, the Todo app was fuctional and accesssed on the internet using the public IP on port 3000. 
- Final command was- `npm run dev` and thw image below was the output:

![Final output](./images/npm%20run%20dev%20final%20output.PNG)
-The To-do application was accessed through a web browser and the image below was the output. 

![The To-do Application](./images/My%20Todo%20Application!.PNG)