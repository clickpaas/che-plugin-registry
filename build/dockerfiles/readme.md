#离线build建议在新加坡服务器,本地太慢
docker build -f build/dockerfiles/Dockerfile --no-cache -t registry.bizsaas.net/eclipse/che-plugin-registry:offline-7.3.0 --target offline-registry 
#离线build完成,再在本地加上配置文件的修改
docker build -f build/dockerfiles/Dockerfile.patch --no-cache -t registry.bizsaas.net/eclipse/che-plugin-registry:offline-7.3.0-patch1 

