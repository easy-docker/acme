# docker-acme
Let's Encrypt acme.sh 脚本

# 使用
显示帮助
```
docker pull ghostry/acme
docker run --rm -it -v ~/.acme:/data ghostry/acme acme
```
例如dnspod泛域名
```
docker run --rm -it \
    -e DP_Id="数字ID" \
    -e DP_Key="Token字符串" \
    -v ~/.acme:/data \
    ghostry/acme acme --issue --dns dns_dp \
    --config-home /data \
    -d 域名 \
    -d *.域名
```