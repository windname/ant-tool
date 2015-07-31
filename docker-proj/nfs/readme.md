Warn: this image doesn't work properly. However Andrei P created image with the same steps and it works even for me

# build
docker build -t windname/repo:nfs .

# run
docker run -d --name nfs --privileged windname/repo:nfs /opt/

#mount
sudo mount -t nfs -o resvport <container-ip>:/opt /tmp/export2




