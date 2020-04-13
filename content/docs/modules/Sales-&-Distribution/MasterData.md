---
title: Master Data
Date: 2020-04-07
tags: []
weight: 3
---

# Master Data

Several sources of data can be copied into a sales order or into another sales and distribution document. Most of them are default values that you can overwrite in the sales and distribution document, if necessary. These sources of data include, for example:

- Customer master data
-	Material master data
-	Condition master data
-	Output information

## Customer Master Data

The customer master groups data into categories: general data, sales area data, and company code data. The customer master includes all data necessary for processing orders, deliveries, invoices, and customer payments.

![Customer Master Data](/images/SD-cust-MD-overview.png)

Customer Master Data will be needed for returning/ regular customers. For one-time customers, a "one-time customer" record is used.

To create a customer master data, use either:

```
TCODE = VD01
Menu path = Logistics/ Sales and distribution/ Master data/ Business partners/ Customer/ Create/ Sales & Distribution
```

### General Data

The general data is relevant for sales and distribution and for accounting. It is stored centrally (client-specific), in order to avoid data redundancy. It is valid for all organisational units within a client. In order to maintain the general data in the customer master that is relevant for sales and distribution and accounting, the data fields are grouped on several tab pages.

The general data in the customer master is set out on the following tab pages:

![Customer General Data](/images/SD-cust-MD-general.png)

By changing the Customizing settings, you can hide certain fields on a tab page or make them required entry fields. The general data is maintained independently of the organizational units.

Note that when you change a master record after having used it to create documents (orders, deliveries, billing documents, etc), the changes do not affect the documents already created. However, the address in the customer master is an exception. Therefore, if it was necessary, you would have to change the data in the documents manually, except for the address.

### Sales Area Data

The sales area data is relevant for sales and distribution. It is valid for the respective sales area (sales organization, distribution channel, division). You can maintain the sales area data in various ways, depending on the sales area (sales organization, distribution channel, division).

The sales area data in the customer master is set out on the following tab pages:

![Customer Sales Area Data](/images/SD-cust-MD-sales-area.png)

By changing the Customizing settings, you can hide certain fields on a tab page or make them required entry fields.

#### Partner Functions in Sales Area Data

You store the partner functions for the customer master in the customer master sales area data (tab page Partner functions). When processing a sales order, they are copied as default values into the documents.

The following obligatory functions are necessary for sales order processing: ***Sold-to party, ship-to party, bill-to party, and payer.*** In the course of processing a sales order, they can differ from each other or can be identical.

-	Sold-to party: places the order.
-	Ship-to party: receives goods or services.
-	Bill-to party: receives the invoice for goods or services.
-	Payer: is responsible for paying the invoice.
-	Other partner functions, such as contact person or forwarding agent, are not necessary for sales order processing.

### Company Code Data

The company code data is relevant for accounting. It is valid for the respective company code. In order to maintain the company code data relevant for accounting in the customer master, the data fields are grouped on several tab pages. You can maintain the company code data in various ways, according to the company code.

The company code data in the customer master comprises the following tab pages:

![customer Company Data](/images/SD-cust-MD-company.png)

By changing the Customizing settings, you can hide certain fields on a tab page or make them required entry fields.

## Material Master Data

The material master is grouped into several views: Basic data, sales and distribution data, purchasing data, various further data for engineering/design, accounting, costing, warehouse management, and so on.

![Material Data Overview](SD-material-MD-overview.png)

There is additional data for several other areas. This is valid for various organisational units.

When looking at the Sales Tab page on the Material Master, you will see several tab pages that are valid for sales and distribution.

![Materials Data Sales Tab](/images/SD-material-MD-salestab.png)

-	Basic data is relevant for all areas. It is maintained independently of organisational units.
-	Sales Org. 1 data, Sales Org. 2 data, and the sales texts are valid for the sales organisation and the distribution channel.
-	Sales: General/Plant data and Foreign Trade: Export data is valid for the delivering plant.

By changing the Customizing settings, you can hide certain fields on a tab page or make them required entry fields.

## Customer-Material Information

You can use the customer-material information to record data for a combination of  certain customers and materials. If a customer-material info exists for a customer and a material, these default values are preferred to the values from the customer or the material master when processing a document (order or delivery).

You can use the customer-material information record to maintain the following data:
-	Cross-reference from your customer's material number to your material number and the customer's material description.
-	Specific shipping information for this customer and material (such as delivery tolerances, specifying if the customer accepts partial deliveries, or the default delivering plant).

## Outputs

Outputs are information that is sent to the customer using various media, such as mail, EDI, or fax. Examples include: the printout of a quotation or an order confirmation, order confirmations using EDI, or invoices by fax. As with pricing, output determination takes place using the condition technique. Output can be sent for various sales and distribution documents (order, delivery, billing document).

In the output master data, you define the transmission medium, the time, and the partner function for an output type.

- Output types include, for example: quotation, order confirmation, invoice.
- Partner functions include, for example: sold-to party, ship-to party, and bill-to party.
- Transmission media include, for example: printer, telex, fax, mail, EDI.
- Times at which output is sent include: immediately when saving, or by using a standard program (RSNAST00) that is run regularly.

The layout of an output is defined by a form in a functional specification. The form is assigned to an output type.

## Incompletion Log

Each sales and distribution document contains data required for the document and for further processing. The system determines which fields are displayed in the incompletion log when the user does not fill them during sales order processing.

The incompletion log will be displayed automatically when you save your entries. You can also call it by choosing Edit -> Incompletion log. In Customizing, you can decide which fields should be part of the incompletion log.

The incompletion log functions are available in the sales order and in the delivery.

## Condition Master Data (Pricing)

The condition master data includes prices, surcharges and discounts, freights, and taxes. You can define condition master data (condition records) to be dependent on various data. You can, for example, maintain a material price customer-specifically or define a discount to be dependent on the customer and the material pricing group.   

![Condition Data Overview](/images/SD-condition-MD-overview.png)

In Customizing, you can control the data on which prices, surcharges and discounts, freights or taxes can be dependent.  (You can define conditions to be dependent on any document fields). Frequently occurring cases have already been set in the standard system.

The condition type defines multiple uses of a condition. You can have a percentage, a quantity-dependent, or an amount-dependent surcharge or discount, depending on the condition type.

By specifying a validity period, you can restrict a price agreement to a certain period. You can maintain values within a condition record (price, surcharge, discount) according to a scale. There is no limit to the number of scale levels.

## Common Master Data

### Common Distribution Channel

If you do not need the master data (customer / material and condition master data) to be differentiated according to distribution channels, you have to set up a representative distribution channel (the common distribution channel). The master data for the representative distribution channel applies to all distribution channels for which you have set up this reference in Customizing.

By doing this, you can minimize the effort of entering and maintaining master data (customer / material and condition master data). In addition, you can update statistics for distribution channels without having to create master data for the various distribution channels.

### Common Division

If you do not need the master data (customer or condition master data) to be differentiated according to divisions, you have to set up a representative division (the common division). The master data in the representative division applies to all divisions for which you have set up this reference in Customising.

By doing this, you can minimise the effort of entering and maintaining master data. In addition, you can update statistics for divisions without having to create master data for the various divisions.
