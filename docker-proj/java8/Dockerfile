FROM windname/repo:tubuntu
MAINTAINER Vladimir Grigoriev

ADD jdk-8u51-linux-x64.tar.gz .
ENV JAVA_HOME /jdk1.8.0_51
ENV PATH "$PATH":${JAVA_HOME}/bin

RUN java -version
# RUN wget
