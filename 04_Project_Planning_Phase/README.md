# Phase 4: Project Planning Phase

## 1. Introduction

This phase describes the planned tasks, development sequence and milestones for the Metro Ticket Booking Application using ServiceNow.

## 2. Project Objectives

- Create a metro station data table.
- Configure the ticket booking catalog item and its variables.
- Implement conditional payment-field behaviour.
- Configure QR-code generation and display.
- Configure and test Flow Designer automation.
- Document the implementation and test results.

## 3. Project Development Plan

| Stage | Planned Activities | Deliverable |
|---|---|---|
| 1. Ideation | Identify the problem and define the proposed solution | Project idea and objectives |
| 2. Requirement Analysis | Identify functional and non-functional requirements | Requirement specification |
| 3. Project Design | Plan the components, data and booking workflow | System design description |
| 4. Data and Form Configuration | Create the station table and configure catalog variables | Booking form and station data |
| 5. Application Logic | Configure the payment UI Policy, QR-code display and workflow automation | Configured application features |
| 6. Testing | Test the form, validation, payment-field behaviour, QR display and workflow | Test results |
| 7. Documentation and Demonstration | Prepare project documentation, screenshots and demo video | Project submission materials |

## 4. Resources Required

- ServiceNow development instance
- Web browser and internet connection
- ServiceNow Catalog configuration
- ServiceNow Service Portal and widget configuration
- Flow Designer
- GitHub repository for version storage and documentation

## 5. Testing Plan

The application should be checked for:

- Correct station selection
- Required-field validation
- Correct visibility and mandatory behaviour of the additional payment field
- QR-code generation and display
- Expected Flow Designer execution
- End-to-end booking submission

## 6. Risks and Mitigation

| Potential Risk | Mitigation |
|---|---|
| Incorrect form configuration | Verify each variable and its settings |
| QR code does not display | Check the client script, widget and QR URL |
| Workflow does not execute | Verify the flow trigger, activation status and execution details |
| Missing booking information | Test mandatory-field validation |

## 7. Planning Outcome

This plan provides an organized sequence for developing, testing and documenting the Metro Ticket Booking Application. The deliverables are verified against the features actually implemented in the ServiceNow instance.
