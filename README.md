# docker compose for traefk and halo

使用 traefik 做 ssl 自动签名以及代理 halo 的 docker compose 编排方案

## 使用方法

1. 修改`docker-compose.yml`文件
   - ALICLOUD_ACCESS_KEY=
   - ALICLOUD_SECRET_KEY=

2. 修改`traefik/dynamic.yml`文件
   - 将 yourdomain.com 替换为你的域名
   - 将 basic-auth 中 的 users 替换为你的用户名以及密码
   - basic-auth 使用 htpasswd 方式生成
   - htpasswd 使用方法: htpasswd -nb username password

3. 修改`traefik/traefik.yml`文件
   - 将 email 修改为你的 email 地址

4. 数据默认保存在当前目录的`data`下
   - 可以在`docker-compose.yml`中修改映射位置

5. enjoy it.
