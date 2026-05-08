# Fire Emergency Support

## Project Overview

Fire Emergency Support is a prototype emergency response platform developed for ELEC1005 Assignment 2.

The system is designed to support communication between civilians and volunteer fire brigade responders during emergency situations. The prototype was implemented using Microsoft Power Apps with SharePoint as the backend data source.

The project extends our Assignment 1 design by improving workflow integration, role separation, and real-time incident status management.

---

## Main Features

### Civilian Workflow
- Immediate emergency request submission
- Automatic location sharing
- Live incident status tracking
- Safety guidance display

### Responder Workflow
- Role-based responder access
- Incident dashboard
- Incident detail viewing
- Dispatch progress tracking
- Status updates for active incidents

---

## System Architecture

### Frontend
- Microsoft Power Apps

### Backend
- SharePoint List (`EmergencyIncidents`)

### Collaboration & Version Control
- GitHub
- Jira
- Confluence

---

## Workflow Summary

1. A civilian submits an emergency request.
2. Power Apps creates a new incident record in SharePoint.
3. Responders access the incident dashboard.
4. Responders update the incident status.
5. Civilian users receive updated incident information.

---

## Status Flow

```text
New → On the way → Done

---

# Repository Structure

## `/docs`
Project documentation, planning records, sprint summaries, and development notes.

Files:
- requirements.md
- architecture.md
- agile-workflow.md
- sprint-summary.md
- meeting-notes.md
- testing-plan.md
- user-stories.md
- final-report.pdf

Purpose:
Stores all written project documentation used throughout the Agile development process and final submission preparation.

---

## `/screenshots`
Application screenshots and implementation evidence.

Files may include:
- home-screen.png
- civilian-help-screen.png
- confirm-request-screen.png
- status-screen.png
- login-screen.png
- responder-dashboard.png
- incident-detail-screen.png
- dispatch-progress-screen.png

Purpose:
Provides visual evidence of implemented screens and workflow progression for demonstrations and reports.

---

## `/testing`
Testing records, bug tracking, and integration validation.

Files:
- test-cases.md
- usability-testing.md
- integration-testing.md
- bug-fixes.md

Purpose:
Documents testing activities, identified issues, workflow validation, and system improvements.

---

## `/powerapps-source`
Exported Power Apps files and backend integration resources.

Files:
- assignment2-app.msapp
- exported-package.zip
- sharepoint-structure.md

Purpose:
Stores the Power Apps source package and backend integration references used for deployment and collaboration.

---

## `/AI-Journal`
AI usage reflections and learning records.

Files:
- ai-reflection-week1.md
- ai-assisted-debugging.md
- prompt-improvement.md

Purpose:
Documents how AI tools were used to support development, debugging, learning, and workflow refinement during the project.

---

# Team Responsibilities

| Team Member | Role | Responsibilities |
|---|---|---|
| Khaled Albreiki | Civilian Flow Developer | Developed civilian-side workflows including emergency request, confirmation, and request status screens |
| Nasser Alhozaim | Responder Flow Developer | Developed responder-side workflows including dashboard, incident management, and dispatch functionality |
| Zhuoran Wang | GitHub and Integration Manager & Product Manager | Managed repository structure, workflow integration, SharePoint connectivity, GitHub coordination, and overall system consistency |
| Yichi Zhang | QA Tester | Conducted usability testing, workflow validation, bug identification, and integration testing |
| Jingxuan Wu | Documentation Lead | Managed project documentation, sprint summaries, meeting records, and report preparation |

---

# Development Process

The project followed an iterative Agile workflow throughout development.

Main activities included:
- Sprint planning
- Workflow refinement
- UI consistency improvements
- SharePoint integration
- Power Apps implementation
- Navigation testing
- Integration debugging
- Documentation updates

The system evolved continuously during development as the team refined requirements, improved usability, and aligned Assignment 2 implementation with updated Assignment 1 design decisions.

---

# Integration Summary

The application integrates:
- Power Apps frontend screens
- SharePoint backend data storage
- Role-based workflows
- Civilian emergency requests
- Responder incident management
- Status tracking workflows

Integration focused on:
- Maintaining workflow consistency
- Simplifying emergency interactions
- Improving usability during high-stress situations
- Supporting Agile iterative development

---

# Testing Overview

Testing activities focused on:
- Screen navigation validation
- Workflow consistency
- SharePoint connectivity
- Incident data updates
- Role-based interaction testing
- UI usability checks
- Integration reliability

Testing feedback was used to refine workflows and improve navigation clarity across both civilian and responder interfaces.

---

# Notes

This project represents an MVP prototype designed to demonstrate emergency response workflow integration using Power Apps and SharePoint.

The implementation prioritised:
- Simplicity
- Fast emergency interaction
- Clear workflow navigation
- Functional integration
- Iterative Agile improvement

The system was continuously refined throughout development based on testing feedback, workflow evaluation, and integration requirements.
