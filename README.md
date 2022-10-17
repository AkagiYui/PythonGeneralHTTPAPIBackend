# 通用 HTTP API 后端模板
| 简体中文 | English(WIP) |

![Python版本](https://img.shields.io/badge/python-3.10.7-blue)
![开源协议](https://img.shields.io/github/license/AkagiYui/PythonGeneralHTTPAPIBackend)
![提交活动](https://img.shields.io/github/commit-activity/m/AkagiYui/PythonGeneralHTTPAPIBackend)
![代码行数](https://img.shields.io/tokei/lines/github/AkagiYui/PythonGeneralHTTPAPIBackend)

这是一款通用的 HTTP API 后端模板，可以用于帮你快速创建一个 HTTP API 项目。
该项目已实现基本的**用户管理**、**文件管理**、**权限管理**、**日志管理**、**配置管理**等功能，
你只需要在此基础上编写业务相关内容即可。

## 支持的功能

- [ ] 自动部署
- [ ] 代码检查
- [ ] 跨域支持

- [ ] 用户注册
- [ ] 用户登录
- [ ] 用户名是否可用
- [ ] 用户信息

## 快速开始

### 使用 Docker 部署

```shell
git clone https://github.com/AkagiYui/PythonGeneralHTTPAPIBackend
cd ./PythonGeneralHTTPAPIBackend
docker compose up -d --build
```

### 手动部署

请确保你的机器有 **Python 3.10.7** 的环境，其他版本未经测试。

#### 安装依赖

##### Windows 10 PowerShell

```ps
git clone https://github.com/AkagiYui/PythonGeneralHTTPAPIBackend
cd ./PythonGeneralHTTPAPIBackend
python -m venv venv
./venv/Scripts/activate
python -m pip install -r ./requirements.txt
cd ./src
```

##### Linux Debian 11

```shell
git clone https://github.com/AkagiYui/PythonGeneralHTTPAPIBackend
cd ./PythonGeneralHTTPAPIBackend
python3 -m venv venv
source ./venv/bin/activate
python -m pip install -r ./requirements.txt
cd ./src
```

#### 修改配置文件

```ps
cp config.yaml.bak config.yaml
```

你也可以使用环境变量

[//]: # (TODO: 待补充环境变量)

#### 启动服务

```ps
python ./main.py --debug
```

## 开发相关

- 操作系统：[Windows 10 19044.1586](https://www.microsoft.com/zh-cn/windows)
- 系统架构：amd64

### 使用技术栈

- Python: [3.10.7](https://www.python.org/) [Download 下载地址](https://www.python.org/downloads/release/python-3107/)
- 依赖表生成工具: [pip-tools 6.8.0](https://github.com/jazzband/pip-tools/)
- 导入排序工具: [isort 5.10.1](https://pycqa.github.io/isort/)
- 代码格式化工具: [flake8 5.0.4](https://flake8.readthedocs.io/en/latest/) [mypy 0.982](https://mypy.readthedocs.io/en/latest/)
- 数据库: [MySQL](https://www.mysql.com/)

### 运行时Python包  

- [rich 12.5.1](https://github.com/Textualize/rich/blob/master/README.cn.md) 控制台美化
- [distro 1.7.0](https://github.com/python-distro/distro) 系统平台信息获取
- [psutil 5.9.1](https://github.com/giampaolo/psutil) 系统信息获取
- [ruamel.yaml 0.17.21](https://yaml.readthedocs.io/en/latest/) Yaml解析
- [peewee 3.15.1](https://github.com/coleifer/peewee/) ORM工具
- [fastapi 0.85.0](https://fastapi.tiangolo.com/zh/) HTTP/Websocket服务器
- [uvicorn 0.18.2](https://www.uvicorn.org/) ASGI web 服务器
- [PyMySQL 1.0.2](https://pymysql.readthedocs.io/) MySQL客户端
- [python-jose 3.3.0](https://python-jose.readthedocs.io/en/latest/) JWT工具
- [cryptography 38.0.1](https://cryptography.io/en/latest/) 加密工具
- [Pillow 9.2.0](https://python-pillow.org/) 图像处理
- [qrcode 7.3.1](https://github.com/lincolnloop/python-qrcode) 二维码生成

### 代码检查

```shell
python -m pip install -r ./requirements-dev.txt
python ./code_lint.py
```
