# AngularJS Pageslide Directive

An AngularJS directive which slides another panel over your browser to reveal an additional interaction pane.

It does all the css manipulation needed to position your content off canvas.


Use within your Angular app


`var app = angular.module("app", ["pageslide-directive"]);`

Just use the ```<pageslide>``` element or attribute inside a controller scope like this:

please note that you need an outer controller to define the scope of your **checked** model

also you need an inner ```<div>``` to wrap your content in

```
<div ... ng-controller="yourCtrl">
    ...
    <pageslide ps-open="checked">
        <div>
            <p>some random content...</p>
        </div>
    </pageslide>
    ...
</div>

```

### Options:

```
pageslide (required)

// Configuration
ps-side (optional) = Where the panel should appear (right,left,top,bottom), if empty defaults to "right"
ps-container (optional) = custom CSS ID selector to which the slider div appends (e.g: <div id='myDiv'/> -> ps-container="myDiv")
ps-body-class (optional) = if true adds a class on the container body reflecting the state of the pageslide

// Interaction
ps-open (optional) = Boolean true/false used to open and close the panel (optional)
ps-auto-close (optional) = true if you want the panel to close on location change
ps-key-listener (optional) = close the sidebar with the ESC key (defaults to false)
ps-click-outside (optional) = close the sidebar by clicking outside (defaults to true)
ps-push (optional) = push the main body to show the panel (defaults to false)

// Style
ps-class (optional) = The class for the pageslide (default: "ng-pageslide")
ps-speed (optional) = The speed of the transition (optional)
ps-size (optional) = desired height/width of panel (defaults to 300px)
ps-zindex (optional) = desired z-index (defaults to 1000)

```

