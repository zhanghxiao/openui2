# 使用官方Python基础镜像
FROM python:3.10-slim

# 设置工作目录
WORKDIR /app

# 安装git
RUN apt-get update && apt-get install -y git

# 克隆代码仓库
RUN git clone https://github.com/zhanghxiao/openui

# 进入backend目录
WORKDIR /app/openui/backend

# 安装Python依赖
RUN pip install .


# 创建根目录数据库目录并赋予权限
RUN mkdir -p /.openui && chmod -R 777 /.openui

# 暴露应用程序端口
EXPOSE 7878

# 运行应用
CMD ["python", "-m", "openui"]
