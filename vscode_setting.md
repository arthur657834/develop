```
vscode-icons

python配置:
vscode安装python插件

pip install flake8
安装flake8成功后，打开VScode，文件->首选项->用户设置，在settings.json文件中输入"python.linting.flake8Enabled": true

pip install autopep8
格式工具
或者更改
pip install yapf 
安装yapf成功后，打开VSCode，文件->首选项->用户设置，在settings.json文件中输入"python.formatting.provider": "yapf"

pip install pylint



GO配置:
cd F:\go_workspace\src\golang.org\x
git clone https://github.com/golang/tools.git

代码着彩色
代码自动完成（使用gocode）
代码片段
快速提示信息（使用godef）
跳转到定义（使用godef）
搜索参考引用（使用go-find-references）
文件大纲（使用go-outline）
重命名（使用gorename）
保存构建（使用go build和go test）
代码格式化（使用goreturns或goimports或gofmt）
调试代码（使用delve）

方法2:
墙的原因安装不成功
go get -v -u github.com/peterh/liner github.com/derekparker/delve/cmd/dlv
go get -u -v github.com/nsf/gocode  
go get -u -v github.com/rogpeppe/godef  
go get -u -v github.com/golang/lint/golint  
go get -u -v github.com/lukehoban/go-outline  
go get -u -v sourcegraph.com/sqs/goreturns  
go get -u -v golang.org/x/tools/cmd/gorename  
go get -u -v github.com/tpng/gopkgs  
go get -u -v github.com/newhook/go-symbols  
go get -u -v golang.org/x/tools/cmd/guru 

```
