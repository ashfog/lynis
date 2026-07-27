# Lynis - 安全审计与系统加固工具

## 🚀 快速开始 - 运行汉化版

```bash
# 方法一：使用环境变量临时运行中文版
LANG=cn_CN ./lynis audit system

# 方法二：创建配置文件永久使用中文
echo "language=cn" > /etc/lynis/default.prf
./lynis audit system
```

---

[![Linux Security Expert badge](https://badges.linuxsecurity.expert/tools/ranking/lynis.svg)](https://linuxsecurity.expert/tools/lynis/)
[![Build Status](https://travis-ci.org/CISOfy/lynis.svg?branch=master)](https://travis-ci.org/CISOfy/lynis)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/96/badge)](https://bestpractices.coreinfrastructure.org/projects/96)
[文档]

[文档]: https://cisofy.com/documentation/lynis/

喜欢这个软件吗？**给项目点个 Star** 成为 [stargazer](https://github.com/CISOfy/lynis/stargazers)。

----

# lynis

> Lynis - 安全审计和加固工具，适用于 UNIX 系统。

Lynis 是一款面向 Linux、macOS、BSD 等 UNIX 系统的安全审计工具。它会在系统本地执行**深度安全扫描**。其主要目标是测试安全防护能力并**提供系统加固建议**。它还会扫描常规系统信息、存在漏洞的软件包以及可能的配置问题。Lynis 通常被系统管理员和安全审计师用于评估系统的安全防御能力。除了"蓝队"人员，如今渗透测试人员也将 Lynis 纳入他们的工具包中。

我们相信软件应该**简单**、**定期更新**且**开源**。您应该能够信任、理解并有能力修改软件。许多人认同我们的理念，每天都有成千上万的用户使用它来保护他们的系统。

## 目标

Lynis 的主要目标包括：
- 自动化安全审计
- 合规性测试（如 ISO27001、PCI-DSS、HIPAA）
- 漏洞检测

本软件还可协助：
- 配置与资产管理
- 软件补丁管理
- 系统加固
- 渗透测试（权限提升）
- 入侵检测

### 适用人群

典型用户包括：
- 系统管理员
- 安全审计师
- 安全官
- 渗透测试人员
- 安全专业人员

## 安装

有多种方式可以安装 Lynis。

### 软件包

对于运行 Linux、BSD 和 macOS 的系统，通常有现成的软件包可用。这是获取 Lynis 的首选方法，因为安装快捷且易于更新。Lynis 项目本身也提供 [软件包](https://packages.cisofy.com/)，包括 RPM 或 DEB 格式，适用于以下系统：
`CentOS`、`Debian`、`Fedora`、`OEL`、`openSUSE`、`RHEL`、`Ubuntu` 等。

某些发行版也可能在其软件仓库中提供 Lynis：[![Repology](https://repology.org/badge/tiny-repos/lynis.svg)](https://repology.org/project/lynis/versions)

注意：某些发行版提供的版本可能不是最新的。这种情况下，最好使用 CISOfy 软件仓库、从官网下载 tarball 压缩包，或下载最新的 GitHub 发布版本。

### Git

您可以通过 git 获取最新的开发版本。

1. 克隆或下载项目文件（**无需编译或安装**）：

        git clone https://github.com/CISOfy/lynis

2. 执行：

        cd lynis && ./lynis audit system

如果您想以 `root` 身份（或使用 sudo）运行此软件，我们建议更改文件所有权。使用 `chown -R 0:0` 递归修改所有者和组为 ID `0`（即 `root`）。否则 Lynis 会警告您文件权限问题。毕竟，您正在执行由非特权用户拥有的文件。


## 文档

请查阅 [Lynis 文档](https://cisofy.com/documentation/lynis/) 了解更多关于 Lynis 的配置和使用方法。如果您对阅读更多 Linux 安全文章感兴趣，可以查看名为 Linux Audit 的 [Linux 安全博客](https://linux-audit.com/)。对于 Lynis 的一些发现和建议，该博客也是了解具体问题的资源来源。

## 自定义

如果您想创建自己的测试，请查看 [Lynis 软件开发工具包](https://github.com/CISOfy/lynis-sdk)。

## 安全

我们参与了 Linux 基金会的 [CII 最佳实践](https://www.bestpractices.dev/en/projects/96) 徽章计划。

## 媒体与奖项

Lynis 一路走来获得了不少奖项，我们为此感到自豪。

* 2016 年
  * [2016 年度最佳开源软件奖](http://www.infoworld.com/article/3121251/open-source-tools/bossie-awards-2016-the-best-open-source-networking-and-security-software.html#slide13)
  * TechRepublic 发表文章，将 Lynis 视为"必备"工具：[如何从命令行快速审计 Linux 系统](http://www.techrepublic.com/article/how-to-quickly-audit-a-linux-system-from-the-command-line/)
  * [![ToolsWatch 最佳工具（前十名）](https://www.toolswatch.org/badges/toptools/2016.svg)](https://www.toolswatch.org/2017/02/2016-top-security-tools-as-voted-by-toolswatch-org-readers/)

* 2015 年
  * [![ToolsWatch 最佳工具（第二名）](https://www.toolswatch.org/badges/toptools/2015.svg)](https://www.toolswatch.org/2016/02/2015-top-security-tools-as-voted-by-toolswatch-org-readers/)
  * [2015 年度最佳开源软件奖](http://www.idgenterprise.com/news/press-release/infoworld-announces-the-2015-best-of-open-source-software-awards/) ([存档](https://web.archive.org/web/20210313082124/https://www.idg.com/news/infoworld-announces-the-2015-best-of-open-source-software-awards/))

* 2014 年
  * [![ToolsWatch 最佳工具（第三名）](https://www.toolswatch.org/badges/toptools/2014.svg)](https://www.toolswatch.org/2015/01/2014-top-security-tools-as-voted-by-toolswatch-org-readers/)

* 2013 年
  * [![ToolsWatch 最佳工具（第六名）](https://www.toolswatch.org/badges/toptools/2013.svg)](https://www.toolswatch.org/2013/12/2013-top-security-tools-as-voted-by-toolswatch-org-readers/)

## 贡献

> 我们欢迎贡献者。

有什么想分享的吗？想帮助将 Lynis 翻译成您的母语？请在 GitHub 上创建 issue 或 pull request，或发送电子邮件至 lynis-dev@cisofy.com。

更多详情可查看 [贡献者指南](https://github.com/CISOfy/lynis/blob/master/CONTRIBUTING.md)。

您也可以通过给项目点 **Star** 来表示支持。

谢谢！

## 许可证

> GPLv3

## 企业版

此软件组件也是企业解决方案的一部分，专注于企业用户。提供相同质量，但包含更多功能。

重点领域包括合规性（`PCI DSS`、`HIPAA`、`ISO27001` 等）。企业版包含：
* Web 界面
* 仪表板和报告
* 加固代码片段
* 改进计划（基于风险）
* 商业支持
