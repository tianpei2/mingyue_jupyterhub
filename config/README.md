# config

## 1. To generate a default config file, `jupyterhub_config.py`:

```
jupyterhub --generate-config
```

## 2. my configuration

```
c.Authenticator.admin_users = {'root'}  # 管理员用户
# 管理员是否有权在各自计算机上以其他用户身份登录，以进行调试，此选项通常用于 JupyterHub 的托管部署，以避免在启动服务之前手动创建所有用户
c.JupyterHub.admin_access = True
c.PAMAuthenticator.open_sessions = False # 解决多用户同时登录问题。
c.Spawner.args = ['--allow-root']  # 允许root用户使用
c.LocalAuthenticator.create_system_users = True  # 允许创建其他用户

c.JupyterHub.ip = '192.168.1.16'
c.JupyterHub.port = 50
c.PAMAuthenticator.encoding = 'utf8'

c.Authenticator.allowed_users = {'test', 'test1'}
c.Authenticator.admin_users = {'root'}  # 管理员用户
c.DummyAuthenticator.password = "test123"  # 初始密码设置
```
