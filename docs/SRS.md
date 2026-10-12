# Software Requirements Specification (SRS)

## Lost & Found Platform

### 0. Document Information

| Field             | Details                                   |
| ----------------- | ----------------------------------------- |
| Project Name      | Lost & Found Platform                     |
| Document Type     | Software Requirements Specification (SRS) |
| Version           | 1.0                                       |
| Status            | Draft                                     |
| Prepared For      | CSE309 Project                            |
| Related Documents | PRD, TDD                                  |

---

### 1. Introduction

#### 1.1 Purpose

The purpose of this Software Requirements Specification (SRS) is to define the functional and non-functional requirements of the Lost & Found Platform. This document describes the system's expected behavior, user interactions, constraints, and quality requirements.

#### 1.2 Scope

The Lost & Found Platform is a web-based application that allows users to report lost belongings, publish found-item information, browse reports, and search for relevant items.

The system aims to organize lost and found information in a centralized platform and help users connect with the people who may have information about their belongings.

#### 1.3 Intended Audience

This document is intended for:

* The project developer.
* Course instructors and evaluators.
* Testers responsible for verifying the system.
* Future developers who may maintain or extend the application.

#### 1.4 Definitions and Abbreviations

| Term       | Definition                                  |
| ---------- | ------------------------------------------- |
| PRD        | Product Requirements Document               |
| SRS        | Software Requirements Specification         |
| TDD        | Technical Design Document                   |
| MVP        | Minimum Viable Product                      |
| UI         | User Interface                              |
| API        | Application Programming Interface           |
| User       | A person who interacts with the platform    |
| Lost Item  | An item reported missing by its owner       |
| Found Item | An item reported as found by another person |

### 2. Overall Description

#### 2.1 Product Perspective

The Lost & Found Platform is a standalone web application consisting of a user interface, backend services, and a database. The frontend communicates with the backend through APIs to submit, retrieve, and manage item reports.

#### 2.2 Product Functions

The primary functions of the system include:

* User registration and login.
* Lost-item report creation.
* Found-item report creation.
* Viewing lost and found listings.
* Searching for items using keywords.
* Viewing detailed item information.
* Accessing contact information provided with a report.
* Managing personal reports, if included in the implemented release.

#### 2.3 User Classes

| User Class      | Description                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| Guest User      | Can browse publicly available listings and search for items                    |
| Registered User | Can access account-related features and submit reports                         |
| Item Owner      | Can report a lost item and search for information about it                     |
| Finder          | Can report an item that has been found                                         |
| Administrator   | May review and moderate reports if administrative functionality is implemented |

#### 2.4 Operating Environment

The application is intended to operate in:

* Modern web browsers such as Google Chrome, Microsoft Edge, and Mozilla Firefox.
* Desktop and laptop environments.
* Mobile browsers with a responsive user interface.
* An environment that supports the chosen frontend, backend, and database technologies.

#### 2.5 Design and Implementation Constraints

* The project is developed as an individual academic project.
* The frontend is planned to use React with TypeScript.
* The backend is planned to use Python with FastAPI.
* The database technology must be finalized in the technical design.
* The application must validate user input and protect restricted operations.
* The implementation must remain within the project timeline and available resources.

#### 2.6 Assumptions and Dependencies

* Users have access to the internet.
* Users provide accurate information about lost and found items.
* The system has a configured database for persistent storage.
* Frontend functionality depends on available backend API endpoints.
* The platform cannot guarantee that every lost item will be recovered.

### 3. Functional Requirements

#### FR-01: User Registration

**Description:** The system shall allow new users to create an account using the required registration information.

**Requirements:**

* The system shall provide a registration form.
* Required fields shall be validated.
* Invalid input shall produce an understandable error message.
* Passwords shall be stored securely using an appropriate password-hashing mechanism.

#### FR-02: User Login

**Description:** The system shall allow registered users to authenticate themselves.

**Requirements:**

* The system shall provide a login form.
* The system shall validate submitted credentials.
* Invalid credentials shall produce an error message.
* Successful authentication shall provide access to authorized functionality.

#### FR-03: Report a Lost Item

**Description:** The system shall allow users to submit a report about a lost item.

**Requirements:**

* The report shall include the required item information.
* The information may include item name, description, category, location, and date lost.
* The system shall validate required fields.
* A valid report shall be saved and made available in the listings.

#### FR-04: Report a Found Item

**Description:** The system shall allow users to submit information about a found item.

**Requirements:**

* The report shall include the required item information.
* The information may include item name, description, category, location, and date found.
* The system shall validate required fields.
* A valid report shall be saved and displayed in the found-item listings.

#### FR-05: View Item Listings

**Description:** The system shall display available lost and found reports.

**Requirements:**

* Users shall be able to browse available listings.
* Each listing shall display basic item information.
* Lost and found reports shall be distinguishable.
* The system shall display an appropriate message when no reports are available.

#### FR-06: Search Items

**Description:** The system shall allow users to search for relevant item reports.

**Requirements:**

* Users shall be able to enter keywords.
* The system shall search relevant report information.
* Matching results shall be displayed to the user.
* The system shall display a message when no matching reports are found.

#### FR-07: View Item Details

**Description:** The system shall allow users to view detailed information about an item report.

**Requirements:**

* Users shall be able to open a listing.
* The detail view shall display the available item information.
* The detail view shall identify whether the report concerns a lost or found item.

#### FR-08: View Contact Information

**Description:** The system shall provide access to the contact method included with a report.

**Requirements:**

