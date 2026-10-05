# Reflection

Working on the BrewMetrics BI project with GitHub Copilot made the development process more structured and helped me move faster when designing the data model and DAX measures. Copilot was directly useful when suggesting a star-schema structure and providing initial DAX patterns for sales analysis. The suggestions gave me a starting point instead of requiring every formula to be written from scratch.

However, the Copilot suggestions still needed to be checked against the actual Power BI model. For example, Copilot suggested column references such as `SalesAmount` and `Date`, while the imported model used `sales_amount` and `date`. I had to correct these references before implementing the measures. This showed that Copilot can provide useful code but does not replace checking the actual schema.

Maintaining the project through GitHub also changed my workflow. Instead of making all changes and saving the final version at once, I separated the schema, individual DAX measures and dashboard development into meaningful commits. This made the development process easier to track and provided a clear history of how the BI solution evolved.

Overall, Copilot was most useful as a development assistant, while GitHub provided a clear version-control workflow for the project.