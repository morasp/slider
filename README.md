# Slider

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/e27cc967ff8147b9b0a4e2b134a81d08)](https://app.codacy.com/manual/morasp/slider?utm_source=github.com&utm_medium=referral&utm_content=morasp/slider&utm_campaign=Badge_Grade_Dashboard)

A simple canvas based slider

## About
**Autor: [Moritz Speidel](https://moritz-speidel.de)**

This is a simple canvas based slider. For a quick start, no configuration is needed. The silder supports vertical and horizontal mode. Mouse and touch is supported.
Also the slider offers a Change-Event for easy usage.

> No JQuery required

## How to use it

First you need to add the library to your page:
```html
<script type="text/javascript" src="slider.js"></script>
```
Then create a container for the slider and specify the width and height:
```html
<div id="slider" style="width: 40px; height: 150px;"></div>
```

At the end of the page (or in an onload-handler) add the code to initialize the slider:
```javascript
var slide = new Slider("slider", {
			orientation: "vertical",
			autoReturnToCenter: true,
			minimum: -100,
			maximum: 100,
			initial: 0
		});
```
The options are not neccesary, if you only want a simple vertical slider from 0 to 100.

You can either get the current value of the slider with the getValue() function or with the change event:
```javascript
var value = slider.getValue();

slider.on("change", (e)=>{
    console.log(e.value)
});
```

