# IT Support Request Manager – ServiceNow

A custom ServiceNow application developed to manage employee IT support requests.

## 📌 Project Overview

The IT Support Request Manager allows employees to submit and track IT support requests through a custom ServiceNow application.

The application captures employee information, request category, priority, description, and status. It also uses Client Scripts and Flow Designer to provide validation and automate request processing.

## 🚀 Features

- Custom Service Request table
- Auto-generated request numbers
- Employee name and email fields
- Request category selection
- Request priority management
- Request status management
- Employee email validation using Client Script
- Automatic request assignment using Flow Designer
- Request priority calculation using Flow Designer
- Default request status automation
- User-friendly ServiceNow form
- Record creation and management

## 🛠️ Technologies Used

- ServiceNow
- ServiceNow Studio
- JavaScript
- Client Scripts
- Flow Designer
- GlideRecord
- Custom Tables
- Choice Fields
- Reference Fields

## 📂 Application Structure

### Custom Table

**Service Request**

The main table stores employee IT support requests.

Important fields include:

| Field | Type |
|---|---|
| Number | String / Auto Number |
| Assigned To | Reference - User |
| Employee Name | String |
| Employee Email | String |
| Request Category | Choice |
| Priority | Choice |
| Description | String |
| Status | Choice |

## 💻 Client Script

A Client Script is used to validate the employee email address before the request is submitted.

### Validation

The script checks whether the entered employee email follows a valid email format.

If the email is invalid, the user receives an error message and the record is not submitted.

This demonstrates client-side form validation using JavaScript.

## ⚙️ Flow Designer

The application uses Flow Designer to automate request processing.

### 1. Auto Assign Service Request

**Trigger:** When a Service Request record is created.

**Action:** Automatically updates the Assigned To field with the configured user.

Purpose:

- Reduce manual assignment
- Demonstrate workflow automation
- Automatically process newly created requests

### 2. Calculate Request Priority

**Trigger:** When a Service Request record is created.

The flow is designed to process the request priority based on the request information.

Purpose:

- Automate priority handling
- Reduce manual processing
- Demonstrate Flow Designer logic

### 3. Set Default Request Status

**Trigger:** When a Service Request record is created.

The flow sets the appropriate initial status for a newly created request.

Purpose:

- Maintain consistent request status
- Automate initial record processing

## 🔄 Request Processing

The basic request lifecycle is:

```text
Employee submits request
        ↓
Client-side validation
        ↓
Service Request record created
        ↓
Flow Designer automation
        ↓
Assignment / Priority / Status processing
        ↓
Request managed by support team
