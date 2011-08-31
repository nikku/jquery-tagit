jQuery Tagit
============

[jQuery](http://jquery.com/) plugin for tag input fields, e.g. the 
ones used by [Stackoverflow](http://stackoverflow.com/).

![screenshot](https://github.com/Nikku/jquery-tagit/raw/master/docs/sample.jpg)

CSS markup is based on [bootstrap](http://twitter.github.com/bootstrap/) and built with [Less](http://lesscss.org/) support.

Inspired by [Tag-it!](http://aehlke.github.com/tag-it/).

Features
--------

* Autocompletion
* Mouse and keyboard handling
* Visual integration into bootstrapped form environments

Requirements
------------

* [jQuery](http://jquery.com/) (tested with jQuery 1.6.2 but might work with earlier versions)
* [bootstrap](http://twitter.github.com/bootstrap/) for styling.

Usage
-----

Include requirements and plugin in the header of your website

```html
<html>
    <head>
        <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.6.2/jquery.min.js"></script>
        <script type="text/javascript" src="jquery.tagit.js"></script>
        <style type="text/css">
            @import url('http://twitter.github.com/bootstrap/assets/css/bootstrap-1.1.1.min.css');
            @import url('tagit.css');
        </style>
    </head>
    <!-- ... -->
```

Create a `ul` element in a bootstrap like form environment:

```html
<form action="#">
    <fieldset>
        <div class="clearfix">
            <label>Experience in</label>
            <div class="input">
                <ul id="languages-select" class="fake-input" tabindex="1">
                    <li>Java</li>
                </ul>
            </div>
        </div>
    </fieldset>
</form>
```

Control the `ul` element using jQuery:

```html
<script type="text/javascript">
    $(function() {
        var tags = ["Java", "Javascript", "Python", "C", 
                    "C++", "Ruby", "CSS", "HTML", "C#", 
                    "Visual Basic", "Prolog", "Smalltalk", 
                    "Scala", "Haskel", "Bash"];
    
        $("#languages-select").tagit({
            tags: tags,
            field: "language"
        });
    });
</script>
```

See the [full example](https://github.com/Nikku/jquery-tagit/raw/master/example/example1.html).
