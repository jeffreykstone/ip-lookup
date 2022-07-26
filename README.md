# ip-lookup
microservice to extract details from the user IP address 

Video walkthrough of service: https://media.oregonstate.edu/media/1_sxkl4p2i

Clone the repository in terminal: gh repo clone jeffreykstone/ip-lookup
or with an IDE/GitHub Desktop.

From your shell in the root directory (ip-lookup) run: npm install express geoip-lite --save

Of the dependencies, Express will be used to handle http requests and Geoip-lite will be used for IP lookup.

Next, from the root directory run: node app.js

You should see "IP Lookup service started!" in the console/terminal.

Next you need to sign up for and install NGROK: https://ngrok.com/download

Open another terminal and from the root directory, run: ./ngrok http 5001 (or whatever port you decide to use).

You should see something similar to this, except with your details:

<img width="812" alt="Screen Shot 2022-07-25 at 6 04 30 PM" src="https://user-images.githubusercontent.com/19604067/180900491-ddeb36c1-1eb7-4034-8f6c-9244e4207aa7.png">

Copy the ngrok.io connection link that is forwarding to localhost, paste it into a browser and add /lookup at the end.

For example, in my case: https://8fda-50-238-179-130.ngrok.io/lookup

You should now see the location (based on your IP) similar to such (my location at the time):

<img width="492" alt="Screen Shot 2022-07-25 at 6 09 28 PM" src="https://user-images.githubusercontent.com/19604067/180900932-924d3d53-da44-4b51-b84e-04d193444b10.png">

UML sequence diagram:

![Sequence Diagram Client and Server Parallel Call Example (1)](https://user-images.githubusercontent.com/19604067/180911371-a9d0c029-e819-48be-afff-397118aecf77.jpg)
