# npm切换国内镜像方法

## 为什么要切换国内镜像
国外的镜像实在是太慢了，极其不稳定，下载模块特别慢，还容易中断

## 临时使用
	
	npm --registry https://registry.npm.taobao.org install <moduleName>

## 持久使用

	npm config set registry https://registry.npm.taobao.org

## 修改配置文件	
配置文件在~/.npmrc, 添加如下内容

	registry=https://registry.npm.taobao.org	
