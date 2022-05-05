``` bash
docker run \
-d \
--name code-server \
--restart always \
-p 10000:8080 \
-v $PWD/config.yaml:/home/coder/.config/code-server/config.yaml \
-v $PWD/project:/home/coder/project \
colinchang/code-server:dotnet6-node14
```