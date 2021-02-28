# templates
> base.html represents common html elements that you would likely repeat among pages
> Flask allows for HTML inheritance which is explained in this example.

## base.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Using double brackets {{ }} you can use python statements within HTML -->
    <!-- This is where we grab title which was passed in the render_template function -->
    <title>BOILERPLATE WEBSITE {{ title }}</title>
    <!-- This is where we use url_for flask function for applying the stylesheet -->
    <link rel="stylesheet" href="{{ url_for('static', filename='style.css') }}">
</head>

<body>
    <!-- Using braces and percents we can implement inheritance such that we begin -->
    <!--     with "block" then the name of the block and make sure we add an endblock -->
    <!--     to show where to stop -->
    {% block header %}{% endblock %}
    <div id="content">{% block content %}{% endblock %}</div>
</body>

</html>
```