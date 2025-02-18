This is a fork of the flask file server by Wildog at https://github.com/Wildog/flask-file-server/fork.

It's only modified to add the mechanics required to be a "block" in BalenaHub.

The intent of the block is to allow download of files found in the directory mounted as a 
share between containers in Balena.

Env vars:
FS_BIND = Param for bind address, default 0.0.0.0  
FS_PORT = Param for server port, default 8000  
FS_PATH = Param for serve path, default /tmp  
FS_KEY = Param for authentication key as base64 encoded username:password, default none  

Below is the original README.md
------------------------------------------------------------------------------------

#flask-file-server

A flask file server with an elegant frontend for browsing, uploading and streaming files

![screenshot](https://raw.githubusercontent.com/Wildog/flask-file-server/master/screenshot.jpg)

## Build
```docker build --rm -t maaydin/flask-file-server:latest .```

## Run
```docker run -p 8000:8000 maaydin/flask-file-server```

## Params
FS_BIND = Param for bind address, default 0.0.0.0  
FS_PORT = Param for server port, default 8000  
FS_PATH = Param for serve path, default /tmp  
FS_KEY = Param for authentication key as base64 encoded username:password, default none  

```docker run -p 8000:8000 -e FS_BIND=0.0.0.0 -e FS_PORT=8000  -e FS_PATH=/tmp -e FS_KEY=dGVzdDp0ZXN0 maaydin/flask-file-server```

