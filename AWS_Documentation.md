# AWS_documentation

Amazon Aws Documentation

Java Installations:
Step 1:   Download Latest Java Archive

> cd /opt/

> wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u151-b12/e758a0de34e24606bca991d704f6dcbf/jdk-8u151-linux-x64.tar.gz"

> tar xzf jdk-8u151-linux-x64.tar.gz


Step 2:  Install Java 8

> cd /opt/jdk1.8.0_151/

> alternatives --install /usr/bin/java java /opt/jdk1.8.0_151/bin/java 2

> alternatives --config java


Step 3:  Setup Java Environment Variables

Setup JAVA_HOME, JRE_HOME and PATH environment variables

> java -version

> export JAVA_HOME=/opt/jdk1.8.0_151

> export JRE_HOME=/opt/jdk1.8.0_151/jre

> export PATH=$PATH:/opt/jdk1.8.0_151/bin:/opt/jdk1.8.0_151/jre/bin

Note: Also put all above environment variables in /etc/environment file for auto loading on system boot.




Maven Installations:

> wget http://mirror.olnevhost.net/pub/apache/maven/maven-3/3.0.5/binaries/apache-maven-3.0.5-bin.tar.gz

> tar xvf apache-maven-3.0.5-bin.tar.gz

> mv apache-maven-3.0.5  /usr/local/apache-maven

>  export M2_HOME=/usr/local/apache-maven

> export M2=$M2_HOME/bin 

> export PATH=$M2:$PATH

>  mvn -version












