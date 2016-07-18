# JavaScript Live Templates for IntelliJ IDEs
The set of javascript live templates for IntelliJ IDEs (Idea, PHPStorm & others).

### Usage
To use the live templates:  

1. Copy **templates.xml** content to system clipboard.
2. In the Live Templates page of the Settings/Preferences dialog, select the group where you want to insert the copied live templates.
3. Right-click the selection, and choose Paste on the context menu.

### Live Templates
+ [amdini](#amdini)
+ [amdini_bbm](#amdini_bbm)
+ [amdini_bbv](#amdini_bbv)
+ [amdini_bbl](#amdini_bbl)
+ [dp_singleton](#dp_singleton)

##### amdini
Init amd module:
```
/**
 * $DESCRIPTION$
 *
 * @module $MODULE$
 * @returns {constructor}
 */
define([], function() {
    'use strict';

    var $MODULE$ = $END$;

    return $MODULE$;
});
```
* `DESCRIPTION` - Module description
* `MODULE` - Module/class name

##### amdini_bbm
Init amd backbone model:
```
/**
 * $DESCRIPTION$
 *
 * @module $MODULE$
 * @returns {Backbone.Model}
 */
define([
    'lodash',
    'backbone'

], function(
    _,
    Backbone

) {
    'use strict';

    var $MODULE$ = Backbone.Model.extend({
        $END$
    });

    return $MODULE$;
});
```
* `DESCRIPTION` - Module description
* `MODULE` - Module/class name

##### amdini_bbv
Init amd backbone view
```
/**
 * $DESCRIPTION$
 *
 * @module $MODULE$
 * @returns {Backbone.View}
 */
define([
    'lodash',
    'backbone'

], function(
    _,
    Backbone

) {
    'use strict';

    var $MODULE$ = Backbone.View.extend({

        initialize: function(options) {
            _.bindAll(this,
                'render'
    
            );
        },
        
        events: {
            
        },

        $END$
    });

    return $MODULE$;
});
```
* `DESCRIPTION` - Module description
* `MODULE` - Module/class name

##### amdini_bbl
Init amd backbone simple layout
```
/**
 * $DESCRIPTION$
 *
 * @module $MODULE$
 * @returns {Backbone.View}
 */
define([
    'lodash',
    'backbone',
    'text!./jst/$TEMPLATE$.jst'

], function(
    _,
    Backbone,
    jstTemplate

) {
    'use strict';

    var $MODULE$ = Backbone.View.extend({
    
        template: _.template(jstTemplate),

        initialize: function(options) {
            _.bindAll(this,
                'render'
    
            );
        },
        
        events: {
            
        },
        
        render: function() {
            this.beforeRender();
            
            this.$el.html(this.template(this.serialize()));
            
            this.afterRender();
            return this;
        },
        
        serialize: function() {
            return {};
        },
        
        beforeRender: function() {},
        afterRender: function() {},

        $END$
    });

    return $MODULE$;
});
```
* `DESCRIPTION` - Module description
* `MODULE` - Module/class name
* `TEMPLATE` - Used JavaScript template

##### dp_singleton
Init Singleton class:
```
/**
 * $DESCRIPTION$
 *
 * @constructor $CLASSNAME$
 */
var $CLASSNAME$ = (function(){
    var instance = null;
    
    return function $CLASSNAME$($ARGS$) {
        if (instance) {
            return instance;
        }
        if (this && this.constructor === $CLASSNAME$) {
            // constructor
            $END$
          
            instance = this;
        } else {
            return new $CLASSNAME$.apply(this, arguments);
        }
    }
 })();
```
* `DESCRIPTION` - Class description
* `CLASSNAME` - Class name
* `ARGS` - Constructor arguments