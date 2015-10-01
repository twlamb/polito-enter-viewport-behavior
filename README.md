# polito-just-in-time-behavior

Behavior to fire an event when the object enters or exits viewport.

Useful to delay processing or loading of resources until element comes visible.

```
bower install polito-enter-viewport-behavior
```
```html
<dom-module id="polito-hello">
    <style>
       :host {
           height:300px;
           display: block;
       }
    </style>
    <template>

        <h1>{{name}}</h1>

    </template>

</dom-module>

<script>
    Polymer({
        is: "polito-hello",
        behaviors: [Polito.EnterViewportBehavior],
        prepareToRender: function(){
            console.log("Hello once " + this.name + "!!");
        },
        enterViewport: function () {
            console.log("Hello " + this.name + "!!");
        },
        exitViewport: function () {
            console.log("Bye " + this.name + "!!");
        }
    });
</script>
```
