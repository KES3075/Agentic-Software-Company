# Agentic Software Company: MVP

This project is an **Agentic Software Company MVP**, a prototype of an autonomous software development team powered by a hierarchy of AI agents. The system takes user requests and automatically manages the entire software development lifecycle, from initial triage and resource allocation to task execution and quality assurance.

---

## 🎯 Core System Functionality

The MVP's core is a network of specialized agents that work together to fulfill a software development request.

* **Client Agent:** Serves as the first point of contact, accepting user requests via a simple web form or chat. It performs initial triage to classify the request's complexity (e.g., simple, medium, complex) before forwarding it to the **CEO Agent**.

* **CEO Agent:** Acts as the strategic leader, prioritizing the request based on business impact (e.g., revenue potential, urgency) and assigning it to the **Product Manager Agent**.

* **Product Manager Agent:** Decomposes the requirement into smaller, manageable tasks (epics or user stories) and delegates to the **HR Agent** for resource planning.

* **HR Agent:** Analyzes the complexity of the requirements (e.g., using NLP for keywords like "OAuth" or "analytics") to recommend the optimal number of execution-level sub-agents (e.g., "2 Developers, 1 Analyst, 1 Tester"). It outputs this staffing plan in a JSON format.

* **Project Manager Agent:** Receives the staffing plan from the HR Agent and assigns tasks to the dynamically instantiated sub-agents. It manages task queues, ensures load balancing, and tracks completion to prevent bottlenecks.

* **Lead Agent:** Ensures quality by reviewing all outputs (e.g., code, test cases) for compliance with predefined standards. It flags issues and routes revisions to the relevant sub-agents, ensuring quality and iterative improvement.

---

## 🚀 How It Works: A Demo Script

1. **Stakeholder Submission:** A stakeholder submits a request: "Build a secure login page with OAuth and analytics."

2. **Triage and Prioritization:** The **Client Agent** triages the request as "medium complexity." The **CEO Agent** prioritizes it as "high" and assigns it to the **Product Manager Agent**.

3. **Task Breakdown & Staffing:** The **Product Manager Agent** decomposes the request into subtasks (UI, backend, analytics, testing) and sends the request to the **HR Agent**. The HR Agent assesses the complexity and recommends a team of **"2 Developers, 1 Analyst, 1 Tester."**

4. **Execution:** The **Project Manager Agent** assigns tasks to the instantiated sub-agents. The sub-agents (Developers, Analyst, Tester) begin their work.

5. **Quality Assurance Loop:** The **Lead Agent** reviews the outputs and finds an OAuth-related bug in the code. It routes the task for revision back to the relevant **Developer Agent**.

6. **Completion:** The developer fixes the bug, the code passes the quality checks, and the **Client Agent** notifies the stakeholder of completion.

---

## ✨ MVP Features

| Feature | MVP Implementation Example | Stakeholder Value |
|---------|----------------------------|-------------------|
| **Web/Chat Intake** | The Client Agent receives and triages requests. | Provides a simple, familiar way to submit project ideas and a quick scoping process. |
| **Task Assignment Workflow** | CEO and Product Manager Agents assign tasks; HR scales sub-agents. | Ensures transparency and allows for adaptive team sizing based on project needs. |
| **Dashboard Visualization** | Progress bars, error alerts, Gantt charts, and sub-agent utilization heatmaps. | Offers real-time oversight and confidence in resource allocation. |
| **Code Review Loop** | The Lead Agent flags issues and routes revisions to sub-agents. | Guarantees quality and facilitates continuous, iterative improvement. |
| **Dynamic Staffing** | The HR Agent recommends 1-6 sub-agents based on complexity analysis. | Enables efficient resource scaling and provides a cost simulation model. |
| **Human-in-the-Loop** | Manual overrides for HR recommendations or agent pauses. | Offers security and critical control for demonstrations and high-stakes projects. |

---
