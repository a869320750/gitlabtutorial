# GitLab 简介
GitLab 是一个基于 Web 的 DevOps 平台，提供从代码管理、CI/CD（持续集成/持续交付）、项目管理到安全扫描等全流程工具。它最初是一个开源项目，后来发展成商业化产品，由 GitLab Inc. 公司开发和维护。

## 1. GitLab 的公司背景
公司名称：GitLab Inc.（成立于 2014 年）<br>
总部：美国旧金山（全球远程办公公司）<br>
创始人：Dmitriy Zaporozhets（乌克兰）和 Sid Sijbrandij（荷兰）<br>
商业模式：<br>
开源免费版（CE, Community Edition）<br>
商业付费版（EE, Enterprise Edition）（提供更多高级功能）<br>
上市情况：2021 年在纳斯达克上市（股票代码：GTLB）<br>

## 2. GitLab 的核心功能
GitLab 是一个 一体化 DevOps 平台，主要功能包括：<br>

### （1）代码仓库（Git Repository）<br>
类似 GitHub，提供 Git 代码托管<br>
支持分支管理、代码审查（MR）、保护分支、Web IDE 等<br>

#### 与 GitHub 的区别：

GitLab 自带完整的 CI/CD（GitHub 需依赖 Actions）<br>
GitLab 支持私有仓库免费（GitHub 免费版仅限公开仓库）<br>

### （2）持续集成/持续交付（CI/CD）
内置 CI/CD 流水线（.gitlab-ci.yml 配置）<br>
支持自动化构建、测试、部署<br>
可集成 Kubernetes、Docker、AWS、Azure 等云服务<br>
Auto DevOps：自动检测语言并生成 CI/CD 流程<br>

### （3）项目管理（Issue Tracking & Boards）
类似 Jira，支持敏捷开发看板（Kanban）<br>
问题（Issue）、里程碑（Milestone）、时间追踪<br>
Epics（企业版）：管理大型需求<br>

### （4）安全与合规（Security & Compliance）
静态应用安全测试（SAST）：检测代码漏洞<br>
动态应用安全测试（DAST）：扫描运行时的安全风险<br>
依赖扫描（Dependency Scanning）：检查第三方库漏洞<br>
许可证合规（License Compliance）：确保开源许可证合规<br>

### （5）代码质量（Code Quality）
内置代码质量分析（如 RuboCop、ESLint）<br>
支持 SonarQube 集成<br>
提供代码覆盖率报告<br>

### （6）包管理（Package Registry）
支持 Docker、NPM、Maven、PyPI、NuGet 等包管理<br>
可搭建私有仓库（类似 Nexus）<br>

### （7）Wiki 与文档管理
内置 Markdown 支持的 Wiki<br>
可托管项目文档、API 文档等<br>

### （8）监控与运维（Monitoring）
集成 Prometheus、Grafana 监控<br>
日志管理（Logging）<br>
错误跟踪（Error Tracking）<br>

### （9）Kubernetes 集成
支持直接部署到 K8s<br>
提供集群管理、Helm Chart 支持<br>

### （10）AI 辅助（GitLab Duo）
AI 代码建议（类似 GitHub Copilot）<br>
AI 测试生成<br>
AI 安全扫描<br>

## 3. GitLab 的版本区别

| 功能 | 社区版（CE）| 企业版（EE）|
|---|---|---|
|代码仓库|	✅	|✅|
|CI/CD	|✅	|✅（更高级功能）|
|项目管理|	✅|	✅（Epics、看板）|
|安全扫描|	❌（有限）|	✅（SAST/DAST）|
|合规管理|	❌	|✅|
|K8s 集成|	✅（基础）|	✅（高级）|
|AI 功能|	❌	|✅（GitLab Duo）|
|价格	|免费	|按用户收费|

## 4. GitLab vs GitHub vs Bitbucket

| 对比项 | GitLab	| GitHub |	Bitbucket |
|---|---|---|---|
| 公司 | GitLab Inc.	| Microsoft|	Atlassian|
|CI/CD	| ✅ 内置	| ✅（Actions）|	✅（Pipelines）|
|私有仓库免费| ✅| 	❌（付费）|	✅|
|K8s 集成	| ✅| 	❌|	❌|
|安全扫描	| ✅| （企业版）|	✅（高级版）	❌|
|AI 功能	| ✅| （GitLab Duo）|	✅（Copilot）	❌|

## 5. 谁在使用 GitLab？
企业：IBM、Siemens、NASA、阿里巴巴、腾讯<br>
政府：欧盟委员会、美国国防部<br>
开源项目：Linux 基金会部分项目<br>

## 6. 总结
GitLab 是一个完整的 DevOps 平台，而 GitHub 更偏向代码托管。<br>
适合团队协作，尤其需要 CI/CD、安全扫描、K8s 集成 的企业。<br>
免费版（CE） 适合个人和小团队，企业版（EE） 提供更多高级功能。<br>
如果你需要一个 从代码到部署的一体化工具，GitLab 是一个非常好的选择！<br>