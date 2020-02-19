# toXPATH.sh

- [Overview](#overview)
- [Flowchart](#flowchart)
- [Reuirement](#requirement)
- [Usage](#usage)
- [License](#license)
- [Author](#author)

## Overview

Run `$> ./toXPATH.sh -h`

Exchanging format to (like) XPATH from validated XML.

Shell script source-code is [gist(github) ulid.sh](https://gist.github.com/search?q=user%3Atd-shi+filename%3A.sh+toXPATH) .

## Flowchart

![Flowchart](./toXPATH_sh.SVG "Flowchart")

## Requirement

- Only POSIX command.

## Usage

The [test.xml](./test.xml) is [ConsolidatedPurchaseOrders.xml](https://docs.microsoft.com/ja-jp/dotnet/visual-basic/programming-guide/concepts/linq/sample-xml-file-consolidated-purchase-orders) .

```
$> cat test.xml | toXPATH.sh
/PurchaseOrders[1]@xmlns www.contoso.com
/PurchaseOrders[1]/PurchaseOrder[1]@PurchaseOrderNumber 99503
/PurchaseOrders[1]/PurchaseOrder[1]@OrderDate 1999-10-20
/PurchaseOrders[1]/PurchaseOrder[1]/Address[1]@Type Shipping
/PurchaseOrders[1]/PurchaseOrder[1]/Address[1]/Name[1] Ellen Adams
/PurchaseOrders[1]/PurchaseOrder[1]/Address[1]/Street[1] 123 Maple Street
/PurchaseOrders[1]/PurchaseOrder[1]/Address[1]/City[1] Mill Valley
/PurchaseOrders[1]/PurchaseOrder[1]/Address[1]/State[1] CA
/PurchaseOrders[1]/PurchaseOrder[1]/Address[1]/Zip[1] 10999
/PurchaseOrders[1]/PurchaseOrder[1]/Address[1]/Country[1] USA
/PurchaseOrders[1]/PurchaseOrder[1]/Address[2]@Type Billing
/PurchaseOrders[1]/PurchaseOrder[1]/Address[2]/Name[1] Tai Yee
/PurchaseOrders[1]/PurchaseOrder[1]/Address[2]/Street[1] 8 Oak Avenue
/PurchaseOrders[1]/PurchaseOrder[1]/Address[2]/City[1] Old Town
/PurchaseOrders[1]/PurchaseOrder[1]/Address[2]/State[1] PA
/PurchaseOrders[1]/PurchaseOrder[1]/Address[2]/Zip[1] 95819
/PurchaseOrders[1]/PurchaseOrder[1]/Address[2]/Country[1] USA
/PurchaseOrders[1]/PurchaseOrder[1]/DeliveryNotes[1] Please leave packages in shed by driveway.
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[1]@PartNumber 872-AA
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[1]/ProductName[1] Lawnmower
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[1]/USPrice[1] 148.95
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[1]/Comment[1] Confirm this is electric
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[2]@PartNumber 926-AA
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[2]/ProductName[1] Baby Monitor
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[2]/USPrice[1] 39.98
/PurchaseOrders[1]/PurchaseOrder[1]/Items[1]/Item[2]/ShipDate[1] 1999-05-21
/PurchaseOrders[1]/PurchaseOrder[2]@PurchaseOrderNumber 99505
/PurchaseOrders[1]/PurchaseOrder[2]@OrderDate 1999-10-22
/PurchaseOrders[1]/PurchaseOrder[2]/Address[1]@Type Shipping
/PurchaseOrders[1]/PurchaseOrder[2]/Address[1]/Name[1] Cristian Osorio
/PurchaseOrders[1]/PurchaseOrder[2]/Address[1]/Street[1] 456 Main Street
/PurchaseOrders[1]/PurchaseOrder[2]/Address[1]/City[1] Buffalo
/PurchaseOrders[1]/PurchaseOrder[2]/Address[1]/State[1] NY
/PurchaseOrders[1]/PurchaseOrder[2]/Address[1]/Zip[1] 98112
/PurchaseOrders[1]/PurchaseOrder[2]/Address[1]/Country[1] USA
/PurchaseOrders[1]/PurchaseOrder[2]/Address[2]@Type Billing
/PurchaseOrders[1]/PurchaseOrder[2]/Address[2]/Name[1] Cristian Osorio
/PurchaseOrders[1]/PurchaseOrder[2]/Address[2]/Street[1] 456 Main Street
/PurchaseOrders[1]/PurchaseOrder[2]/Address[2]/City[1] Buffalo
/PurchaseOrders[1]/PurchaseOrder[2]/Address[2]/State[1] NY
/PurchaseOrders[1]/PurchaseOrder[2]/Address[2]/Zip[1] 98112
/PurchaseOrders[1]/PurchaseOrder[2]/Address[2]/Country[1] USA
/PurchaseOrders[1]/PurchaseOrder[2]/DeliveryNotes[1] Please notify by email before shipping.
/PurchaseOrders[1]/PurchaseOrder[2]/Items[1]/Item[1]@PartNumber 456-NM
/PurchaseOrders[1]/PurchaseOrder[2]/Items[1]/Item[1]/ProductName[1] Power Supply
/PurchaseOrders[1]/PurchaseOrder[2]/Items[1]/Item[1]/USPrice[1] 45.99
/PurchaseOrders[1]/PurchaseOrder[3]@PurchaseOrderNumber 99504
/PurchaseOrders[1]/PurchaseOrder[3]@OrderDate 1999-10-22
/PurchaseOrders[1]/PurchaseOrder[3]/Address[1]@Type Shipping
/PurchaseOrders[1]/PurchaseOrder[3]/Address[1]/Name[1] Jessica Arnold
/PurchaseOrders[1]/PurchaseOrder[3]/Address[1]/Street[1] 4055 Madison Ave
/PurchaseOrders[1]/PurchaseOrder[3]/Address[1]/City[1] Seattle
/PurchaseOrders[1]/PurchaseOrder[3]/Address[1]/State[1] WA
/PurchaseOrders[1]/PurchaseOrder[3]/Address[1]/Zip[1] 98112
/PurchaseOrders[1]/PurchaseOrder[3]/Address[1]/Country[1] USA
/PurchaseOrders[1]/PurchaseOrder[3]/Address[2]@Type Billing
/PurchaseOrders[1]/PurchaseOrder[3]/Address[2]/Name[1] Jessica Arnold
/PurchaseOrders[1]/PurchaseOrder[3]/Address[2]/Street[1] 4055 Madison Ave
/PurchaseOrders[1]/PurchaseOrder[3]/Address[2]/City[1] Buffalo
/PurchaseOrders[1]/PurchaseOrder[3]/Address[2]/State[1] NY
/PurchaseOrders[1]/PurchaseOrder[3]/Address[2]/Zip[1] 98112
/PurchaseOrders[1]/PurchaseOrder[3]/Address[2]/Country[1] USA
/PurchaseOrders[1]/PurchaseOrder[3]/DeliveryNotes[1] Please do not deliver on Saturday.
/PurchaseOrders[1]/PurchaseOrder[3]/Items[1]/Item[1]@PartNumber 898-AZ
/PurchaseOrders[1]/PurchaseOrder[3]/Items[1]/Item[1]/ProductName[1] Computer Keyboard
/PurchaseOrders[1]/PurchaseOrder[3]/Items[1]/Item[1]/USPrice[1] 29.99
/PurchaseOrders[1]/PurchaseOrder[3]/Items[1]/Item[2]@PartNumber 898-AM
/PurchaseOrders[1]/PurchaseOrder[3]/Items[1]/Item[2]/ProductName[1] Wireless Mouse
/PurchaseOrders[1]/PurchaseOrder[3]/Items[1]/Item[2]/USPrice[1] 14.99
/PurchaseOrders[1]/aw:PurchaseOrder[1]@PONumber 11223
/PurchaseOrders[1]/aw:PurchaseOrder[1]@Date 2000-01-15
/PurchaseOrders[1]/aw:PurchaseOrder[1]@xmlns:aw http://www.adventure-works.com
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:ShippingAddress[1]/aw:Name[1] Chris Preston
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:ShippingAddress[1]/aw:Street[1] 123 Main St.
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:ShippingAddress[1]/aw:City[1] Seattle
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:ShippingAddress[1]/aw:State[1] WA
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:ShippingAddress[1]/aw:Zip[1] 98113
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:ShippingAddress[1]/aw:Country[1] USA
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:BillingAddress[1]/aw:Name[1] Chris Preston
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:BillingAddress[1]/aw:Street[1] 123 Main St.
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:BillingAddress[1]/aw:City[1] Seattle
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:BillingAddress[1]/aw:State[1] WA
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:BillingAddress[1]/aw:Zip[1] 98113
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:BillingAddress[1]/aw:Country[1] USA
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:DeliveryInstructions[1] Ship only complete order.
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:Item[1]@PartNum LIT-01
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:Item[1]/aw:ProductID[1] Litware Networking Card
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:Item[1]/aw:Price[1] 20.99
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:Item[2]@PartNum LIT-25
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:Item[2]/aw:ProductID[1] Litware 17in LCD Monitor
/PurchaseOrders[1]/aw:PurchaseOrder[1]/aw:Item[2]/aw:Price[1] 199.99

```

## License

- [CC0(Public domain)](https://creativecommons.org/publicdomain/zero/1.0/legalcode)

## Author

[TD](https://github.com/td-shi/)
