---
title: Bootstrap Date/Time Picker
layout: layout
author: Thiago de Arruda
authorUrl: https://github.com/tarruda
projectName: bootstrap-datetimepicker
projectDescription: Date/Time Picker for Twitter Boostrap 
zipDownloadUrl: assets/dist/bootstrap-datetimepicker-0.0.5.zip
githubUrl: https://github.com/tarruda/bootstrap-datetimepicker
css:
  - assets/css/bootstrap-datetimepicker.min.css
js:
  - assets/js/bootstrap-datetimepicker.min.js
  - assets/js/bootstrap-datetimepicker.pt-BR.js
  - assets/js/index.js
---
### Introduction
Simple date/time picker component based on the work of [Stefan Petre](http://www.eyecon.ro/bootstrap-datepicker/),
with contributions taken from [Andrew Rowls](https://github.com/eternicode) and
[jdewit](https://github.com/jdewit).

### Demo

Default behavior in pt-BR, picks date/time with fast masked input typing
(need only to type the numbers, the static part of the mask is inserted
automatically if missing) or via the
popup widget, which supports year, month, day, hour and minute views:

{% highlight html %}
{% include demo1.html %}
{% endhighlight %}
{% include demo1.html %}

Similar to above example, but in US date/hour format:

{% highlight html %}
{% include demo2.html %}
{% endhighlight %}
{% include demo2.html %}

Disables date picker:

{% highlight html %}
{% include demo3.html %}
{% endhighlight %}
{% include demo3.html %}

Disables time picker:

{% highlight html %}
{% include demo4.html %}
{% endhighlight %}
{% include demo4.html %}

### Complete example

Copy and paste the following code in a file(eg: test.html) and it should
produce a widget similar to the first demo:

{% highlight html %}
<!DOCTYPE HTML>
<html>
  <head>
    <link href="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.2.2/css/bootstrap-combined.min.css" rel="stylesheet">
    <link rel="stylesheet" type="text/css" media="screen"
     href="http://tarruda.github.com/bootstrap-datetimepicker/assets/css/bootstrap-datetimepicker.min.css">
  </head>
  <body>
    <div id="datetimepicker" class="input-append date">
      <input type="text"></input>
      <span class="add-on">
        <i data-time-icon="icon-time" data-date-icon="icon-calendar"></i>
      </span>
    </div>
    <script type="text/javascript"
     src="http://cdnjs.cloudflare.com/ajax/libs/jquery/1.8.3/jquery.min.js">
    </script> 
    <script type="text/javascript"
     src="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.2.2/js/bootstrap.min.js">
    </script>
    <script type="text/javascript"
     src="http://tarruda.github.com/bootstrap-datetimepicker/assets/js/bootstrap-datetimepicker.min.js">
    </script>
    <script type="text/javascript"
     src="http://tarruda.github.com/bootstrap-datetimepicker/assets/js/bootstrap-datetimepicker.pt-BR.js">
    </script>
    <script type="text/javascript">
      $('#datetimepicker').datetimepicker({
        format: 'dd/MM/yyyy hh:mm:ss',
        language: 'pt-BR'
      });
    </script>
  </body>
<html>
{% endhighlight %}

The element also has the bootstrap-datepicker 'changeDate' event and 'setValue' method.

### Compilation
To compile/minify you need to have make, node.js and npm on your $PATH

{% highlight sh %}
$ git clone git://github.com/tarruda/bootstrap-datetimepicker.git
$ cd bootstrap-datetimepicker
$ make deps
$ make build
{% endhighlight %}
