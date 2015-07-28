docker rmi windname/repo:simple-web
docker build -t windname/repo:simple-web .
docker run -d -p 8080:8080 -t windname/repo:simple-web
