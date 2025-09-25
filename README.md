# n8n 和 postgres

n8n 使用 postgreSQL 做数据库


```markdown
.env: 环境变量参数
.docker-compose.yml Docker 配置文件
.init-data.sh 数据库初试化脚本
```


# 使用方法

1. 下载当前仓库，放在合适的文件夹中（路径不要有中文）
2. 修改 .env 中的变量值
```
# 定义变量
# 数据库 ROOT 角色的用户名、密码
POSTGRES_USER=<用户名>
POSTGRES_PASSWORD=<用户密码>

# 数据库名称
POSTGRES_DB=n8n

# 非ROOT角色的用户名、密码
POSTGRES_NON_ROOT_USER=<用户名>
POSTGRES_NON_ROOT_PASSWORD=<用户密码>


# 设置时区
GENERIC_TIMEZONE=Asia/Shanghai
```

3. 执行安装指令

```
docker compose up -d
```
