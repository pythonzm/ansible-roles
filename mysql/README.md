#### 用于部署单机版MySQL

安装方式是直接使用官方编译好的tar包，下载地址：[https://dev.mysql.com/downloads/mysql/](https://dev.mysql.com/downloads/mysql/) 

适用于 MySQL 5.7 + 以及 CentOS 7

因为tar包下载速度比较慢，就没有使用 `get_url` 模块，而是先下载文件，再将文件放到 `files` 目录下，然后在 `vars/main.yaml` 中配置变量 `mysql_tar_file_name` 值为文件的名称

#### 使用示例

```yaml
---
- hosts: cloud
  roles:
    - mysql
```
