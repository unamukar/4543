```bash
#!/bin/sh
sudo yum update -y
sudo amazon-linux-extras install docker -y
sudo systemctl enable docker
sudo systemctl start docker
sudo docker container run --publish 8888:80 --name ec2api --restart unless-stopped --detach secobau/4399-ec2api
```
