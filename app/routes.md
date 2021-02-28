# routes
> First off routes AND app instantiation can exist in the same file but I like to separate the 2.

```python
# importing "render_template" and "url_for" from flask 
## render_template will render the HTML from your templates folder
## url_for is used in the HTML file (see app/templates/base.html for more details)
from flask import render_template, url_for
# importing app from app folder (from app/__init__.py)
from app import app


# use app object as a decorator with a route method
## this "index" function is where we can add python computation if needed
## the '/' string parameter will be the endpoint direction for example
##     for @app.route('/index') when {host}/index is called this function
##     will run and the returned HTML will be presented.
@app.route('/')
@app.route('/index')
def index():
    # return rendered HTML to the client server, render_template can accept
    #    arguments to be used in the HTML such as "title"
    return render_template('index.html', title="Home")
```