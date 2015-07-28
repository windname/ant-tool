docker build -t windname/repo:tomcat7 .

# start image in background mode
docker run -d -p 8081:8080 -t windname/repo:tomcat7
# see logs
docker logs 6d80ce4a54bd

