```bash
#!/bin/sh
sudo yum update -y
sudo amazon-linux-extras install docker -y
sudo systemctl enable docker
sudo systemctl start docker
sudo docker container run --publish 8080:80 --name ec2aws --restart unless-stopped --detach secobau/4399-ec2aws
```
