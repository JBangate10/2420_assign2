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
> wget https://github.com/caddyserver/caddy/releases/download/v2.6.2/caddy_2.6.2_linux_amd64.tar.gz
> tar xvf caddy_2.6.2_linux_amd64.tar.gz
> sudo chown root: caddy
> sudo cp caddy /usr/bin/
