#### 用于部署单机版Mongodb

安装方式是直接使用官方编译好的tar包，下载地址：[https://www.mongodb.com/try/download/community?tck=docs_server](https://www.mongodb.com/try/download/community?tck=docs_server) 

适用于CentOS 7 + 

因为tar包下载速度比较慢，就没有使用 `get_url` 模块，而是先下载文件，再将文件放到 `files` 目录下，然后在 `vars/main.yaml` 中配置变量 `mongod_tar_file_name` 值为文件的名称

#### 使用示例

```yaml
---
- hosts: cloud
  roles:
    - mongod
```
