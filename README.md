# Mathematical Calculations using JavaScript
## AIM:
To design a website to calculate the area of a circle and volume of a cylinder using JavaScript.

## DESIGN STEPS:
### Step 1: 
Requirement collection.
### Step 2:
Creating the layout using HTML and CSS.
### Step 3:
Write JavaScript to perform calculations.
### Step 4:
Choose the appropriate style and color scheme.
### Step 5:
Validate the layout in various browsers.
### Step 6:
Validate the HTML code.
### Step 6:
Publish the website in the given URL.


## PROGRAM:
### arearectangle.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Area Of A Rectangle</title>
    <link rel="stylesheet" href="{% static 'css/own.css' %}">
</head>

<body>
    <div class="container">
        <div class="formview">
            <div class="banner">
                CALCULATE AREA OF A RECTANGLE
            </div>
            <div class="content">
                <form action="/addnumber.html/" method="GET">
                    {% csrf_token %}
                    <div class="forminput">
                        <label for="value_a">LENGTH=</label>
                        <input type="text" name="value_a" id="value_a">
                    </div>
                    <div class="forminput">
                        <label for="value_b">BREADTH=</label>
                        <input type="text" name="value_b" id="value_b">
                    </div>
                    <div class="forminput">
                        <button type="button" name="button_calculate" id="button_calculate">CALCULATE</button>
                    </div>
                    <div class="forminput">
                        <label for="value_c">AREA=</label>
                        <input type="text" name="value_c" id="value_c">
                    </div>
            </div>
            </form>
        </div>
    </div>
    </div>
    <script src="/static/js/arearectangle.js"></script>
</body>

</html>
```
### arearectangle.js
```
addBtn = document.querySelector('#button_calculate');

addBtn.addEventListener('click',function(e){

    txtA = document.querySelector('#value_a');
    txtB = document.querySelector('#value_b');
    txtC = document.querySelector('#value_c');

    let c;

    c = parseFloat(txtA.value) * parseFloat(txtB.value);

    txtC.value = c;
});

```

### mathadd.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Adding Two Numbers</title>
    <link rel="stylesheet" href="{% static 'css/own.css' %}">
</head>
<body>
    <div class="container">
        <div class="formview">
            <div class="banner">
                ADD TWO NUMBERS
            </div>
            <div class="content">
                <form action="/addnumber.html/" method="GET">
                    {% csrf_token %}
                    <div class="forminput">
                        <label for="value_a">A=</label>
                        <input type="text" name="value_a" id="value_a">
                    </div>
                    <div class="forminput">
                        <label for="value_b">B=</label>
                        <input type="text" name="value_b" id="value_b">
                    </div>
            <div class="forminput">
                <button type="button" name="button_add" id="button_add">Add</button>
            </div>
            <div class="forminput">
                <label for="value_c">C=</label>
                <input type="text" name="value_c" id="value_c" readonly>
            </div>
            </form>
        </div>
    </div>
    </div>
    <script src="/static/js/mathadd.js"></script>
</body>

</html>
```

### mathadd.js
```

addBtn = document.querySelector('#button_add');

addBtn.addEventListener('click',function(e){

    txtA = document.querySelector('#value_a');
    txtB = document.querySelector('#value_b');
    txtC = document.querySelector('#value_c');

    let c;

    c = parseFloat(txtA.value) + parseFloat(txtB.value);

    txtC.value = c;
});
```


## OUTPUT:
![output](./static/img/e2.png)

![output](./static/img/e3.png)

![output](./static/img/e4.png)

## RESULT:
Thus a website is designed for the chip manufacturing company and is hosted in the url http://balaji.student.saveetha.in:8000/mathadd.
Thus a website is designed for the chip manufacturing company and is hosted in the url http://balaji.student.saveetha.in:8000/arearectangle.