---
Title: displayAdminOrderSideBottom
hidden: true
hookTitle: 
files:
    -
        url: 'https://github.com/PrestaShop/PrestaShop/blob/8.0.x/src/PrestaShopBundle/Resources/views/Admin/Sell/Order/Order/view.html.twig'
        file: src/PrestaShopBundle/Resources/views/Admin/Sell/Order/Order/view.html.twig
locations:
    - 'back office'
type: display
hookAliases: 
hasExample: true
array_return: false
check_exceptions: false
chain: false
origin: core
description: ''

---

{{% hookDescriptor %}}

## Parameters details

```php
    <?php
    array(
      'id_order' => (int) Order ID
    );
```

## Call of the Hook in the origin file

```php
{{ renderhook('displayAdminOrderSideBottom', {'id_order': orderForViewing.id}) }}
```

## Example implementation

This hook has been implemented as an example in our [modules examples repository - demovieworderhooks](https://github.com/PrestaShop/example-modules/tree/8.x/demovieworderhooks).
