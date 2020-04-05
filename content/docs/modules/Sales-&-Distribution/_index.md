---
title: Sales & Distribution
weight: 10
---

# Sales & Distribution (SD)

## What is SD?

SAP Sales and Distribution (SAP SD) is a core functional module in SAP ERP Central Component (ECC) that allows organisations to store and manage customer and product related data. Organisations use this data to manage all of the sales ordering, shipping, billing, and invoicing of their goods and services.

SAP SD is part of SAP ECC's Logistics function and integrates with other modules, including Production Planning (PP), Plant Maintenance (PM), Quality Management (QM), Materials Management (MM), Finance and Controlling (FICO), and Human Resources (HR).

## The Sales Process

Working in conjunction with the other modules, SAP SD enables an order-to-cash business process. SD handles all the details in the sales and distribution part of the process. In a typical cycle, SD will create:

1. A Quote to the Customer
2. The customer then places a Sales Order
3. The goods are Picked from a Warehouse or production facility
4. The goods are Shipped to the Customer
5. An Invoice is sent to the Customer  
6. Accounts Receivable settles the payment with the Customer

Each step in the process generates transactions in the SD module, which then generate further transactions in the other system modules. For example, when a sales order is generated in SD, it establishes a link for a product availability check to MM, a credit check to FICO, or a tax calculation to FICO.

## SD Sub-modules

SAP SD consists of several sub-modules that can be configured to handle specific functions in the module:

- SD Master Data (SD-MD) tracks each transaction that affects the SD module's data, including customer data, materials data, price condition records, and credit management.
- SD Basic Functions (SD-BF) allows you to establish the basic functions that work across SD, such as pricing, goods availability check and credit management.
- SD Sales (SD-SLS) handles the details of the sales process, such as customer data, products, pricing and feedback.
- SD Shipping (SD-SHP) tracks the details of the shipping process, including when and how the order is shipped through to delivery or return.
- SD Transportation (SD-TBA) works closely with SD-SHP and keeps track of all the transportation data involved in the shipment.
- SD Foreign Trade (SD-FTT) handles the details related to foreign trade transactions, including both exports and imports.
- SD Billing (SD-BIL) manages billing data, including the amounts of the transactions and methods of payment.
- SD Sales Support (SD-CAS) handles the data generated in the interactions between customers and sales teams.
