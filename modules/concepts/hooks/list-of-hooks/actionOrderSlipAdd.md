---
Title: actionOrderSlipAdd
hidden: true
hookTitle: 'Order slip creation'
files:
    -
        url: 'https://github.com/PrestaShop/PrestaShop/blob/8.0.x/src/Adapter/Order/Refund/OrderSlipCreator.php'
        file: src/Adapter/Order/Refund/OrderSlipCreator.php
locations:
    - 'back office'
type: action
hookAliases:
    - orderSlip
array_return: false
check_exceptions: false
chain: false
origin: core
description: 'This hook is called when a new credit slip is added regarding client order'

---

{{% hookDescriptor %}}

## Parameters details

```php
    <?php
    array(
      'order' => Order,
      'productList' => array(
        (int) order detail ID 1 => Order Slip Detail 1,
        (int) order detail ID 2 => Order Slip Detail 2,
        ...,
        (int) order detail ID n => Order Slip Detail n
      ),
      'qtyList' => array(
        (int) order detail ID 1 => (int) quantity 1,
        (int) order detail ID 2 => (int) quantity 2,
        ...,
        (int) order detail ID n => (int) quantity n 
      )
    );
```

## Call of the Hook in the origin file

```php
Hook::exec('actionOrderSlipAdd', [
                'order' => $order,
                'productList' => $orderRefundSummary->getProductRefunds(),
                'qtyList' => $fullQuantityList,
            ], null, false, true, false, $order->id_shop)
```
