How to mixins Js in Magento 2

This is example for modifier submitFrom function of catalogAddToCart widget
Before and after submi form I want to do something.
Let me step by step

Add mixins config to requirejs-config.js
```js
var config = {
    config: {
        mixins: {
            'Magento_Catalog/js/catalog-add-to-cart': {
                'Vendor_Module/js/catalog-add-to-cart-mixin': true
            }
        }
    }
};
```

Create new file catalog-add-to-cart-mixin.js

```js
define([
    'jquery',
    'mage/translate',
    'mage/url',
    'jquery/ui',
], function ($, $t, url) {
    'use strict';

    return function (widget) {

        $.widget('mage.catalogAddToCart', widget, {
            submitForm: function (form) {

                //do something
                this._super(form);
                //do something
                return this;
            }
        });

        return $.mage.catalogAddToCart;
    }
});
```
