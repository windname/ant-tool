
# start image 
docker run -d --hostname perforce -p 1666 -v /srv/perforce:/data/p4depot --name perforce ambakshi/perforce-server

# get container IP
docker inspect perforce | grep IP

# get account password
docker logs perforce

# installclient
mkdir /usr/local/perforce
chmod +x p4

# add dir for workspace
mkdir /usr/local/perforce/docker_ws
chmod -R 777 /usr/local/perforce/docker_ws

# edit ~/.bash_profile
export P4_HOME=/usr/local/perforce
export PATH=$P4_HOME:$PATH
export P4PORT=ssl:172.17.0.3:1666
export P4USER=p4admin
export P4PASSWD=pass12349ers!
export P4CLIENT=docker_ws


# save changes
source ~/.bash_profile

# add hosts to trust
p4 trust

# run it 
p4 info
