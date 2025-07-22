# GitLab Runner 注册步骤

## 1. 获取 Registration Token

1. 登录你的 GitLab 网页端。
2. 进入对应项目或组，点击左侧菜单【Settings】→【CI / CD】→ 展开【Runners】。
3. 找到 **Registration token**，复制它。

## 2. 安装 GitLab Runner

以 Ubuntu 为例：

```sh
sudo apt-get update
sudo apt-get install -y gitlab-runner
```

## 3. 注册 Runner

在终端执行：

```sh
sudo gitlab-runner register
```

根据提示依次输入：

- **GitLab 实例 URL**（如：https://gitlab.com 或你的私有服务器地址）
- **Registration token**（上一步复制的 token）
- **Runner 描述**（随便写，比如 uavcli_ird_runner）
- **Runner 标签**（如 python, docker，多个用逗号分隔）
- **Executor**（常用 docker 或 shell，推荐 docker）
- **默认 Docker 镜像**（如 python:3.10-slim 或你自定义的镜像）

## 4. 启动 Runner

```sh
sudo gitlab-runner start
```

## 5. 检查 Runner 状态

在 GitLab 网页端【Settings】→【CI / CD】→【Runners】可以看到新注册的 Runner。

---

**常见问题：**
- 如果用 docker executor，服务器需已安装 Docker。
- 标签要和 `.gitlab-ci.yml` 里的 `tags` 保持一致。

---

下次只需照此文档操