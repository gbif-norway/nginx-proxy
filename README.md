# From https://blog.ssdnodes.com/blog/host-multiple-websites-docker-nginx/

Every time you add a new Docker container to your network, nginx-proxy sees the event through the socket, automatically creates the configuration file needed to route traffic, and restarts nginx to make the changes available immediately.

The proxy looks for containers with the VIRTUAL_HOST variable enabled. In that variable you specify the destination, like blog.example.com or app.example.com. The proxy will see that person A has requested blog.example.com and will route (or proxy!) their request to the correct container. Same goes for app.example.com or any other containers you want to run.

This docker-compose includes the letsencrypt companion for ssl. 

Run with `sudo docker-compose up --build -d`
