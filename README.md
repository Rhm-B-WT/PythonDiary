# pythondiary

## 專案介紹

我的第一個網站!!!
[網站網址(host by Heroku)](https://pythondiary1218.herokuapp.com/)

## 成品展示

![](https://github.com/Rhm-B-WT/PythonDiary/blob/master/%E6%9C%AA%E5%91%BD%E5%90%8D.png)

## 使用技術

工具名稱 | 用途
---------|----------
Python 3 | 不需要解釋
Flask(python)    | 幫助我建立伺服器
HTML/CSS  | 網頁表示和排版
Heroku   | 託管網頁
Github   | 存放原始碼

## 程式碼片段

```python
@app.route("/")
def home():
    temp = glob.glob("articles/*")
    fill = []
    for t in temp:
        length = len(glob.glob(t + "/*.txt"))
        category = t.replace("articles/", "")
        f = (category, length)
        fill.append(f)
    return render_template("index.html", cat=fill)

```
