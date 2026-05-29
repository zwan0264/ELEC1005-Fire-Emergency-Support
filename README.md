# Volunteer Fire Brigade Community Safety App

This repository contains the unpacked source code for our ELEC1005 Assignment 2 Power Apps prototype.

The app is designed for a community safety volunteer organisation. It supports two main user groups:

- civilians who need to submit an emergency request quickly;
- volunteer responders who review, dispatch, support, and complete active incidents.

## Project Summary

The prototype turns our Assignment 1 design into a working Power Apps application connected to SharePoint backend lists.

The main goal of the app is to keep the emergency response flow simple:

1. a civilian submits an emergency request;
2. the incident is saved to SharePoint;
3. responders view active incidents in a queue;
4. responders accept, request support, flag false reports, or mark incidents as done;
5. the incident status is updated and reflected back in the app.

## Main Workflows

### Civilian Workflow

The civilian flow is designed for fast action under stress.

Main steps:

1. Select the **Civilian** role.
2. Tap **SEND HELP**.
3. Check current GPS location.
4. Select an incident type.
5. Confirm the request.
6. View incident status and safety guidance.

### Responder Workflow

The responder flow is designed for volunteer fire brigade members managing active incidents.

Main steps:

1. Select the **Responder** role.
2. Sign up or log in.
3. View active incidents in the responder queue.
4. Open an incident detail screen.
5. Choose one of the responder actions:
   - **Accept / Dispatch**
   - **Request Support**
   - **Flag False Report**
6. Track the incident.
7. Mark the incident as done when completed.

## App Architecture

The app uses Power Apps screens as the frontend and SharePoint lists as the backend.

### Main SharePoint Lists

#### EmergencyIncidents

This is the main operational backend list. It stores incident records submitted by civilians and updated by responders.

Important fields include:

- Incident ID
- Location
- Reporter Email
- Status
- Created Time
- Last Updated
- GPS Status
- Reports From Same Reporter
- Incident Type
- Support Requested

#### ResponderDetails

This list supports the prototype responder sign-up and login flow.

Important fields include:

- Username
- Email
- Password
- First Name
- Station Name

This is only used for the prototype login flow and should not be treated as a secure production authentication system.

## Incident Status Model

The app uses four main incident statuses.

| Status | Meaning |
|---|---|
| New | The incident has been submitted and is waiting for responder action. |
| On the Way | A responder has accepted the incident or requested support. |
| Done | The incident has been completed and removed from the active queue. |
| False Report | The incident has been judged invalid and removed from the active queue. |

The **Support Requested** field is stored separately as a Yes/No value. It is not treated as a separate incident status.

## Repository Structure

```text
Assignment-2-PowerApp/
│
├── README.md
│
├── powerapp-source/
│   └── Assignment2App-Unpacked/
│       ├── Src/
│       ├── Assets/
│       ├── DataSources/
│       ├── Connections/
│       └── CanvasManifest.json
│
├── exported-app/
│   └── Assignment2App.msapp
│
├── diagrams/
│   ├── use-case-diagram.png
│   ├── civilian-flow.png
│   ├── responder-flow.png
│   ├── architecture-backend.png
│   ├── backend-data-model.png
│   └── state-diagram.png
│
└── docs/
    └── README-assets/

## Testing Summary

The app was tested using a combination of:

- Power Apps Test Studio
- manual UI checks
- SharePoint backend evidence
- Power Apps Monitor
- accessibility review

Test Studio was useful for repeatable workflow checks, but it did not replay every control reliably. For example, some modern dropdown controls and fast screen transitions had to be supported with manual screenshots and backend checks.

These limitations and workarounds are documented in our testing documentation submitted with the Confluence export.

## Known Prototype Limitations

This is a functional prototype rather than a production emergency system.

Known limitations include:

- location is shown as GPS coordinates rather than a street address
- responder login is implemented using a prototype SharePoint list
- false report decisions are made manually by responders
- Power Apps Test Studio does not reliably replay every modern control
- the prototype does not include real emergency service integration

## How to Use This Repository

This repository is mainly for teaching staff and future maintainers who want to inspect the Power Apps source structure.

To review the implementation:

1. Open the `powerapp-source` folder.
2. Review the screen and component source files.
3. Check the data source references for the SharePoint lists.
4. Compare the implementation with the diagrams and documentation submitted in Confluence.

To run the app, use the shared Power Apps application link provided in the assignment submission.

The full testing evidence, technical documentation, user guide, and reflection are included in the submitted Confluence documentation suite.

## Team

The Bug Slayers  
ELEC1005 Assignment 2  
University of Sydney

