# 命令启动

docker run -d -v ${PWD}/data/:/etcd-data -p 2379:2379 \
 --restart=always \
 --name etcd0 endlessday3/etcd:v3.3 \
 /usr/local/bin/etcd \
 -name etcd0 \
 -data-dir /etcd-data \
 -advertise-client-urls http://etcd0:2379 \
 -listen-client-urls http://0.0.0.0:2379
 