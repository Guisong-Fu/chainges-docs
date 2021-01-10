---
description: '详见：https://docs.daml.com/getting-started/installation.html'
---

# DAML 安装 & IDE

## 安装流程：

请参照官方教程： 

{% embed url="https://docs.daml.com/getting-started/installation.html" %}

## IDE：

理论上可以用任何编辑器编写daml程序。但到目前为止，VS Code Studio仍是唯一一个整合相对较好的IDE，有比如支持关键词高亮，测试\(scenario\)结果直接显示等功能。  
但请注意，VS Code Studio对daml的支持仍远逊于比如PyCharm对Python的支持。比如我个人非常依赖的auto-intent\(自动缩进\)功能，VS Code Studio仍不能很好的支持DAML。

## DAML Assistant\(DAML Cli - daml\)

参见： 

{% embed url="https://docs.daml.com/tools/assistant.html" %}

范例：

```text
# List all templates -- 显示所有模板
daml new --list

# 用模板创建新的项目（project）
daml new create-daml-app --template create-daml-app

# 用VS Code 打开当前文件夹
daml studio
```



