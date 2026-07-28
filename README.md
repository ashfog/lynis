[![Linux Security Expert badge](https://badges.linuxsecurity.expert/tools/ranking/lynis.svg)](https://linuxsecurity.expert/tools/lynis/)
[![Build Status](https://travis-ci.org/CISOfy/lynis.svg?branch=master)](https://travis-ci.org/CISOfy/lynis)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/96/badge)](https://bestpractices.coreinfrastructure.org/projects/96)
[项目文档]

[项目文档]: https://cisofy.com/documentation/lynis/

喜欢这个项目的话，欢迎点一个 **Star**。

----

# Lynis 简体中文汉化版

> Lynis 是一款适用于 UNIX 类系统的安全审计与系统加固检查工具。

本仓库是 Lynis 的**简体中文汉化版**。汉化范围仅限用户可见的菜单、提示、状态、报告说明和文档，不增加功能，也不改变原有审计逻辑、命令参数、检查规则、报告字段或兼容行为。

Lynis 适用于 Linux、macOS、BSD 等 UNIX 类系统。它会直接在目标系统上执行深入的安全检查，主要用于评估系统当前的安全防护情况，并给出进一步加固的建议。Lynis 还会收集常规系统信息，检查存在风险的软件包以及可能有问题的配置。系统管理员、审计人员、安全人员和渗透测试人员都可以使用它来了解系统的安全状况。

上游项目：[CISOfy/lynis](https://github.com/CISOfy/lynis)

## 主要用途

Lynis 的主要用途包括：

- 自动执行系统安全审计
- 检查合规要求，例如 ISO 27001、PCI DSS、HIPAA
- 发现潜在漏洞和配置问题

它还可以辅助完成：

- 配置与资产管理
- 软件补丁管理
- 系统加固
- 渗透测试和提权检查
- 入侵检测

### 适用人群

- 系统管理员
- 安全审计人员
- 企业安全负责人
- 渗透测试人员
- 其他安全从业者

## 安装与使用

### 直接通过 Git 使用

本项目不需要编译，也不需要执行安装程序。

1. 克隆仓库：

        git clone https://github.com/ashfog/lynis.git

2. 进入目录并开始系统审计：

        cd lynis
        sudo ./lynis audit system

不使用 `sudo` 也可以运行，但部分需要管理员权限的检查会被跳过，因此结果可能不够完整。

如果使用 `root` 或 `sudo` 运行，而仓库文件属于普通用户，Lynis 可能会提示文件所有权不安全。确认文件来源可信后，可以把文件所有者改为 `root`：

        sudo chown -R 0:0 lynis

### 软件包安装

Linux、BSD 和 macOS 的部分发行版提供 Lynis 软件包。上游项目也提供适用于 RPM 和 DEB 系统的软件包，可用于 `CentOS`、`Debian`、`Fedora`、`OEL`、`openSUSE`、`RHEL`、`Ubuntu` 等系统。

需要注意：发行版软件源中的 Lynis 版本可能较旧。若需要使用本汉化版，请直接克隆本仓库，而不要安装发行版提供的原版软件包。

## 常用命令

执行完整系统审计：

        sudo ./lynis audit system

查看帮助：

        ./lynis --help

查看手册页：

        ./lynis --man

快速、非交互式扫描：

        sudo ./lynis audit system --quick

只显示警告：

        sudo ./lynis audit system --warnings-only

## 日志与报告

默认情况下，Lynis 会生成：

- 日志文件：`/var/log/lynis.log`
- 报告数据：`/var/log/lynis-report.dat`

报告中的字段名称会保持上游原样，以确保脚本、自动化工具和后续分析仍然兼容；终端中显示给用户阅读的章节、状态和说明会逐步汉化。

## 文档

详细配置和使用方法请参考 [Lynis 官方文档](https://cisofy.com/documentation/lynis/)。

Linux 安全相关资料也可以参考 [Linux Audit](https://linux-audit.com/)。Lynis 的部分检查建议会链接到该网站的说明文章。

## 自定义检查

需要编写自定义检查项目时，可以参考 [Lynis SDK](https://github.com/CISOfy/lynis-sdk)。

## 安全与上游维护

Lynis 参与 Linux Foundation 的 [CII Best Practices](https://www.bestpractices.dev/en/projects/96) 项目。

本汉化仓库以保持上游功能不变为原则。同步上游更新时，应只解决翻译冲突，不主动修改检查逻辑。

## 贡献

欢迎提交与中文翻译有关的问题或改进，包括：

- 发现仍然显示英文的用户界面文字
- 中文表达生硬、不准确或容易误解
- 同一术语在不同位置翻译不一致
- 上游新增了尚未翻译的菜单或提示

涉及 Lynis 功能、检查逻辑或安全规则的问题，请优先向[上游项目](https://github.com/CISOfy/lynis)反馈。

## 许可证

> GPLv3

本汉化版继续遵守 Lynis 原项目的 GPLv3 许可证。原项目版权和作者信息保持不变。

## 企业版

Lynis 也是 CISOfy 企业安全产品的一部分，企业版提供 Web 管理界面、仪表盘、集中报告、加固片段、风险改进计划和商业支持等功能。相关服务由上游 CISOfy 提供，与本汉化仓库无关。
