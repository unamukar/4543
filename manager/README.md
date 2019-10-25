```bash
#!/bin/sh
sudo yum update -y
sudo amazon-linux-extras install docker -y
sudo systemctl enable docker
sudo systemctl start docker
# PUT BELOW THE OUTPUT OF LEADER DEPLOYMENT (token manager)
sudo docker swarm join --token XXXXXXXXXX X.X.X.X:2377
```
