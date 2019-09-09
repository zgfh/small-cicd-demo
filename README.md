# small-cicd-demo
该项目是一个demo，解释如何使用small-cicd
### 安装
```
git clone https://github.com/zgfh/small-cicd-demo.git small-cicd-demo
cd small-cicd-demo
curl http://github.com/small-cicd/get-small-cicd.sh |sh
```
### 效果
1. 本配置仓库更新后，自动更新配置
1. 自动拉取app设定的代码到当前目录(small-cicd-demo)的app目录
2. 当检测到 master 分支变化后运行(如果同目录有Dockerfile.app会复制到app目录下) `docker build -t app .`
3. 如果 docker-compose.yaml 存在，执行 `docker-compose up -d app`
