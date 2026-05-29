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
powerapp-source/

