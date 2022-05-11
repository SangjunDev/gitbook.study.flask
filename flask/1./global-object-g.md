# Global Object:g

**Application Context**

* Application 영역에서 붙어있는 모든 사람을 컨트롤 하고 싶을때 사용
* _\_\_init_\_\_.py

```
from flask import Flask,g

app = Flask(__name__)
app.debug = True


@app.before_request
def before_request():
    print("before_req")
    g.str = "한글"
    
@app.route("/gg")
def helloworld2():
    return "Hello Flask World!" + getattr(g , 'str','111')

@app.route("/")
def helloworld():
    return "Hello Flask World!" 
```
