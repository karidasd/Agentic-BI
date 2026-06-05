Thoroughly read and understand the PBIP knowledge base in the [kb-pbip](../.resources/kb-pbip.md) file.
Also review the [kb-html-cards](../.resources/kb-html-cards.md) file for generating custom visuals.

# Business Requirements 💼

Create a new semantic model named 'HR Analytics' and ensure the following requirements are met:

| Requirement ID | Description | User Story | Expected Behavior |
|---------------|-------------|------------|-------------------|
| **HR-001** | Total Active Employees | As an **HR Manager**, I want to see the total number of active employees so that I know the current headcount. | Create an [Active Employees] measure that counts employees where Status is 'Active' or TerminationDate is empty. |
| **HR-002** | Employee Turnover Rate | As an **Executive**, I want to see the turnover rate so that I can monitor employee retention. | Create [Terminations] and [Turnover Rate %] measures, ensuring proper relationship handling with the Calendar table based on TerminationDate. |
| **HR-003** | Average Training Hours | As an **L&D Manager**, I want to see the average training hours per employee so that I can track our investment in learning. | Create [Average Training Hours] measure using the FactEmployeePerformance table and join with DimEmployee. |
| **HR-004** | Custom HTML KPI Cards | As an **Executive**, I want a visually appealing custom KPI card for Turnover Rate. | Create a DAX measure `[Turnover Rate HTML Card]` that generates HTML and CSS code, compatible with the HTML Viewer visual, displaying the `[Turnover Rate %]` with conditional formatting (red if > 15%, green otherwise). Follow the `kb-html-cards` guide. |

# Data source information 🛢️

- **Server**: `hrserver.database.windows.net`
- **Database**: `HRDataWarehouse`

If you cannot connect to the SQL Server above to get the schema, all information of the Datawarehouse can be found in the file `AzureSQLSchema.csv`. 

# Development rules 🧑‍💻

- Analyze the datasource tables in `AzureSQLSchema.csv` and pick the tables that best answer the requirements. But dont bring any tables or columns that are not strictly necessary, when in doubt ask me.
- Use import storage mode for all tables.
- Don't create a new Calendar table, make sure you reuse Calendar table in the TMDL file `.resources/Calendar.tmdl` you may change names but keep exactly as-is. 
- Always prefer simple star-schema modeling and not snowflake.
- The created TMDL tables should have the necessary columns and measures to answer the requirements.
- The relationship between Calendar and fact table should be made using a datetime column. 
- All measures should be created in the source fact tables TMDL files, but do not duplicate measures they must be unique within the model. 
- The server and database name should be semantic model parameters
- Make sure you set descriptions on all created measures using business language
- Don't try to test the semantic model data

# Semantic Model Naming conventions 🏷️

- Use singular names for dimension tables
- Use plural names for fact tables
- All model object names should be lower case
- Don't use 'fact' or 'dim' in the table or column names. Prefer business friendly representation
- Measure names should follow a consistent naming convention: 
  - [measure name] for base measure
  - [measure name (ly)] for last year value of the base measure
  - [measure name (ytd)] for ytd value for the base measure