* Contact information shall be displayed only when it has been provided and is intended to be shared.
* The system shall avoid exposing private information unnecessarily.
* Users shall be able to use the provided contact method to communicate outside or through the platform, depending on the implemented functionality.

#### FR-09: Manage Personal Reports

**Description:** If implemented in the MVP, the system shall allow registered users to manage reports they created.

**Requirements:**

* Authorized users shall be able to view their own reports.
* Users shall not be allowed to modify reports belonging to other users without authorization.
* The system shall validate changes before saving them.
* Report deletion shall require an appropriate user action.

#### FR-10: Administrative Moderation

**Description:** If administrative functionality is implemented, the system shall allow authorized administrators to review inappropriate reports.

**Requirements:**

* Administrative operations shall require appropriate authorization.
* Administrators shall be able to review available report information.
* Unauthorized users shall not be allowed to perform administrative actions.

### 4. Non-Functional Requirements

#### NFR-01: Performance

* Common pages should load within a reasonable time under normal operating conditions.
* Search results should be returned without unnecessary delay for the expected project dataset.
* Database queries should avoid unnecessary processing.

#### NFR-02: Security

* Passwords must not be stored in plain text.
* User input must be validated on the backend.
* Restricted operations must require appropriate authorization.
* Sensitive information must not be exposed unnecessarily.
* The system should use secure communication when deployed over a network.

#### NFR-03: Usability

* The interface should be understandable for first-time users.
* Forms should have clear labels and validation messages.
* Navigation should be consistent across the application.
* Users should be able to identify lost and found reports easily.

#### NFR-04: Reliability

* The system should handle invalid input without crashing.
* Errors should be reported using understandable messages.
* Valid reports should be saved correctly when the database is available.
* The system should handle unavailable data gracefully.

#### NFR-05: Maintainability

* The codebase should be organized into understandable modules.
* Frontend and backend responsibilities should be separated.
* API endpoints and data structures should be documented.
* Changes should be managed using Git and GitHub.

#### NFR-06: Compatibility

* The application should support commonly used modern browsers.
* The interface should remain usable on desktop and laptop screens.
* The layout should adapt to smaller screens where responsive design is implemented.

#### NFR-07: Data Integrity

* Required report fields must be validated before saving.
* Stored information should remain consistent with the defined data model.
* Only authorized users should be able to modify restricted information.

### 5. External Interface Requirements

#### 5.1 User Interface

The user interface should provide:

* A home page with access to lost and found listings.
* Registration and login pages.
* Forms for submitting lost and found reports.
* A search field and search results.
* An item detail view.
* Clear navigation and error messages.

#### 5.2 Software Interfaces

The planned application will use:

* React with TypeScript for the frontend.
* Python with FastAPI for the backend.
* A database selected during technical design.
* REST APIs for communication between the frontend and backend.

#### 5.3 Communication Interfaces

* The frontend and backend shall exchange data using HTTP-based API requests.
* JSON shall be used for API request and response data where appropriate.
* The deployed application should use HTTPS to protect information in transit.

### 6. Data Requirements

#### 6.1 User Data

The system may store the following user information:

* User ID.
* Name.
* Email address.
* Hashed password.
* Account creation date.

#### 6.2 Item Report Data

The system may store:

* Report ID.
* Item name.
* Item description.
* Report type: lost or found.
* Item category.
* Location.
* Date lost or found.
* Image reference, if image uploads are implemented.
* Contact information, where provided.
* Report creator's user ID.
* Report creation and update timestamps.

#### 6.3 Data Validation

* Required fields must not be empty.
* Email addresses must follow a valid format when collected.
* Date fields must contain valid dates.
* Text fields must follow defined length limits.
* Users must not be able to change records they are not authorized to manage.

### 7. Use Cases

| Use Case ID | Use Case           | Primary Actor            | Expected Result                                            |
| ----------- | ------------------ | ------------------------ | ---------------------------------------------------------- |
| UC-01       | Register Account   | Guest User               | An account is created after valid information is submitted |
| UC-02       | Log In             | Registered User          | The user is authenticated                                  |
| UC-03       | Report Lost Item   | Registered User          | A lost-item report is saved                                |
| UC-04       | Report Found Item  | Registered User          | A found-item report is saved                               |
| UC-05       | Browse Listings    | Guest or Registered User | Available reports are displayed                            |
| UC-06       | Search Items       | Guest or Registered User | Matching reports are displayed                             |
| UC-07       | View Item Details  | Guest or Registered User | Detailed report information is displayed                   |
| UC-08       | Manage Own Reports | Registered User          | The user manages their own reports, if supported           |
| UC-09       | Moderate Reports   | Administrator            | An authorized administrator reviews reports, if supported  |

### 8. Error Handling Requirements

* The system shall display validation messages for missing required information.
* The system shall display an appropriate message when login fails.
* The system shall handle unavailable or empty search results.
* The system shall inform users when a request cannot be completed.
* The system shall not expose internal error traces or sensitive technical details to ordinary users.

### 9. Acceptance Criteria

The MVP will be considered functionally acceptable when:

* Users can register and log in if authentication is included in the implemented MVP.
* Valid lost-item reports can be submitted and displayed.
* Valid found-item reports can be submitted and displayed.
* Users can browse available reports.
* Keyword search returns matching reports.
* Users can view item details.
* Required form fields are validated.
* Restricted operations are protected by appropriate authorization.
* The core workflows pass functional testing.

### 10. Future Enhancements

The following features may be considered for future releases:

* Advanced category and location filters.
* Email or in-app notifications.
* Administrative moderation.
* Improved image management.
* AI-based matching of lost and found reports.
* A dedicated mobile application.

---


