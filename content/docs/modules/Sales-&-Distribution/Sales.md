---
title: Sales
Date: 2020-04-06
weight: 2
tag: []
---
# Sales

[sales overview diagram]
describe sales process and overview
pre-sale > sales order > proc > shipping > billing > payment > recovery

## Sales processing

[SD document overview]

These SD documents are discussed below, including how to create.

### Sales Orders
what is it? what is its purpose in SAP?
#### Structure
#### Create SO

### Outbound Delivery
what is it? what is its purpose in SAP?
#### Structure
#### Create Outbound Delivery

### Pick Stock
what is it? what is its purpose in SAP?
#### Structure
#### Create Picking Request

###Post Goods Issue
what is it? what is its purpose in SAP?
#### Structure
#### Create Post Goods Issue

### Billing (invoice)
what is it? what is its purpose in SAP?
#### Structure
#### Create Billing Document

### Post customer payment ...?

## Document flow
The documents in a sales process are linked to each other using the document flow. This enables you to access the history and current status of your sales processes at any time.

[document flow]

You can display the document flow as a list of linked documents. All preceding and succeeding documents are displayed, depending on the document you call the list from. From this list, you can display the relevant documents or call up status overviews for the documents.

The document flow is updated on the document header and document line level. Only sales documents contain schedule lines. Since each schedule line contains its own delivery date, each deliverable schedule line becomes an item in a delivery document. Therefore delivery documents and billing documents do not need schedule lines.
