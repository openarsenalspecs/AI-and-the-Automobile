# PathAI
**Tagline:** *Compliance Made Simple.*

---

## Overview
**PathAI** is an **open-source AI-powered cloud platform** for fleet management and compliance. It automatically collects and analyzes GPS tracking data to generate **real-time compliance reports**, optimize routes, predict maintenance needs, and ensure safe and efficient fleet operations.

Built for fleet managers, drivers, and administrators, PathAI simplifies compliance with regulations while providing **actionable insights** powered by AI.

**Hosted on GitLab:** [https://gitlab.com/Roxanne_Ardary](https://gitlab.com/Roxanne_Ardary)  

---

## Key Features

### Core Features
- **GPS Tracking:** Real-time vehicle location tracking via GPS or telematics devices.  
- **Route Adherence:** Detect deviations from assigned routes.  
- **Speed Compliance:** Monitor speed limits per road or area.  
- **Hours of Service (HOS):** Track driver hours and ensure regulatory compliance.  
- **Maintenance Scheduling:** Track mileage/engine usage for preventive maintenance.  
- **Geo-Fencing:** Alerts when vehicles enter restricted or high-risk zones.

### Advanced Fleet Insights
- Driver scoring and ranking based on compliance, safety, and efficiency.  
- Fuel efficiency monitoring and optimization.  
- Carbon footprint tracking for sustainability metrics.

### Predictive & AI Analytics
- Predictive maintenance to avoid breakdowns.  
- Route optimization for faster and safer trips.  
- Risk prediction to identify trips or drivers likely to violate rules.  
- Anomaly detection for unusual behaviors like off-route driving or excessive idling.  
- AI-driven behavioral coaching for drivers.

### Automated Reporting
- Custom compliance templates per region or industry.  
- Comparative analytics to benchmark fleet performance over time.  
- Visual AI insights: heatmaps for violations, idle time, and risky areas.  
- AI-generated textual summaries highlighting trends and risks.  
- Multiple export formats: PDF, Excel, Web Dashboard.

### Integration & Extensibility
- Telematics & IoT device support (OBD-II, dash cams, sensors).  
- ERP / Payroll integration for automated reporting.  
- Open API for third-party access and automation.

### User Experience & Automation
- Mobile driver app for HOS, route guidance, and incident reporting.  
- Real-time notifications via SMS, email, and push.  
- AI chat assistant to query fleet data naturally.  
- Interactive dashboards with role-based KPIs and alerts.  
- Gamification and incentives with driver scoring and leaderboards.  
- Workflow automation for report generation, maintenance triggers, and HR notifications.  
- Contextual AI insights highlighting patterns and risks.

### Security & Privacy
- Encrypted data storage and transmission.  
- Role-based access control for drivers, managers, and admins.  
- Audit logs for report generation and edits.

### Optional Premium AI Features
- Incident reconstruction using GPS + dashcam + sensor data.  
- Fleet-wide forecasting for HOS, maintenance, and fuel needs.  
- Weather-aware routing adjustments.  

---

## Installation & Setup
PathAI can be deployed as a **cloud platform** using Docker and Kubernetes.  
- Backend: Python (FastAPI) or Node.js (Express)  
- Database: PostgreSQL + TimescaleDB for GPS and compliance data  
- Frontend: React or Vue.js dashboards  
- AI/ML: Scikit-learn, PyTorch, or TensorFlow for predictive analytics  
- LLMs (optional) for automated report summarization  

> **Note:** Examples for deployment, API usage, or automation are explained in **descriptive steps** rather than code snippets to comply with repository guidelines.

---

## Specification Branding License (SBL)

### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/pathai/](https://roxanneardary.com/pathai/)

---

## License & Notice Requirements

PathAI is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.  
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- PathAI specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a merge/pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.  

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
