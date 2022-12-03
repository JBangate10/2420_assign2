# ACIT 2420 - Assignment 2
## By: Jose Bangate, A01271709


## Creating Servers using Caddy

### Step 1: Create DO Infrastructure
Follow this video to create a proper DO Infrastructure: (https://vimeo.com/775412708/4a219b37e7)

After following the video, your DO Infrastructure should include the following:
- VPC
- At least 2 Droplets
- Load Balancer (Use the DigitalOcean Load Balancer)
- Firewall (Use the DigitalOcean Cloud Firewall)

### Step 2: Create New Regular User for 2 Droplets
Follow this video below to create a new regular user for both of your newly added Droplets.   
**Tip:** Skip the video to 20:14
(https://learn.bcit.ca/d2l/le/content/877753/viewContent/8037537/View)

### Step 3: Install Caddy on Both Droplets
To install Caddy, run these commands one by one below:   
```
wget https://github.com/caddyserver/caddy/releases/download/v2.6.2/caddy_2.6.2_linux_amd64.tar.gz   
tar xvf caddy_2.6.2_linux_amd64.tar.gz   
sudo chown root: caddy   
sudo cp caddy /usr/bin/
```   

Once installation is complete, you can then begin to configure Caddy configuration file by following    
and running these commands below:   
```
sudo mkdir /etc/caddy
sudo chmod 777 Caddyfile
vim Caddyfile
```   
   
Add the following inside the Caddyfile:   
![Step 3 (1)!](./images/step3(1).png)   

### Step 4: Writing "Web App"
To start, create a new directory (doesn't matter where you create it) on WSL and name it "2420-assign-two".   
![Step 4 (1)!](./images/step4(1).png)   
   
Inside of the "2420-assign-two" directory, create 2 new directories called "html" and "src".   
![step 4 (2)!](./images/step4(2).png)   
   
Inside of the "html" directory, create an "index.html" page by using running the command `vim index.html`.   
and create a simple html document.   
![Step 4 (3)!](./images/step4(3).png)   
   
Inside of the "src" directory, create node project by running these commands below.   
```
npm init   
npm i fastify   
```   
   
After that, create an index.js file by running the command `vim index.js` and add the fastify hellow world program.   
![Step 4 (4)!](./images/step4(4).png)   
   
Next we will be testing the server locally. To be able to do this, we would need to install node first.   
To install node, follow and run these commands below one by one:   
```
curl https://get.volta.sh | bash   
source ~/.bashrc   
volta install node    
which npm
```   
   
After installing node, run the index.js file by running the command `node index.js` in your **Terminal**   
   
### Step 5: Write Caddyfile Server Block on Local Machine
