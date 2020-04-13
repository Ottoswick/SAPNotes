---
title: SD
---
# SD Cheat Sheet

Transaction codes for Sales and Distribution.

## Master Data

TCODE | Description
:--- | :---
XD01/02/03 | Create/Change/Display Customer. Data can be entered on the different levels (e.g. at Company code, Sales Area)
XD04 | Display change documents – Track the changes for customer master
XD05 | To block Customer on different levels (global or sales areas)
VK11/12/13 | Create/ change/ display conditions (e.g. price discounts)
VB01/02/03 | Create/ change/ display Listing/ Exclusion. Used to restrict customers buying choice. If materials are on the exclusion list customer cannot buy them. If Listing is used, customer can buy materials only from the Listing list. It is possible to set by customer group and material group.
VB11/12/13 | Create/ change display Material determination - manage material substitutions
VD51/52/53 | Create/ change/ display customer-material master record
CS61/62/63 | Create/ change / display sales order bill material

## Credit management

TCODE | Description
:--- | :---
FD32/33 | Change/ display customer credit management
F.34 | Mass change customer credit management
VKM4 | To release blocked SD document

## Sales

TCODE | Description
:--- | :---
VA41/42/43 | Create/ change/ display contract
VA11/12/13 | Create/ change/ display inquiry
VA21/22/23 | Create/change/ display quotation
VA01/02/03 | Create/ change/ display order (sales orders, credit/ debit memos requests, returns and consignments)
VA51/52/53 | Create/ change/ display item proposal
C009 | Stock availability overview
VB01/02/03 | Create/ change/ display rebate agreement
VB(D | Extended rebate agreement to extend the validity date of the existing agreement

## Billing

TCODE | Description
:--- | :---
VF01/02/03 | Create/ change/ display billing documents
VF11 | Cancel billing document. Appropriate reversal reason must be entered
VB0F | Update billing documents
VF31 | Issue billing documents

## Shipping & Transport

TCODE | Description
:--- | :---
VL01N/02N/03N | Create/ change/ display outbound delivery
VL10 | Collective processing of documents sue for delivery creation
VL10B | Collective processing for Stock Transfer Order (used to create mass outbound deliveries for STO)
VL71 | Outbound delivery output
VT01N/02N/03N | Create/ change / display shipment
VT06 | Shipment mass changes
VLPOD | Use to process proof of delivery in order to proceed further with billing creation. If Proof of Delivery is conﬁgured in customer master, the invoice cannot be issued until the customer conﬁrms the goods are received

## Reports

TCODE | Area | Description
:--- | :--- | :---
VD59 | Master Data | Line customer-material information
VCUST | Master Data | Customer List
V/LD | Master Data | Pricing reports
VKM1 | Credit Management | Blocked SD documents
VKM2 | Credit Management | Released SD documents
VA15 | Sales | Inquiries List
VA25 | Sales | Quotation List
VA05N |Sales | List of sales orders
VA45 | Sales | List of contracts
FBL5N | Billing | Display billing documents per account with document status (cleared/ open items)
VF05N | Billing | List of billing documents
VB(8 | Billing | List rebate agreements
VL06O | Shipping | Outbound delivery monitor
VT11 | Shipping | Transportation planning list
VT12 | Shipping | Shipment completion List
VT14 | Shipping | Utilisation list
