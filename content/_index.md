---
title: Introduction
type: docs

---

# Introduction

## What is SAP?

When referring to SAP I am referring to SAP Enterprise Resource Planning (ERP), being the SAP system ERP Central Component (SAP ECC). ERP provides an integrated and continuously updated view of core business processes using common databases maintained by the database management system. SAP ECC tracks business resources (cash, raw materials, production capacity) and the status of business commitments (orders, purchase orders, and payroll). The modules that make up the system share data across various departments (manufacturing, purchasing, sales, accounting, etc.) that provide the data.

## Modules in ECC

System SAP ERP (previously SAP R/3) has a modular structure; that is, it contains a number of modules accessible via one login to the SAP ERP system (with the exception of SAP BW and SAP KW).

SAP ERP modules are widely known by their abbreviations. Modules are organized hierarchically; that is, they have submodules (e.g. Fixed Assets FI-AA is a submodule of Finance FI). Some modules are extensions of existing modules, but are not officially a submodule (e.g., Fleet Management FM is an extension of Plant Maintenance PM).

![SAP Modules](static\images\R3-sap-modules.jpg)

## SAP R/3, ECC and S/4HANA

SAP is known for changing the names of it's applications, sometimes for marketing purposes, sometimes because they merged products into a suite, or any other reason.

People that have been working with an application for a while a are already using a specific name, tent to keep using that "old" terminology. You can see the names mentioned above as just different versions of the ERP. It used to be called R3, then ECC and the latest version is S/4HANA.

### So What is HANA?

In a very simple way, HANA is just the database where the data is stored. Just this database run in-memory, which makes it really fast and can manage huge amounts of information without performance issues. SAP has been moving and developing most of it's application to run on HANA the same way it has been working on moving everything to a cloud offering.
