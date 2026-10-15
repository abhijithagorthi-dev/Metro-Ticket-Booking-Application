# Phase 3: Project Design Phase

## 1. Introduction

This phase describes the design of the Metro Ticket Booking Application developed on the ServiceNow platform. The design covers the station data, booking form, payment-field behaviour, QR-code display and configured workflow automation.

## 2. System Architecture

The application follows this high-level design:

1. **User Interface:** Service Portal provides the interface for entering booking details.
2. **Booking Form:** The catalog item collects the source station, destination, journey type, passenger count, fare-related details and payment information.
3. **Station Data:** The Metro Station Details table stores the station records used by the booking form.
4. **Form Behaviour:** A Catalog UI Policy controls the visibility and mandatory status of the additional payment field when "Others" is selected.
5. **QR-Code Display:** The configured catalog client script and Service Portal widget work together to display a QR code.
6. **Workflow Automation:** Flow Designer supports the configured ticket-processing automation.

## 3. Main Components

| Component | Purpose |
|---|---|
| Metro Station Details table | Stores metro station information |
| Book A Metro Ticket catalog item | Collects booking details |
| Reference variables | Allow users to select stations |
| Journey type variable | Selects single or return journey |
| Passenger variable | Captures the passenger count |
| Payment UI Policy | Displays and requires additional payment details when applicable |
| QR widget | Displays the generated QR code |
| Flow Designer | Runs the configured automation |

## 4. Booking Workflow

The intended user flow is:

1. The user opens the Service Portal.
2. The user opens the Metro Ticket Booking form.
3. The user selects the source and destination stations.
4. The user chooses the journey type and number of passengers.
5. The user provides the required fare and payment information.
6. If "Others" is selected as the payment method, the additional payment field appears and becomes mandatory.
7. The user proceeds through the booking submission and QR-code display process.
8. The configured Flow Designer automation can process the relevant workflow steps.

## 5. Data Design

The Metro Station Details table stores the station records referenced by the booking form.

The catalog variables collect the remaining booking information, including journey selection, passenger count, fare-related values and payment details.

Only fields and tables actually configured in the ServiceNow instance should be described as persistent database records.

## 6. User Interface Design

The booking form is designed to group the required information into a simple sequence: station selection, journey details, fare information and payment details.

The conditional payment field reduces unnecessary input when the user chooses UPI or Card.

## 7. Design Outcome

The design provides a structured foundation for implementing, testing and maintaining the Metro Ticket Booking Application within ServiceNow.
