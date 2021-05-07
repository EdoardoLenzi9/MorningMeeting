# Setup environment variables

```cmd
set JAVA_HOME=C:\Program Files\Java\jdk1.8.0_171
set JRE_HOME=%JAVA_HOME%\jre
set CLASSPATH=%CLASSPATH;%JAVA_HOME%\lib
set PATH=%PATH%;%JAVA_HOME%\bin
```

in order to make the set persistent use `setx` (with `/M` if you want to set System Scope instead of User Scope)

```cmd
setx /M PATH "%PATH%;%JAVA_HOME%\bin"
```

# Java compilation

```tree
.
+--> HelloWorld.java
+--> utils/
     +--> Utils.java
```

```sh
# standard compilation
javac HelloWorld.java utils/Utils.java

# order doesn't matter
javac HelloWorld.java utils/Utils.java

# compile separately (order matter)
javac utils/Utils.java 
javac HelloWorld.java

# it is not possible to compile HelloWorld.java alone!
```

# Launch application

```sh
# java <MainClass>  // without .java
java HelloWorld
```

# JAR Creation

```sh
jar [OPTION ...] [ [--release VERSION] [-C dir] files]
-c --create
-t --list      list of contents that will be included
-v --verbose
-x --extract   extract a jar
```

```sh
javac HelloWorld.java utils/Util.java
jar -cvfe jar HelloWorld.jar *.class utils/*.class
```