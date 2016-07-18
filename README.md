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

        $END$
    });

    return $MODULE$;
});
```
* `DESCRIPTION` - Module description
* `MODULE` - Module/class name