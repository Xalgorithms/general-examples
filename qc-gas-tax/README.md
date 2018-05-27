## Rule: Quebec Border-Proximity Gas Tax

This rule operates on documents that are prepared by the Lichen application, originating as UBL invoices. It selects invoices that apply to consumer petrol sales (using ISIC and UNSPSC) coding. For any items in the invoice that required UNSPSC code, it will generate a revision that adds an allowance (discount) to the invoice.

This rule only applies to invoices from suppliers in the consumer petrol industry (ISIC/G4711).

```
WHEN envelope:type == 'invoice';
WHEN envelope:parties.supplier.industry.list_id == 'ISIC';
WHEN envelope:parties.supplier.industry.value == 'G4711';
```

This rule only operates on invoice items that are coded as consumer petrol (UNSPSC/506505).

```
WHEN item:classification.list_name == 'UNSPSC';
WHEN item:classification.value == '506505';
WHEN item:quantity.value > 0;
```



