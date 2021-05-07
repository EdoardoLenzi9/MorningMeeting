[download here](https://maven.apache.org/download.cgi)

```cmd
set PATH=%PATH%;C:\Code\drive\MorningMeetingRepo\002_ApacheMaven\apache-maven-3.8.1-bin\apache-maven-3.8.1\bin
mvn --version

# execute the maven goal:
mvn archetype:generate ^
    -DgroupId=com.mycompany.app ^
    -DartifactId=my-app ^
    -DarchetypeArtifactId=maven-archetype-quickstart ^
    -DarchetypeVersion=1.4 ^
    -DinteractiveMode=false

mvn dependency:tree
mvn dependency:analysis

mvn install

mvn compile
mvn test 
mvn test-compile

mvn package

mvn clean
mvn site
```