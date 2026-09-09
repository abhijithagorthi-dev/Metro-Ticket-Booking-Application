# 🚇 Metro Ticket Booking Application

## 📌 Project Overview

The **Metro Ticket Booking Application** is a ServiceNow-based digital metro ticketing solution designed to simplify the process of booking metro tickets through the **Service Portal**.

The application allows users to select their starting station and destination, choose the journey type and number of passengers, select a payment mode, calculate the applicable fare, and receive a QR-based digital ticket.

The project demonstrates how ServiceNow can be used to build a complete service-based application using **Service Catalog, Catalog Variables, Catalog UI Policies, Catalog Client Scripts, Service Portal, Flow Designer, and custom tables**.

---

## 🎯 Project Objectives

- Provide a simple digital metro ticket booking experience.
- Allow users to select metro stations from a centralized station table.
- Support single and return journeys.
- Allow users to select the number of passengers.
- Calculate and display the applicable ticket amount.
- Provide multiple payment options.
- Dynamically display payment details when required.
- Generate a QR-based digital ticket.
- Store and process ticket information using ServiceNow.
- Automate ticket processing using ServiceNow Flow Designer.

---

## ✨ Key Features

### 🚉 Metro Station Management
A custom **Metro Station Details** table is used to maintain metro station information.

Sample stations include:

- Kukatpally
- Jubilee Hills
- Panjagutta
- Ameerpet
- Uppal Stadium
- Madhapur
- LB Nagar

### 🎫 Ticket Booking

Users can provide:

- Starting station
- Destination station
- Journey type
- Number of passengers
- Payment mode
- Payment details when required

### 🔄 Journey Types

The application supports:

- Single Journey
- Return Journey

### 👥 Passenger Selection

Users can select between:

- 1 passenger
- 2 passengers
- 3 passengers
- 4 passengers

### 💳 Payment Options

The application provides:

- UPI
- Card
- Others

When **Others** is selected, an additional payment-mode field is displayed using a **Catalog UI Policy**.

### 📱 QR-Based Digital Ticket

A Service Portal widget is used to display the generated QR code.

The QR generation process uses a **Catalog Client Script** and displays the QR code through the Service Portal.

---

## 🏗️ ServiceNow Architecture

The application uses the following ServiceNow components:

| Component | Purpose |
|---|---|
| Custom Table | Stores metro station information |
| Service Catalog | Provides the metro ticket booking service |
| Catalog Variables | Collects booking information |
| Catalog UI Policy | Controls dynamic form behaviour |
| Catalog Client Script | Handles client-side ticket/QR logic |
| Service Portal | Provides the user-facing booking interface |
| Flow Designer | Automates ticket processing |
| Service Portal Widget | Displays the QR-based ticket |

---

## 🔄 Application Workflow

```text
User
  ↓
Service Portal
  ↓
Book A Metro Ticket
  ↓
Select Metro Stations
  ↓
Select Journey Type
  ↓
Select Number of Passengers
  ↓
Select Payment Mode
  ↓
Fare / Amount
  ↓
Checkout / Submit
  ↓
QR Code Generation
  ↓
Ticket Processing
  ↓
Ticket Information Stored in ServiceNow
🧩 Catalog Variables

The Book A Metro Ticket catalog item contains:

Order	Variable	Type
100	Starting From	Reference
200	Going To	Reference
300	Type of Journey	Multiple Choice
400	No of Passengers	Select Box
500	Amount for Single Journey	Single Line Text
600	Amount Including Return	Single Line Text
700	Mode of Payment	Multiple Choice
800	Enter Payment Mode	Single Line Text
🛠️ Technologies Used
ServiceNow
Service Catalog
Service Portal
Flow Designer
Catalog Variables
Catalog UI Policies
Catalog Client Scripts
ServiceNow Custom Tables
Service Portal Widgets
QR Code Integration
JavaScript
🧪 Testing

The application was tested through the ServiceNow Service Portal.

Testing covered:

Metro station selection
Journey type selection
Passenger selection
Payment mode selection
Conditional payment field
Fare/amount behaviour
QR code generation
Ticket submission
Ticket data processing
Flow execution

Detailed testing information is available in:

Documentation/Testing.md

📸 Project Screenshots

Screenshots demonstrating the ServiceNow implementation are available in the Documentation folder.

Important screenshots include:

Metro Station table
Book A Metro Ticket catalog item
Catalog variables
Payment UI Policy
Service Portal booking form
QR code
Flow Designer
📚 Documentation
Document	Description
Project Overview	Project purpose, objectives, and overview
Configuration	ServiceNow configuration details
Testing	Testing approach and test cases
Setup Guide	Steps to recreate the application
🚀 Project Status

Completed and tested as a ServiceNow Capstone Project.

The application demonstrates an end-to-end metro ticket booking workflow using ServiceNow platform capabilities.

🔮 Future Enhancements

Possible future improvements include:

Online payment gateway integration
SMS ticket notifications
Email ticket notifications
Real-time metro information
Travel and booking analytics
Advanced fare calculation based on distance
Mobile-friendly enhancements
👩‍💻 Project

Metro Ticket Booking Application

Built as a ServiceNow Capstone Project.


