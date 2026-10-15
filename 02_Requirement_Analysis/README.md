# Phase 2: Requirement Analysis

## 1. Introduction

The Metro Ticket Booking Application is developed using ServiceNow to provide a digital interface for collecting metro journey and ticket booking details.

## 2. Functional Requirements

The application should:
- Allow users to select a starting metro station.
- Allow users to select a destination station.
- Provide single and return journey options.
- Allow users to select the number of passengers.
- Capture fare-related fields and payment details.
- Display an additional payment field when the user selects "Others".
- Generate and display a QR code through the booking interface.
- Support the configured Flow Designer automation.
- Allow users to submit the booking form through the Service Portal.

## 3. Non-Functional Requirements

- **Usability:** The booking form should be easy to understand.
- **Reliability:** The form should validate required information.
- **Maintainability:** Configuration should be manageable within ServiceNow.
- **Performance:** The booking interface should respond within reasonable time.
- **Security:** Access should follow the permissions configured in ServiceNow.

## 4. Software Requirements

- ServiceNow development instance
- Web browser
- ServiceNow Service Portal
- ServiceNow Catalog configuration
- ServiceNow Flow Designer
- GitHub for project documentation and version storage

## 5. Hardware Requirements

- Computer or laptop
- Internet connection
- Supported web browser

## 6. Project Scope

The project demonstrates metro station selection, booking-form configuration, payment-field behaviour, QR-code display and configured workflow automation.

Integration with a real payment gateway, live metro operations, and actual gate-based QR validation are outside the implemented prototype unless separately configured.

## 7. Expected Outcome

A working ServiceNow prototype that demonstrates the main metro ticket booking flow and provides documentation for setup, configuration and testing.
