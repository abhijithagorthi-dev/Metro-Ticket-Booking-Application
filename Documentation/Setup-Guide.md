# Setup Guide

## 1. Prerequisites

The following are required to recreate the Metro Ticket Booking Application:

- ServiceNow Personal Developer Instance (PDI)
- Access to ServiceNow Service Catalog
- Service Portal access
- Flow Designer access
- Basic ServiceNow administration knowledge

---

## 2. Create the Metro Station Table

1. Log in to the ServiceNow instance.
2. Navigate to **System Definition → Tables**.
3. Create a custom table named **Metro Station Details**.
4. Add a String field named **Station Name**.
5. Configure the list layout to display Station Name.
6. Create metro station records.

### Sample Stations

- Kukatpally
- Jubilee Hills
- Panjagutta
- Ameerpet
- Uppal Stadium
- Madhapur
- LB Nagar

---

## 3. Create the Catalog Item

1. Navigate to **Service Catalog → Catalog Definitions → Maintain Items**.
2. Create a new catalog item.
3. Set the name as **Book A Metro Ticket**.
4. Add the required catalog variables.

---

## 4. Configure Catalog Variables

The catalog item contains the following variables:

| Order | Variable | Type |
|---|---|---|
| 100 | Starting From | Reference |
| 200 | Going To | Reference |
| 300 | Type of Journey | Multiple Choice |
| 400 | No of Passengers | Select Box |
| 500 | Amount for Single Journey | Single Line Text |
| 600 | Amount Including Return | Single Line Text |
| 700 | Mode of Payment | Multiple Choice |
| 800 | Enter Payment Mode | Single Line Text |

### Starting From

- Type: Reference
- Reference table: Metro Station Details
- Mandatory: Yes

### Going To

- Type: Reference
- Reference table: Metro Station Details
- Mandatory: Yes

### Type of Journey

Choices:

- Single journey
- Return journey

Default value:

- Single journey

### No of Passengers

Choices:

- 1
- 2
- 3
- 4

Default value:

- 1

### Mode of Payment

Choices:

- UPI
- Card
- Others

Default value:

- UPI

---

## 5. Configure Conditional Payment Field

The **Enter Payment Mode** variable is displayed only when the user selects **Others** as the payment mode.

Create a Catalog UI Policy:

**Condition:**
Mode of Payment is Others

**UI Policy Action:**

- Enter Payment Mode → Visible
- Enter Payment Mode → Mandatory

This provides dynamic form behaviour.

---

## 6. Configure Service Portal

The catalog item should be available through the ServiceNow Service Portal.

Open the Service Portal and navigate to the catalog.

The user should be able to:

1. Open the metro booking service.
2. Select starting station.
3. Select destination station.
4. Select journey type.
5. Select number of passengers.
6. Select payment mode.
7. Enter payment details when required.
8. Submit the booking.

---

## 7. Configure QR Code Generation

A Service Portal widget is used to display the QR code.

The QR code widget receives a QR image URL through its input data.

The Catalog Client Script generates the QR image URL when the catalog item is submitted.

The overall process is:

**User submits booking → Catalog Client Script → QR URL generated → Service Portal Widget → QR Code displayed**

---

## 8. Configure Flow Designer

Flow Designer is used to automate the ticket processing after submission.

The flow can be configured to:

1. Trigger when the metro ticket request is created.
2. Process the submitted ticket information.
3. Perform the required ticket-processing actions.
4. Update the ticket status.
5. Perform required notifications or automation.

Flow Designer Execution Details can be used to verify each step and troubleshoot failures.

---

## 9. Testing the Application

After configuration, perform an end-to-end test.

Test the following:

- Station selection
- Journey type selection
- Passenger selection
- Payment mode selection
- Conditional payment field
- Fare calculation
- QR code generation
- Ticket submission
- Ticket data storage
- Flow execution

Record the final test results in:

`Documentation/Testing.md`

---

## 10. Expected User Flow

The complete application flow is:

**Service Portal**

↓

**Book A Metro Ticket**

↓

**Enter Journey Details**

↓

**Select Payment Mode**

↓

**Calculate Fare**

↓

**Checkout / Submit**

↓

**Generate QR Code**

↓

**Process Ticket**

↓

**Store Ticket Information**

---

## 11. Troubleshooting

### QR Code Not Displaying

Check:

- Catalog Client Script
- QR URL generation
- Service Portal widget
- Browser console errors

### Variable Not Appearing

Check:

- Catalog UI Policy
- UI Policy Action
- Variable name
- Variable visibility settings

### Flow Not Executing

Check:

- Flow trigger
- Flow activation status
- Flow Designer Execution Details
- Trigger conditions

---

## 12. Reproduction Result

After completing these steps, the Metro Ticket Booking Application can be recreated in a ServiceNow PDI with the configured catalog item, metro station data, dynamic form behaviour, QR code functionality, Service Portal integration, and Flow Designer automation.
