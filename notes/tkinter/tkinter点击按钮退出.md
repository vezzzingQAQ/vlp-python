## tkinter点击按钮退出

https://zhuanlan.zhihu.com/p/475387345

```python
import tkinter as tk

class Test():
    def __init__(self):
        self.root=tk.Tk()
        self.root.geometry=('100x50')

        button=tk.Button(self.root,text='click to exit',command=self.quit)

        button.pack()
        
        self.root.mainloop()

    def quit(self):
        self.root.destroy()

app=Test()
```

destroy() 用来关闭窗口

### 非类方法

```python
import tkinter as tk

root=tk.Tk()
root.geometry('100x50')

def close_window():
    root.destroy()

button=tk.Button(text='click to exit',command=close_window)
button.pack()

root.mainloop()
```

2024.2.4