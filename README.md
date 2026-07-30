# AI-Augmented-PowerBI-Dashboard
## Project Overview

This project aims to build an interactive **Sales Analytics Dashboard** in **Power BI**, providing comprehensive insights through **Sales**, **Product**, and **Customer** views. The dashboard is designed to help stakeholders analyze business performance, monitor key performance indicators (KPIs), and make data-driven decisions using intuitive visualizations and dynamic reports.

The project leverages **Claude's Model Context Protocol (MCP) integration** with **Power BI Desktop** to streamline data modeling, manage semantic relationships, and assist in creating robust **DAX measures**. This AI-assisted workflow accelerates the development of accurate calculations while maintaining a scalable and well-structured semantic model for business reporting.

## Data Source

The project uses **4 CSV files** as the data source:

* **Customer.csv** – Customer information and attributes
* **Product.csv** – Product details and categories
* **Sales.csv** – Transactional sales data
* **calendar.csv** – Calendar table for time-based analysis and DAX calculations

## Connect Claude with Power BI
Tools used : VS code (As a middleman between Claude and Power BI) , Claude Desktop and Power BI Desktop
Follow instructions given in the video : https://www.youtube.com/watch?v=OrJpkD7XHt0  

## Connecting Claude with Power BI Desktop

> **Note:** For the initial setup, watch and follow the tutorial from the **13:00** timestamp onward.

A simple prompt in Claude establishes the connection with the active Power BI Desktop instance.

```text
Connect to the active Power BI Desktop instance.
```

<p align="center">
  <img width="1076" height="563" alt="Claude connected to Power BI" src="https://github.com/user-attachments/assets/663f60cf-2c19-45cf-ac48-5d10ba8c1bb2" />
</p>

After selecting the Power BI Desktop instance, Claude confirms that the connection has been established successfully.

<p align="center">
  <img width="1102" height="297" alt="Connection successful" src="https://github.com/user-attachments/assets/ab90a59d-fb9b-42d2-87ae-86619345691f" />
</p>

Once connected, you can instruct Claude to interact directly with your semantic model, including creating DAX measures, validating calculations, inspecting the model, and assisting with data modeling tasks.

---

## My Findings

While experimenting with Claude MCP integration, I observed the following:

* Creating an **empty semantic model** and asking Claude to import CSV files using file paths was significantly slower and occasionally resulted in data loading issues that required additional debugging.
* A more reliable workflow was to **import the data into Power BI using the standard *****Get Data***** experience**, and then connect Claude to the existing Power BI model.
* After the tables were loaded, Claude was able to **read and debug the Power Query (M) layer**, not just the DAX layer.
* I validated customer data using Claude, and it correctly interpreted the transformations defined in Power Query, demonstrating an understanding of the complete semantic model.

---

## Building Relationships

Creating relationships was remarkably straightforward. A single prompt was sufficient:

```text
Create all the relationships among the tables.
```

Claude automatically:

* Created the required table relationships.
* Correctly identified and marked the **Date** table as the official date table.
* Configured the model with the appropriate relationship structure.

<p align="center">
  <img width="1190" height="656" alt="Relationships created by Claude" src="https://github.com/user-attachments/assets/4f86dc66-0a70-4680-972b-d55223c6b8ac" />
</p>

Claude also generated a clean summary of the semantic model, including table names and their relationships, making it easy to review and validate the overall data model.

<p align="center">
  <img width="815" height="342" alt="Semantic model summary" src="https://github.com/user-attachments/assets/c10d922a-cb29-47a5-9e7f-475744906a39" />
</p>





Then after getting data from the above sources , what are the actions performed by Claude ? Prompts given ? Result of each prompts ?
What is the work done manually ? 





