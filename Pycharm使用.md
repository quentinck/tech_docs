# Pycharm使用

## Pycharm基本使用

### 常用快捷键

| 调试运行 | shift + F9       |
| -------- | ---------------- |
| 运行     | shift + F10      |
| 代码     | Ctrl + k         |
| 链接     | Ctrl + Shift + k |
| 单步运行 | F8               |



### Pycharm生成requirements.txt

在Terminal在命令行中输入

```shell
pip freeze>requirements.txt
```

### 创建文件

创建文件：app/main/__ init__.py

使用 PyCharm，这里有个快捷方式，右键点击 app 文件夹，在菜单中选择 new -> Python Package，在弹出的对话框中填写包名然后确认即可，填写内容：main/__ init__.py



### 函数跳转

Ctrl跳转进入函数

### 页面刷新

Ctrl+F5刷新页面，有时候修改html后无效，可以手动刷新一次

## Pycharm配置

### 查看函数说明

![image-20200411163609118](https://quentin-md.oss-cn-shanghai.aliyuncs.com/img/2020/04/11/20200411163610.png)

### Pycharm用鼠标滚轮控制字体大小

File —> setting —> Keymap —>在搜寻框中输入：increase —> Increase Font Size（双击） —> 在弹出的对话框中选择Add Mouse Shortcut 

File —> setting —> Keymap —>在搜寻框中输入：decrease —>Decrease Font Size（双击）—> 在弹出的对话框中选择Add Mouse Shortcut

### pycharm自动提示安装requirement.txt中的库

项目根目录中已经添加了requirements.txt文件，怎么提示自动安装？

 

解决：
Settings/Preferences -> Tools | Python Integrated Tools.

选项 Package requirements file field 中填入 requirements.txt。

![](https://quentin-md.oss-cn-shanghai.aliyuncs.com/img/2020/03/09/20200309223534.png)

也可以使用pip安装，在终端中输入：

```
pip install -r requirements.txt
```

生成

```
pip freeze > requirements.txt
```

### PyCharm无法Import当前文件夹下文件的问题解决

使用PyCharm，Import当前文件夹下文件的时候，会提示出错，找不到文件。
但是执行没有问题，说明文件，路径都没问题，只是PyCharm没有找到而已。

解决办法：
PyCharm上选中当前工程文件夹，右击->Mark  Directory as->Sources Root


### Pycharm中开启Flask的Debug

问题描述：Pycharm中无法通过代码开启Flask调试：

```python
app.run(debug=True)
```

解决办法：

通过pycharm的系统配置进行修改：

![](https://quentin-md.oss-cn-shanghai.aliyuncs.com/img/2020/03/07/20200307154618.png)

![](https://quentin-md.oss-cn-shanghai.aliyuncs.com/img/2020/03/07/20200307154655.png)

### Pycharm安装

1. 安装pycharm专业版，可自动生成flask的项目；

2. 使用“pycharm-professional-anaconda-2019.2.6.exe”版本，可安装conda进行虚拟环境管理；

3. pycharm conda executable:Tools->Install Miniconda3，路径为：D:\pycharm\miniconda3；

   ### Pycharm安装tensorflow 

   File>Settings：左侧Projection Interpreter安装

   问题：could not find a version that satisfies 

   解决办法：

   安装Python3.7的64位版本

### Pycharm显示rst文件

reStructuredText




## Pycharm常见问题

### PyCharm:Error running xxx: Cannot run program "D:\Python27\python.exe"

解决办法：设置界面File>Settings：左侧Projection Interpreter选项，显示的是当前使用的python版本，可以通过向下的箭头找到要切换成的版本。



### Error running 'test': Cannot run program "\usr\bin\python2.7" :CreateProcess error=2, 系统找不到指定文件

解决办法：关掉pycharm，再删掉.idea文件夹，再重新打开项目就好了



### [Python3 异常: name 'basestring' is not defined详解](http://www.itxm.cn/post/18707.html)

问题分析：

python3 里已经没有basestring 类型，用str代替了basestring ；

解决方案：

将关键字“basestring”替换为“str”；

### [PyCharm: Process finished with exit code 0](https://stackoverflow.com/questions/49460212/pycharm-process-finished-with-exit-code-0)

问题描述：flask程序运行后无法通过网页访问

解决办法：

```
app.run(host='127.0.0.1',port=5001)
```



