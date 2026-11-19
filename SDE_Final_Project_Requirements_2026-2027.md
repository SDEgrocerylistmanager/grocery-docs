## FINAL PROJECT REQUIREMENTS

2026/2027 • Service Design and Engineering

50% of the final course grade

1–3 students per project

Required proposal validation

## 1. Project goal

The goal of the Final Project is to ideate, design, implement, and demonstrate a service-oriented application. The application domain and implementation technologies are open, but the selected problem must genuinely benefit from a service-oriented approach and satisfy the requirements in this document.

Dedicated design sessions will be offered in December. Every project idea and architecture must be validated by the teaching staff. Individual projects are possible, but teams of two or three students are strongly encouraged because services can be developed separately and then composed at a higher level.

## 2. Expected architecture

The final application must use a layered service architecture and include meaningful service composition. It must go beyond a set of unrelated CRUD endpoints: Process-Centric Services should coordinate lower-level services to fulfil complete user goals.

*Figure 1 — Reference layered architecture for the Final Project.*


## 2.1 Architecture layers

| Layer | Primary responsibility | Typical elements |
| --- | --- | --- |
| Adapter Services | Connect the application to external systems while hiding technology-specific details. | External APIs, SaaS, Web/HTML sources, IoT, external databases |
| Data Services | Provide persistence, retrieval, queries, and data aggregation for the application. | SQL/NoSQL databases, storage, data-access APIs |
| Business Logic Services | Implement reusable application-specific processing and rules. | Calculations, decisions, recommendations, notifications, transformations |
| Process-Centric Services | Compose and orchestrate multiple services to satisfy complete user requests. | Sequential/parallel calls, coordination, integrated responses |

## Service composition

A Process-Centric Service normally receives a user-level request, invokes several Business Logic, Data, or Adapter Services, and returns an integrated result. Calls may be sequential, parallel, or a combination of both.

*Figure 2 — Example of service orchestration performed by a*

*Process-Centric Service.*


## 3. General technical requirements

| Area | Minimum requirements |
| --- | --- |
| Architecture | • At least one service for each of the four logical layers (minimum four services; normally more). • Clear responsibilities; services should be reasonably reusable and scalable. • Both internally developed services and at least one external service or data source. |
| APIs | • Services must be based on REST and interact with one another only through documented APIs. • Use clearly defined JSON or XML request/response structures and provide representative examples. |
| Data | • Any suitable database technology may be used, including relational, NoSQL, embedded, or cloud- hosted solutions. |
| Deployment | • Provide a clear, reproducible procedure for starting and executing the complete application. • Local services, VMs, containers, or cloud deployment are acceptable; containerization is encouraged. |
| Repository & docs | • Maintain all code with Git from the beginning and host it on GitHub or an equivalent platform. • Document the principal APIs using OpenAPI/Swagger, a repository wiki, ReadTheDocs, or an equivalent tool. |

## 4. Expected complexity according to team size

| Team | Interface and access control | Process-Centric Services and scope |
| --- | --- | --- |
| 1 student | At least a command-line or equivalent simple interface. Basic authentication for selected endpoints when relevant. | At least 1 significant orchestration scenario invoking approximately 3–4 services sequentially and/or in parallel. |
| 2 students (recommended) | A more usable interface: simple Web UI, Postman application, bot, Slack/Telegram integration, or equivalent. Authentication where relevant. | At least 2 distinct Process-Centric Services; each should compose approximately 3–4 services. |
| 3 students | A visual Web, mobile, or desktop interface. Appropriate authentication and authorization; OAuth/OIDC or equivalent where suitable. | At least 3 distinct Process-Centric Services; each should compose approximately 3–4 services. Explicitly address user roles and resource ownership. |


## 5. Documentation and submission

Each team must submit a concise technical report of no more than three pages. It should focus on architecture and engineering decisions and include:

- Problem, intended users, and main application scenario.

- Architecture diagram showing the services and the four logical layers.

- Description of the main Process-Centric Services and orchestration scenarios.

- External services and data sources and their role in the application.

- Principal technologies, deployment approach, and execution instructions.

- Links to repositories and API documentation.

Submission: use the dedicated Moodle assignment and provide access to the source-code repositories, report, API documentation, and all information required to reproduce and run the application.

## 6. Evaluation and final demonstration

| Dimension | What will be assessed |
| --- | --- |
| Architecture | Correct application of the service-oriented approach; quality of decomposition, layering, APIs, and service composition. |
| Execution | Reliable demonstration; reproducible deployment; code quality and organization; API/project documentation; appropriate use of Git. |
| Complexity | A feasible but sufficiently challenging problem for the team size, with meaningful orchestration rather than unnecessary technologies. |

## Final presentation and demo

During the selected exam session, the team will present the problem, architecture, principal services, and orchestration scenarios, followed by a live demonstration. The teaching staff may ask questions about any component or design decision.

- All team members must understand the overall architecture and the main service interactions.

- Project grading is individual for individual projects and at group level for team projects.

- A smaller, coherent, and well-documented system is preferable to a larger application with weak architectural justification.

## Pre-submission checklist

| Four layers represented External service/data source used REST APIs documented |
| --- |
| Deployment reproducible Report within 3 pages Repositories accessible |
