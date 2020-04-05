---
title: Enterprise Structure
date: 2020-04-05
weight: 1
tags: ["sales, enterprise structure, master data"]
---
# Enterprise Structure

## Business Scenario

In any business scenario there a multiple elements that come together that allow us to define the process. The Enterprise Structure or Organisational Unit is a the makeup of the business to enable the process. The main elements that comprise a business scenario as defined by SAP are:

- **Organisational Unit**: Organisational grouping of enterprise areas which, for legal reasons or for other specific business-related reasons or purposes, are grouped together. Organisational units are mapped to the system Enterprise Structure and include legal entities (Company Codes), Sales Offices, and Profit Centers.
- **Master Data**: Data which is used long-term in the system for several business processes.  Examples include Customers, Materials, and Vendors.
- **Transactions**: Application programs which execute business processes in the system such as creating a customer order, posting an incoming payment, or approving a leave request.
- **Document**: A data record that is generated when a transaction is carried out.
- **Reports**: Program which reads certain data elements and displays them in a list.

## Enterprise Structure

Organisational Units are mapped to the system Enterprise Structure. Units may be mapped to one application in the enterprise structure (i.e. Sales unit to Sales and Distribution) or may be mapped to many (i.e. a plant to Materials Management and to Production Planning).

Overview Enterprise Structure:  
![Overview](/static/images/ent-str-overview.png)

An enterprise is structured in the SAP system according to business functions that must correspond to the functionality assigned to the organisational units.

Examples:
-	A Company Code is a unit included in the balance sheet of a legally-independent enterprise. It is the central organisational element of Financial Accounting.
-	The Controlling Area is the business unit where Cost Accounting is carried out. For the purpose of company-wide cost accounting, one controlling area can handle cost accounting for several company codes in one enterprise.
-	In the context of Sales and Distribution, the Sales Organization is central organisational element that controls the terms of sale to the customer.  Distribution Channel is the element that describes through what channel goods and/or services will be distributed to the customer.
-	In the context of Production Planning and Control, the Plant is the central organizational unit. A plant is the place of production or simply a collection of several locations of material stocks in close physical proximity.
-	A Storage Location is a storage area comprising warehouses in close proximity. Material stocks can be differentiated within one plant according to storage location (inventory management).

The SD module is integrated with other modules in order to deliver the order to cash process. These modules integrate per below:
![SD integration](static\images\SD-integration-R3.png)

## Organisational Structures in sales

The configurable units available in SAP to model the business sales process are:

- Sales Organisation
- Distribution Channel
- Division
- Sales Area
- Sales Office
- Sales Group

O­ther organisational units in SD, such as the shipping point and the transportation planning point, are covered in other SD courses.

### Sales Organisation

The Sales Organisation represents the highest organisational unit in SD. Each Sales Organisation represents a selling unit as a legal entity. It is, for example, responsible for product liability and other customer rights of recourse. You can use sales organisations to subdivide markets into regions. Each business transaction is processed within a sales organisation.
- A sales organisation is assigned to exactly one company code.
- A sales organisation is assigned to one or more plants.
- Each sales organisation has its own master data, for example, its own customer and material master data as well as condition records (although this master data can be extended or shared between Sales Organisations if needed with additional config.).

### Dsitribution Channel

Distribution channels provide a general structure for distributing goods. Wholesale trade, sales to industrial customers or direct sales from a plant are typical examples of distribution channels.
- Distribution channels can be set up according to your company's market strategy or internal organization.
- Customers can be served through one or more distribution channels within a sales organization.
- In addition, you can vary the master data relevant to sales, such as customer master data, sales master data, prices, and surcharges/discounts, for each sales organization and distribution channel.

### Division

A broad product range can be divided into divisions. In the SAP system, you can also define a division-specific sales structure.

You can make customer-specific agreements for each division, for example regarding partial deliveries or pricing. Within a division, you can carry out statistical analyses or devise your own marketing strategies.

### Sales Area

![Sales Are](static\images\SD-sales-area.png)

Sales Area is a combination of sales organization, distribution channel and division. Sales documents, delivery documents, and billing documents are always assigned to a sales area. Every sales process always takes in a specific sales area. The relevant master data can usually be maintained explicitly for each sales area, for example:

- Sales-relevant customer master data
- Sales-relevant material master data (the division is a general field of the material master; as a result, a material can only be assigned to one division.)
- Conditions (prices, discounts/surcharges)

You can carry out analyses within a sales area, for example, by evaluation sales volume. It is best practice to keep the organisational structure of a sales area as simple as possible.

### Sales Office and Sales Group

![Sales Office and Sales Group](static\images\SD-salesoffice-salesgrp.png)

#### Sales office
Geographical aspects of the organisational structures in business development and sales are defined using sales offices. A sales office can be viewed as an actual office or perhaps a territory or region. Sales offices are assigned to sales areas. If you enter a sales order for a sales office within a particular sales area, the sales office must be permitted for that sales area. A sales office can be assigned to more than one sales area.

#### Sales group
Employees of a sales office can be assigned to sales groups defined for each division or distribution channel. Sales groups are assigned to sales offices.

#### Salesperson
A sales group consists of a certain number of salespersons. A salesperson is assigned to a sales office and group in the sales employee master record. Thereafter you can select this personnel master record in the partner screen of a sales document.

### Plants

Production facilities (Plants) and locations for storing stock (Storage Locations) must be defined in the system to allow for flow of materials within the company. Material stocks can be described in detail at the level of different storage locations within a plant. A plant can either be a location for production and material requirements planning (MRP) or it may simply represent one or more material stock locations in close proximity to one another.

For a plant to deliver goods to customers, it must be configured as a delivering plant in SD customising. During the sales process, the delivering plants are first used to verify the stocks, and later to supply the goods the customer has ordered.

Plants are assigned to each sales organisation. The plants that are used depends on the Distribution Channel. Any one sales organisation can sell goods from several plants. A plant can be assigned to different sales organizations at any one time, all of which can sell from the same plant.

A sales organisation can also sell products supplied by a plant which is assigned to a different company code (inter-company sales processing).
