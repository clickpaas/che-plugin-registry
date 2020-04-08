
#离线build建议在新加坡服务器,本地太慢
docker build -f build/dockerfiles/Dockerfile --no-cache -t registry.bizsaas.net/eclipse/che-plugin-registry:offline-7.3.0 --target offline-registry .

#离线build完成,再在本地加上配置文件的修改

##需要特别注意有的配置文件指向本地的资源eg: v3/plugins/redhat/java11/latest/meta.yaml
docker build -f build/dockerfiles/Dockerfile.patch --no-cache -t registry.bizsaas.net/eclipse/che-plugin-registry:7.3.0-offline-patch1 .

