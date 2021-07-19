# What is this script?
Script that waits for a ready TCP / UDP connection, can be used to synchronize services like docker containers.

### Usage

Wait for TCP connection on host `127.0.0.1` and port `3306` to be ready.
Timeout is 60 sec with retries every 5 sec.

```
./wait-for 127.0.0.1:3306 -t 60 -i 5
```
or
```
./wait-for 127.0.0.1:3306 --timeout=60 --interval==5
```

There is also possibility to start a program once check is successfull:
```
./wait-for 127.0.0.1:3306 --timeout=60 --interval==5 -- echo "Database ready"
```

### Installation
1. Download `wait-for` script
1. Execute it by calling `./wait-for` with expected parameters


### Inspiration
Script was inspired by [this](https://github.com/eficode/wait-for) repository.
