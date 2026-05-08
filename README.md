# Fire Emergency Support

## Project Overview

Fire Emergency Support is our ELEC1005 Assignment 2 prototype, developed from our Assignment 1 design for a volunteer fire brigade emergency response platform.

In Assignment 1, our focus was mainly on understanding the problem, identifying user needs, and designing the basic civilian and responder workflows. For Assignment 2, we extended that design into a working Power Apps prototype connected to a SharePoint backend.

The main goal of the system is to make emergency help requests faster and clearer for civilians, while helping responders view and update incident information more efficiently. During development, we refined the design based on feedback and simplified the workflow so that the platform focuses on the most important emergency actions: requesting help, confirming an incident, viewing status updates, and managing responder progress.

The final prototype demonstrates a role-based emergency response workflow, with separate civilian and responder paths.

---

## Main Features

### Civilian Workflow

- Fast emergency request access
- No login required for civilians to reduce delay during emergencies
- Location sharing display
- Emergency request confirmation
- Request status tracking
- Simple safety guidance for users under stress

### Responder Workflow

- Simplified responder login to represent restricted operational access
- Incident list view
- Incident detail view
- Incident acceptance workflow
- Dispatch progress tracking
- Status updates for active incidents

---

## System Architecture

### Frontend

- Microsoft Power Apps

### Backend

- SharePoint List: EmergencyIncidents

### Collaboration and Project Management

- GitHub
- Jira
- Confluence

---

## Workflow Summary

1. The civilian opens the app and selects the civilian path.
2. The civilian sends an emergency help request.
3. The request is confirmed and stored as an incident record.
4. The responder logs in and views available incidents.
5. The responder opens the incident details and accepts the incident.
6. The incident moves into dispatch progress.
7. The incident status is updated until completion.

---

## Status Flow

New → On the way → Done

This status flow keeps the prototype simple and easy to follow. It also matches the MVP scope of the project by focusing on the core emergency response process rather than adding unnecessary status categories.

---

## Role-Based Access Design

The system uses different access paths for civilians and responders.

Civilians do not need to log in because emergency situations require fast action with as few steps as possible.

Responders use a simplified login screen to represent restricted access for authorised brigade personnel. In this prototype, the login is used to demonstrate role separation rather than a full production authentication system.

---

## Repository Structure

## /docs

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
Stores written project documentation used throughout the Agile development process and final submission preparation.

---

## /screenshots

Application screenshots and implementation evidence.

Files may include:
- home-screen.png
- civilian-help-screen.png
- confirm-request-screen.png
- request-status-screen.png
- responder-login-screen.png
- incident-list-screen.png
- incident-detail-screen.png
- dispatch-progress-screen.png
- sharepoint-list.png
- jira-board.png
- github-issues.png

Purpose:
Provides visual evidence of the implemented Power Apps screens, workflow progress, and project management activities.

---

## /testing

Testing records, bug tracking, and integration validation.

Files:
- test-cases.md
- usability-testing.md
- integration-testing.md
- bug-fixes.md

Purpose:
Documents testing activities, identified issues, workflow validation, and system improvements.

---

## /powerapps-source

Exported Power Apps files and backend integration resources.

Files:
- assignment2-app.msapp
- exported-package.zip
- sharepoint-structure.md

Purpose:
Stores the Power Apps source package and backend integration references used for backup, submission evidence, and collaboration.

---

## /AI-Journal

AI usage reflections and learning records.

Files:
- ai-reflection-week1.md
- ai-assisted-debugging.md
- prompt-improvement.md

Purpose:
Documents how AI tools were used to support learning, debugging, development decisions, and workflow refinement during the project.

---

## Team Responsibilities

| Team Member | Role | Responsibilities |
|---|---|---|
| Khaled Albreiki | Civilian Flow Developer | Developed civilian-side workflows including the emergency request, confirmation, and request status screens |
| Nasser Alhozaim | Responder Flow Developer | Developed responder-side workflows including the responder dashboard, incident management, and dispatch functionality |
| Zhuoran Wang | GitHub and Integration Manager & Product Manager | Managed repository structure, workflow integration, SharePoint connectivity, GitHub coordination, and overall system consistency |
| Yichi Zhang | QA Tester | Conducted usability testing, workflow validation, bug identification, and integration testing |
| Jingxuan Wu | Documentation Lead | Managed project documentation, sprint summaries, meeting records, and report preparation |

---

## Development Process

The project followed an iterative Agile workflow.

Main development activities included:

- Breaking the work into sprint tasks
- Assigning work based on team roles
- Building and refining Power Apps screens
- Connecting the prototype to SharePoint
- Testing navigation and workflow behaviour
- Updating documentation as the design evolved
- Recording progress through Jira and GitHub

The design changed during development as the team improved the workflow and aligned the implementation with updated requirements. This reflects the normal software engineering process where requirements, design, and implementation evolve together.

---

## Integration Summary

The application integrates:

- Power Apps frontend screens
- SharePoint backend data storage
- Role-based civilian and responder workflows
- Incident creation
- Incident status updates
- Navigation between civilian and responder interfaces

The integration work focused on making the prototype more than a static interface. The goal was to show how data could move through the system from a civilian request to responder action.

---

## Testing Overview

Testing focused on:

- Screen navigation
- Civilian request workflow
- Responder login flow
- Incident list and detail screens
- Status update consistency
- SharePoint connection
- UI clarity and usability

Testing feedback was used to improve the interface, reduce unnecessary steps, and make the workflow easier to understand.

---

## MVP Scope

This project is an MVP prototype. The focus is on demonstrating the core emergency response workflow rather than building a full production system.

The prototype prioritises:

- Fast civilian emergency requests
- Clear responder workflow
- Simple status tracking
- Role separation
- Power Apps and SharePoint integration
- Practical usability in emergency situations

Future development could include full authentication, real GPS routing, automated ETA calculation, and more advanced incident prioritisation.

