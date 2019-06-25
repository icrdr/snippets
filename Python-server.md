### Setting mirror
Create User/pip/pip.int
```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple 
[install]
trusted-host=mirrors.aliyun.com
```

### Installing virtualenv
`pip install virtualenv`

`pip install virtualenvwrapper` / `pip install virtualenvwrapper-win`

### Create new env
`mkvirtualenv [name]`
#### (with other python version)
`mkvirtualenv [name] -p [python path]`

- check python version `python -V`
- check python path `which python` `which python3`

### Active env
`workon [name]`
### Quit env
`deactivate`

### Generate requirements.txt
`pip freeze > requirements.txt`
### Reinstall requirements
`pip install -r requirements.txt`



