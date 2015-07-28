FROM windname/repo:java8
MAINTAINER Vladimir Grigoriev

# RUN apt-get install -y tomcat7
ADD apache-tomcat-7.0.63.tar.gz .
ENV CATALINA_HOME /apache-tomcat-7.0.63
EXPOSE 8080

ADD  tomcat-users.xml  $CATALINA_HOME/conf/
CMD $CATALINA_HOME/bin/catalina.sh run

# CMD $CATALINA_HOME/bin/startup.sh
# CMD service tomcat7 start && tail -f /var/lib/tomcat7/logs/catalina.out
