```
1   yum -y install java-1.8.0-openjdk java-1.8.0-openjdk-devel
    2  cat > /etc/profile.d/java8.sh <<EOF 
    2  export JAVA_HOME=$(dirname $(dirname $(readlink $(readlink $(which javac)))))
    3  export PATH=\$PATH:\$JAVA_HOME/bin
    4  export CLASSPATH=.:\$JAVA_HOME/jre/lib:\$JAVA_HOME/lib:\$JAVA_HOME/lib/tools.jar
    5  EOF



    3  cat > /etc/profile.d/java8.sh <<EOF 
    2  export JAVA_HOME=$(dirname $(dirname $(readlink $(readlink $(which javac)))))
    3  export PATH=\$PATH:\$JAVA_HOME/bin
    4  export CLASSPATH=.:\$JAVA_HOME/jre/lib:\$JAVA_HOME/lib:\$JAVA_HOME/lib/tools.jar
    5  EOF

    4  cat > /etc/profile.d/java8.sh <<EOF 
export JAVA_HOME=$(dirname $(dirname $(readlink $(readlink $(which javac)))))
export PATH=\$PATH:\$JAVA_HOME/bin
export CLASSPATH=.:\$JAVA_HOME/jre/lib:\$JAVA_HOME/lib:\$JAVA_HOME/lib/tools.jar
EOF

    5  cd /usr/local
    6  yum install wget
    7  wget http://www-us.apache.org/dist/maven/maven-3/3.5.4/binaries/apache-maven-3.5.4-bin.tar.gz
    8  sudo tar xzf apache-maven-3.5.4-bin.tar.gz
    9  sudo ln -s apache-maven-3.5.4  maven
   10  cat > /etc/profile.d/maven.sh <<EOF
export M2_HOME=/usr/local/maven
export PATH=${M2_HOME}/bin:${PATH}
EOF

   11  source /etc/profile.d/maven.sh
   12  history
   13  git clone https://github.com/ricardozanini/soccer-stats
   14  yum install git
   15  git clone https://github.com/ricardozanini/soccer-stats
   16  ls
   17  cd 
   18  cd /home/ec2-user/
   19  ls
   20  git clone https://github.com/ricardozanini/soccer-stats
   21  mvn clean package
   22  /usr/local/maven/bin/mvn clean install
   23  ls
   24  cd soccer-stats/
   25  ls
   26  /usr/local/maven/bin/mvn clean install
   27  ls
   28  cd target/
   29  ls
   30  java -jar target/soccer-stats-0.0.2.war
   31  java -jar soccer-stats-0.0.2.war

```
