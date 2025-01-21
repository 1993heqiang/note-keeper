## 命令

### config

- 查看配置项及来源
  
  ```shell
  # 查看所有配置及来源
  git config --show-origin --list
  
  # 查看特定配置项的来源
  git config --show-origin user.name
  
  # 查看匹配特定模式的配置项来源
  git config --show-origin --get-regexp user
  ```
  
  

- 



## 配置参数

### core.autocrlf

```shell
# 提交时会自动将CRLF转换为LF,检出时会将LF转换为CRLF,适用于Windows系统.
git config --global core.autocrlf true

# 提交时会自动将CRLF转换为LF,检出时不转换,适用于macOS和Linux.
git config --global core.autocrlf input

# 仅在Windows上开发时,关闭该特性可以将CRLF都保留在版本库中.
git config --global core.autocrlf false
```


