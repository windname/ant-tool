docker run -p 22 -it windname/repo:ssh

-- mounted folder opt from docker container to /tmp/share3 on host
sshfs root@172.17.0.75:/opt /tmp/share3


-- ubuntu not tested
pre-install
yum install fuse sshfs
-- apt-get install sshfs

sudo apt-get install sshfs
sudo modprobe fuse
sudo adduser maythux fuse
sudo chown root:fuse /dev/fuse
sudo chmod +x /dev/fusermount
