# 简介

大家好，我是向善，一名从程序员转型的 AI 实践者，专注于 AI 智能体和 AI 编程。

应用栈包含：
- `n8n` 必选
- `postgres` 必选
- `ngrok`：可选
- `rsshub`：可选
- `redis`：可选
  
不需要的服务，请在 `docker-compose.yml` 文件中注释掉。


项目文件说明：

- `.env`: 环境变量参数
- `.docker-compose.yml`: Docker 配置文件
- `.init-data.sh`: 数据库初试化脚本
- `volumes`: n8n 和 db 的卷映射。
- `data`: 映射 n8n 容器的 `/data/files` 文件夹。


# 使用教程

1. 下载当前仓库，放在合适的文件夹中（路径不要有中文）
2. 修改 `.env` 中的变量值。如果需要 ngrok 使用前请申请token和地址[Ngrok](https://dashboard.ngrok.com/get-started/your-authtoken)。
3. 执行安装指令
```
docker compose down
docker compose up -d
```


# 关于作者

公众号：向善AIGC
