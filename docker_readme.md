https://stackoverflow.com/questions/72528606/docker-rancher-permission-denied-when-using-docker-from-wsl


sudo addgroup --system docker
sudo adduser $USER docker
newgrp docker
# And something needs to be done so $USER always runs in group `docker` on the `Ubuntu` WSL
sudo chown root:docker /var/run/docker.sock
sudo chmod g+w /var/run/docker.sock

```
