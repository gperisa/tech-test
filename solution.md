# Solution.md

Hours Tracking App

My idea is to separate development in 2 phases. In the first phase we'll create a "proof of concept" that would connect to JIRA and HR Payroll APIs, retrieve the data and generate reports based on date/time input parameters. 

In the second phase components StoryManager and ReportGenerator wouldn't connect to JIRA and HR Payroll APIs anymore but to a local database that we created just for reporting purposes (explained in salability part). To minimize code changes new DAL component is introduced and it implements JIRAConnector and HRConnector interfaces but instead of calling APIs it calls the database. Component for scheduled data retrieval is created and it does it's job during the night by connecting to external systems, querying them and filling local database.

Diagrams:

1. Activity Diagram -  https://github.com/gperisa/tech-test/blob/master/Travix%20-%20Activity%20Diagram.jpg
2. Phase 1 - Component Diagram - https://github.com/gperisa/tech-test/blob/master/Travix%20Phase%201%20-%20Component%20Diagram.jpeg
3. Phase 2 - Component Diagram - https://github.com/gperisa/tech-test/blob/master/Travix%20Phase%202%20-%20Component%20Diagram.jpeg
4. SSO functionality Activity Diagram - https://github.com/gperisa/tech-test/blob/master/Travix%20-%20SSO%20Diagram.jpg
5. ER Diagram - https://github.com/gperisa/tech-test/blob/master/Travix%20-%20Database%20ER%20Diagram.jpeg
