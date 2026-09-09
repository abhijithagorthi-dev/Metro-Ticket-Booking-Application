# System Configuration

## 1. Custom Metro Station Table

A custom table was created to store metro station details.

### Table Purpose

The table stores the available metro stations that can be selected while booking a metro ticket.

### Sample Station Records

- Kukatpally
- Jubilee Hills
- Panjagutta
- Ameerpet
- Uppal Stadium
- Madhapur
- LB Nagar

---

## Variable-to-Application Mapping

The Metro Ticket Booking catalog item collects passenger booking information through catalog variables.

The main mapping is:

| Catalog Variable | Purpose |
|---|---|
| Starting From | Selects the source metro station |
| Going To | Selects the destination metro station |
| Type of Journey | Selects single or return journey |
| No of Passengers | Specifies number of passengers |
| Amount for Single Journey | Stores calculated single journey amount |
| Amount Including Return | Stores return journey amount |
| Mode of Payment | Selects payment method |
| Enter Payment Mode | Captures additional payment details when Others is selected |

These variables are used by the catalog submission and automation logic to process the metro ticket request.

## 2. Catalog Item

A Service Catalog item was created for metro ticket booking.

### Catalog Item

**Book A Metro Ticket**

The catalog item provides the user-facing form through which commuters enter their journey and payment details.

---

## 3. Catalog Variables

The following variables were configured for the catalog item:

| Order | Question | Type |
|------:|----------|------|
| 100 | Starting From | Reference |
| 200 | Going To | Reference |
| 300 | Type of journey | Multiple Choice |
| 400 | No of Passengers | Select Box |
| 500 | Amount for single journey | Single Line Text |
| 600 | Amount including return | Single Line Text |
| 700 | Mode of Payment | Multiple Choice |
| 800 | Enter payment mode | Single Line Text |

---

## 4. Starting From

**Type:** Reference

The variable allows the user to select the starting metro station.

The reference is connected to the Metro Station Details table so that users can select a valid station.

---

## 5. Going To

**Type:** Reference

The variable allows the user to select the destination metro station.

The reference is connected to the appropriate metro station table/list.

---

## 6. Type of Journey

**Type:** Multiple Choice

The available choices are:

| Choice | Value |
|--------|-------|
| Single journey | 1 |
| Return journey | 2 |

The default journey type is configured as **Single journey**.

---

## 7. Number of Passengers

**Type:** Select Box

The available choices are:

| Choice | Value |
|--------|-------|
| 1 | 1 |
| 2 | 2 |
| 3 | 3 |
| 4 | 4 |

The default value is **1 passenger**.

---

## 8. Amount Fields

Two fields are provided for fare information:

- Amount for single journey
- Amount including return

These fields are used to display the applicable fare based on the selected journey details.

---

## 9. Mode of Payment

**Type:** Multiple Choice

The available payment options are:

| Payment Mode | Value |
|--------------|-------|
| UPI | UPI |
| Card | Card |
| Others | Others |

The default payment mode is **UPI**.

---

## 10. Enter Payment Mode

A separate field is provided for users who select **Others** as their payment mode.

A Catalog UI Policy is used to control this field.

### UI Policy Condition

**Mode of Payment is Others**

### UI Policy Action

**Enter Payment Mode**

- Visible: True
- Mandatory: True

Therefore, the field is displayed and required only when the user selects **Others**.

---

## 11. Service Portal

The catalog item is made available through the ServiceNow Service Portal.

Users can access the metro ticket booking form through the portal and submit their ticket requests.

---

## 12. QR Code Generation

A Service Portal widget is used to display the metro ticket QR code.

The QR implementation consists of:

- Service Portal Widget HTML
- Widget Server Script
- Catalog Client Script
- QR code generation URL

The Catalog Client Script generates the QR image URL and opens the QR widget using `spModal`.

### QR Process

```text
User clicks Checkout
        ↓
Catalog Client Script executes
        ↓
QR image URL is generated
        ↓
QR widget is opened
        ↓
QR code is displayed
---
##13. Flow Designer

Flow Designer is used to automate the ticket processing workflow.

The flow is designed to process the submitted metro ticket information and perform the required automated actions.

Screenshots of the configured flow and execution details will be added to this documentation.

---
##14. Testing

The application is tested through the Service Portal to verify:

Station selection
Journey type selection
Passenger selection
Fare information
Payment mode selection
Conditional payment field visibility
QR code generation
Ticket submission
Ticket data storage
