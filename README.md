
# Smart Portfolio Manager

Smart Portfolio Manager is an end-to-end portfolio management system built with OutSystems ODC, extended with external APIs, automation workflows, and AI-assisted analysis.

This project goes beyond UI development and demonstrates full solution architecture, integrating multiple systems, automating analysis pipelines, and combining low-code development with traditional engineering practices.

---

## Overview

The application centralizes project and task management, supporting both internal (OutSystems) and external (NodeJS) project sources.

It integrates multiple systems to provide automated project insights, including summaries, risks, and recommendations, powered by both rule-based analysis and AI.

---

## Key Features

- Portfolio dashboard for monitoring projects and tasks  
- Support for both local and external project sources  
- Integration with external AWS MySQL database  
- Custom NodeJS + Express API for external project data  
- Automated analysis pipeline triggered from the application  
- Callback flow to update results in real-time  
- AI-assisted agent capable of generating project insights (summary, risk, recommendations)  
- Multi-source insight generation (local vs external projects)  

---

## 🧠 AI Agent (OutSystems + Claude)

A custom agent was developed within OutSystems to generate project insights using Claude.

### Capabilities

- Generates:
  - Project summary  
  - Risk assessment  
  - Recommendations  
- Differentiates between:
  - Local projects (OutSystems)
  - External projects (NodeJS API)
- Fetches and processes relevant data dynamically before generating insights  

### Integration

- Connected via REST APIs exposed by OutSystems  
- Uses prompt-based generation to create contextual and dynamic responses  
- Fully integrated into the application workflow  

---

## Technologies Used

### Core Stack

- OutSystems Developer Cloud  
- NodeJS + Express  
- AWS MySQL  

### Automation & Processing

- GitHub Actions (YAML workflows)  
- Python (analysis logic)  
- Bash  
- jq (data transformation)

### Development & Validation

- Postman (API testing and validation)  
- MySQL Workbench (database inspection and manipulation)  
- VS Code  

### Deployment

- Render (NodeJS API hosting)  

---

## System Architecture

This solution follows an end-to-end distributed architecture integrating multiple systems and services.

### Flow Overview

OutSystems App
→ Triggers analysis request
→ GitHub Actions workflow (multi-job pipeline)
→ Python / Bash analysis logic
→ Callback API
→ OutSystems updates execution results

---

### External Integrations

- AWS MySQL (external database)  
- NodeJS + Express API (external project source)  
- GitHub Actions (automation pipeline)  
- Render (API deployment)  

---

### Data Flow

- Local projects fetched via OutSystems REST APIs  
- External projects fetched via NodeJS API  
- Data normalized into a unified structure before processing  

---

## Data Normalization

The system supports multiple project sources:

- Local OutSystems data  
- External NodeJS API data  

A normalization layer ensures consistent processing by converting different data formats into a unified structure.

This allows the analysis pipeline to remain independent from the data source.

---

## Automation Pipeline

A GitHub Actions workflow orchestrates the automated analysis process.

### Pipeline Jobs

- `setup` → prepares environment  
- `fetch_data` → retrieves project data (NodeJS or OutSystems)  
- `analyze` → calculates metrics and generates insights  
- `callback` → sends results back to OutSystems  

---

### Key Concepts

- Multi-job orchestration  
- Cross-platform data integration  
- JSON transformation using Bash + jq  
- Python-based analysis logic  
- Callback-driven result handling  

---

## Asynchronous Processing

The analysis pipeline runs outside the application lifecycle.

### Flow

1. User triggers analysis in the app  
2. GitHub Actions workflow is executed  
3. Processing happens asynchronously  
4. Results are returned via callback API  
5. UI updates with execution results

---

## Analysis Logic

Two types of analysis are implemented:

### Rule-Based Analysis (GitHub Actions + Python)

- Processes project data  
- Calculates:
  - Total tasks  
  - Completed tasks  
  - Overdue tasks  
  - Progress percentage  
- Generates:
  - Summary  
  - Risk report  

---

### AI-Based Analysis (OutSystems Agent + Claude)

- Generates contextual insights  
- Produces:
  - Summary  
  - Risk assessment  
  - Recommendations  
- Adapts output based on project source and data  

---

## Testing & Validation

- REST APIs tested using Postman (GET and POST)  
- Payload validation across integrations  
- Workflow logs used to trace execution and debug issues  
- Database inspection performed through MySQL Workbench  

---

## Observability & Debugging

- Structured logs in GitHub Actions  
- API response inspection across systems  
- Error handling for callback failures  
- Debugging JSON payload issues using jq  

---

## What This Project Demonstrates

- End-to-end system architecture  
- Integration between low-code and traditional development  
- REST API consumption and exposure  
- External database integration  
- Multi-source data handling  
- Automation pipeline orchestration  
- Asynchronous processing patterns  
- AI-assisted application behavior  
- Cross-platform engineering mindset  

---

## Key Takeaway

This project demonstrates how low-code development can be extended with external systems, automation pipelines, and AI-driven insights to build scalable, intelligent, and production-like solutions.

## Screenshots

### Portfolio Dashboard
<img width="1904" height="909" alt="image" src="https://github.com/user-attachments/assets/8b24ddac-386c-40be-80c4-20a87f13ddb6" />

### Project Information 
<img width="1902" height="911" alt="image" src="https://github.com/user-attachments/assets/e8bc9276-0ddd-474c-86b5-422df3ffb85c" />

### Postman
<img width="1393" height="705" alt="image" src="https://github.com/user-attachments/assets/f162b45f-8d6f-4ed3-9f37-0fde2bb630a2" />

### GitHub Jobs
<img width="1606" height="641" alt="image" src="https://github.com/user-attachments/assets/6dfbf0d4-fad3-49fc-935b-a67d8b76fc0d" />

### External AWS DB Connection and Integration
<img width="1303" height="854" alt="image" src="https://github.com/user-attachments/assets/322fd95e-c41e-4569-9046-e16d1c9cd25d" />

### ODC Agent SmartPortfolioManager
<img width="1420" height="690" alt="image" src="https://github.com/user-attachments/assets/24b8782c-0c8f-4896-9dbc-1004c0069924" />

### NodeJS + Express API Project List
<img width="1293" height="966" alt="image" src="https://github.com/user-attachments/assets/608ed4e6-c979-450a-8a71-e7a299e33864" />

### API Deployment Render
<img width="1582" height="808" alt="image" src="https://github.com/user-attachments/assets/5bd84c4b-ef96-47f7-b638-5346160bd907" />

### Python + YAML + jq Configuration
<img width="1683" height="961" alt="image" src="https://github.com/user-attachments/assets/88147fe5-e83f-46dc-8cdb-d283f4022500" />


















