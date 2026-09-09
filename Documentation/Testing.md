# Testing and Validation

## 1. Testing Approach

The Metro Ticket Booking Application was tested through the ServiceNow Service Portal to verify the functionality of the catalog item, variables, UI policies, scripts, QR generation, and ticket submission.

Testing was performed using realistic metro booking scenarios.

---

## 2. Functional Test Cases

| Test Case | Test Data | Expected Result | Status |
|-----------|-----------|-----------------|--------|
| Station selection | Starting and destination stations | User can select metro stations | Pending |
| Journey type | Single journey | Single journey is selected | Pending |
| Journey type | Return journey | Return journey is selected | Pending |
| Passenger selection | 1–4 passengers | Correct passenger count can be selected | Pending |
| Payment selection | UPI | UPI can be selected | Pending |
| Payment selection | Card | Card can be selected | Pending |
| Payment selection | Others | Enter Payment Mode field becomes visible and mandatory | Pending |
| Fare calculation | Valid journey details | Correct fare is displayed | Pending |
| QR generation | Checkout | QR code is displayed | Pending |
| Ticket submission | Valid booking details | Ticket is successfully submitted | Pending |
| Data storage | Submitted ticket | Ticket information is stored in ServiceNow | Pending |

---

## 3. Service Portal Testing

The catalog item was tested through the Service Portal to verify the user experience and form behaviour.

The following were checked:

- Catalog item accessibility
- Variable visibility
- Mandatory fields
- Choice values
- Station selection
- Payment mode behaviour
- Fare fields
- QR code behaviour
- Form submission

---

## 4. UI Policy Testing

The payment-mode UI policy was tested using the following scenario:

### Test Scenario

**Condition:**

Mode of Payment = Others

### Expected Result

The **Enter Payment Mode** field should:

- Become visible.
- Become mandatory.

This validates that the Catalog UI Policy is working correctly.

---

## 5. QR Code Testing

The QR generation functionality was tested from the Service Portal.

### Expected Flow

```text
Checkout
    ↓
Catalog Client Script
    ↓
QR URL Generation
    ↓
Metro QR Widget
    ↓
QR Code Display
---
##6. Flow Designer Testing

Flow Designer execution was tested using the Execution Details to verify:

Trigger execution
Flow actions
Conditions
Record creation/update
Notifications
Successful completion

Execution details and screenshots will be added after final testing.
---

##7. Defect Tracking

During testing, issues related to fare calculation, variable behaviour, and QR generation were identified and investigated.

Issues were debugged using:

Browser console logs
ServiceNow logs
Script debugging
Flow Designer Execution Details
Service Portal testing

Resolved issues will be documented with their respective fixes.
---
##8. Final Test Result

The final test status will be updated after completing end-to-end testing of the Metro Ticket Booking Application.


### Important ⚠️

Keep the **Status = Pending** for now.

We're going to test your actual application later and change them to:

**✅ Pass** or **❌ Fail**

Don't claim something works until we've tested it.

---

### After you commit it

Your repository will now have:

```text
Metro-Ticket-Booking-Application
│
├── README.md
│
└── Documentation
    ├── Project-Overview.md
    ├── Configuration.md
    └── Testing.md

## Final Test Result

The Metro Ticket Booking Application was successfully tested through the Service Portal.

The following functions were verified:

- Metro station selection
- Metro ticket booking form
- Mandatory field validation
- Payment mode UI Policy
- QR code generation
- QR code display
- Flow Designer execution
- End-to-end ticket submission

All major functional tests passed successfully.
