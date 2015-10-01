# polito-just-in-time-behavior

Behavior to fire an event when the object first enters viewport.

Useful to delay processing or loading of resources until element comes visible.

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
        behaviors: [Polito.JustInTimeBehavior],
        prepareToRender: function(){
            console.log("Hello " + this.name + "!!");
        }
    });
</script>
```
