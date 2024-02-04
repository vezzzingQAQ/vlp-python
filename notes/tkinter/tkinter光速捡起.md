## tkinter快速捡起

https://blog.csdn.net/weixin_42953201/article/details/103026235

https://www.runoob.com/python/python-gui-tkinter.html

Python 的标准 GUI 库

只要安装好 Python 之后就能 import Tkinter 库、而且 IDLE 也是用 Tkinter 编写而成、对于简单的图形界面 Tkinter 还是能应付自如

### 搭建

```python
#!/usr/bin/python3
 
import tkinter
top = tkinter.Tk()
# 进入消息循环
top.mainloop()
```

### Tkinter组件

![](./assets/1.png)

### 标准属性

所有控件的共同属性，如大小，字体和颜色等等

![](./assets/2.png)

### Canvas

#### 创建

```python
w = Canvas ( master, option=value, ... )
```

* master: 按钮的父容器

* options: 可选项，即该按钮的可设置的属性，这些选项可以用键 = 值的形式设置，并以逗号分隔

#### 划线

```python
from tkinter import*

root=Tk()

w=Canvas(root,width=200,height=100,background='white')
w.pack()

line1=w.create_line(0,50,200,50,fill='yellow')
rect1=w.create_rectangle(0,0,18,75,fill='pink')

mainloop()
```

#### 绘制椭圆

```python
from tkinter import*

root=Tk()

w=Canvas(root,width=200,height=100,background='white')
w.pack()

w.create_rectangle(40,20,100,50,dash=(4,4))
w.create_oval(40,20,100,50,fill='pink')

mainloop()
```

![](./assets/3.png)

#### 插入文字

```python
from tkinter import*

root=Tk()

w=Canvas(root,width=200,height=100,background='white')
w.pack()

line1=w.create_line(0,0,200,100,fill='yellow',width=3)
line2=w.create_line(200,0,0,100,fill='green',width=3)
rect1=w.create_rectangle(40,20,160,80,fill='pink')
rect2=w.create_rectangle(65,35,135,65,fill='white')

w.create_text(100,50,text='你好!')

mainloop()
```

![](./assets/4.png)

2024.2.4