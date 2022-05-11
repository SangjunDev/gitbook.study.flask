# Hello Flask World

\_\__**init\_\_**_**.py**

```
from flask import Flask

app = Flask(__name__)

@app.route("/")
def helloworld():
    return "Hello Flask World!"
```

**start\_helloflask.py**

```
from helloflask import app

app.run(port=8080, host='0.0.0.0')
```
