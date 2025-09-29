# n8n 和 postgres

大家好，我是向善，一名从程序员转型的 AI 实践者，专注于 AI 智能体和 AI 编程。

n8n 使用 postgreSQL 做数据库

文件说明：

- .env: 环境变量参数
- .docker-compose.yml: Docker 配置文件
- .init-data.sh: 数据库初试化脚本
- volumes: n8n 和 db 的卷映射。
- data: 映射 n8n 容器的 `/data/files` 文件夹。

`ngrok` 内网穿透版本请切换分支 `n8n-hosting-ngrok`。


# 使用教程

## 参数配置及教程

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
docker compose down
docker compose up -d
```
