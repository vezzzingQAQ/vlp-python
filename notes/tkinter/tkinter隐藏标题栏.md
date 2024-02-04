## tkinter隐藏标题栏

https://blog.csdn.net/qq_41415692/article/details/132618235

```python
import tkinter as tk

win=tk.Tk()
win.overrideredirect(True) # 去掉标题栏
win.geometry('300x100+600+400') # 窗口放置位置
win.configure(bg='Violet')

win.mainloop()
```

2024.2.4