# Java RMI Hello World

[Java RMI - Getting Started](https://docs.oracle.com/javase/8/docs/technotes/guides/rmi/hello/hello-world.html)

## How to use

### Compile
```
javac -cp bin/ src/example/hello/*.java
```

### Run

Registry:
```
rmiregistry -J-Djava.rmi.server.useCodebaseOnly=false &
```

Server:
```
java -cp bin/ -Djava.rmi.server.useCodebaseOnly=false -Djava.rmi.server.codebase=file:$(pwd)/bin/ example.hello.Server
```

Client:
```
java -cp bin/ -Djava.rmi.server.useCodebaseOnly=false -Djava.rmi.server.codebase=file:$(pwd)/bin/ example.hello.Client
```

Note: You may have to expand the $(pwd) first.