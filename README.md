This repository showcases Agentic AI development in Power BI, specifically tailored for an **HR Analytics** use case.

# 🔍 What is Agentic Development?

Agentic development is a new paradigm where developers shift from writing code or using UI applications to guiding intelligent agents. The developer defines the what - the requirements, rules, and intent - and the AI agent handles the how - generating specs, implementing the model, running validations, fixing issues, and iterating toward a working solution. 

In Power BI, this is made possible by open file formats with [Power BI Project file format](https://learn.microsoft.com/power-bi/developer/projects/projects-overview) and the [TMDL language](https://learn.microsoft.com/analysis-services/tmdl/tmdl-overview), which provide structure and linting AI agents can use to reason, check, and improve their own work. 

# ⚙️ How does it work?

1. You describe what you need – your [requirements](.requirements/requirements-01.md) and the [rules](.resources/kb-pbip.md) the agent should follow.
2. An AI agent turns that into a development spec – readable, reviewable, and adjustable.
3. You say "Go" and the agent starts implementing the spec autonomously.
4. It runs its own best practice checks, fixes issues, and iterates until it gets it right.
5. You open the Power BI application and review the result, just like you would with a teammate’s pull request.

# 🧪 Example Included

This repository comes with an HR Analytics example, tracking active employees, turnover rate, and training hours based on an HR data warehouse schema. Check the `.requirements` folder for the details.
