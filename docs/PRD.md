# Product Requirements Document (PRD)

## Lost & Found Platform

### 0. Document Information

| Field             | Details                             |
| ----------------- | ----------------------------------- |
| Product Name      | Lost & Found Platform               |
| Document Type     | Product Requirements Document (PRD) |
| Version           | 1.0                                 |
| Release           | MVP                                 |
| Status            | Draft                               |
| Prepared For      | CSE309 Project                      |
| Related Documents | SRS, TDD                            |

### Documents in This Set

| Document | Purpose                                                           |
| -------- | ----------------------------------------------------------------- |
| PRD      | Defines the product goals, scope, features, and user requirements |
| SRS      | Defines the functional and non-functional requirements            |
| TDD      | Describes the technical architecture and implementation design    |

---

### 1. Release Plan

| Release | Description                                                  | Deliverables                                                                                |
| ------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| MVP     | Provides the essential features of the Lost & Found Platform | User authentication, lost-item reports, found-item reports, item listings, and basic search |
| Beta    | Improves the core system with additional features            | Advanced filtering, report management, notifications, and administrative moderation         |

The MVP will focus on the essential features required to help users report and find lost belongings. Beta features may be added after the core system is implemented and tested.

### 2. Purpose

The purpose of the Lost & Found Platform is to provide a centralized web application where users can report lost items, publish information about found items, and search existing reports.

The platform aims to make it easier for people to recover their belongings by organizing lost and found information in one place.

### 3. Problem Statement

People often lose personal belongings such as student ID cards, wallets, mobile phones, keys, and bags. Finding these belongings can be difficult because information is scattered across social media groups, notice boards, and personal networks.

Similarly, people who find lost items may not know how to reach the rightful owners.

The Lost & Found Platform addresses this problem by allowing users to publish lost and found reports, browse available listings, search for relevant items, and access the contact information provided with a report.

### 4. Goals

| ID   | Goal                                                      | Release |
| ---- | --------------------------------------------------------- | ------- |
| G-01 | Allow users to register and log in securely               | MVP     |
| G-02 | Allow users to report lost items                          | MVP     |
| G-03 | Allow users to report found items                         | MVP     |
| G-04 | Allow users to browse available item reports              | MVP     |
| G-05 | Allow users to search for relevant lost and found reports | MVP     |
| G-06 | Display detailed information about reported items         | MVP     |
| G-07 | Improve search and filtering capabilities                 | Beta    |
| G-08 | Improve report management and moderation                  | Beta    |

### 5. Target Users

| User Type       | Description                                                         | Main Needs                                                          |
| --------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| Item Owner      | A person who has lost a belonging                                   | Report lost items and find matching reports                         |
| Finder          | A person who has found someone else's belongings                    | Publish found-item reports and help owners recover their belongings |
| Registered User | A person with an account on the platform                            | Access account-related features and manage their reports            |
| Administrator   | A person responsible for managing platform activity, if implemented | Review inappropriate reports and maintain platform quality          |

### 6. Scope

#### 6.1 In Scope — MVP

* User registration and login.
* Lost-item report submission.
* Found-item report submission.
* Viewing lost and found listings.
* Basic keyword search.
* Viewing item descriptions, categories, and locations.
* Viewing individual item details.
* Accessing available contact information.
* Validating required form fields.
* Providing a user-friendly web interface.

#### 6.2 Out of Scope — MVP

* Real-time GPS tracking.
* AI-based image recognition.
* Live chat between users.
* Online payments or rewards.
* Dedicated Android and iOS applications.
* Automated identity verification.
* Advanced recommendation algorithms.

#### 6.3 Planned for Beta

* Advanced search filters.
* Improved image upload and display.
* Better report management.
* Notifications about relevant updates.
* Administrative moderation tools.
* Additional usability improvements based on testing.

### 7. Features and Priorities

The MoSCoW method is used to prioritize features: Must Have, Should Have, Could Have, and Won't Have for the current release.

| ID   | Feature              | Description                                                   | Priority    | Release |
| ---- | -------------------- | ------------------------------------------------------------- | ----------- | ------- |
| F-01 | User Authentication  | Users can register and log in                                 | Must Have   | MVP     |
| F-02 | Lost-Item Reporting  | Users can submit information about lost belongings            | Must Have   | MVP     |
| F-03 | Found-Item Reporting | Users can submit information about found belongings           | Must Have   | MVP     |
| F-04 | Browse Listings      | Users can browse available reports                            | Must Have   | MVP     |
| F-05 | Search Listings      | Users can search reports using keywords                       | Must Have   | MVP     |
| F-06 | Item Details         | Users can view detailed information about an item             | Must Have   | MVP     |
| F-07 | Contact Information  | Users can view the contact method provided in a report        | Should Have | MVP     |
| F-08 | Report Management    | Users can edit or delete their own reports                    | Should Have | MVP     |
| F-09 | Advanced Filtering   | Users can filter reports by category or location              | Could Have  | Beta    |
| F-10 | Notifications        | Users receive updates about relevant activities               | Could Have  | Beta    |
| F-11 | Report Moderation    | Administrators can review inappropriate reports               | Could Have  | Beta    |
| F-12 | AI-Based Matching    | The system suggests potentially matching lost and found items | Won't Have  | Future  |

### 8. User Stories

#### 8.1 MVP User Stories

| ID    | User Story                                                                                               | Acceptance Criteria                                                            |
| ----- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| US-01 | As a user, I want to register an account so that I can access the platform                               | Valid registration information is accepted and invalid information is rejected |
| US-02 | As a registered user, I want to log in so that I can access account-related features                     | Valid credentials allow login and invalid credentials display an error         |
| US-03 | As an item owner, I want to report a lost item so that others can help me find it                        | A valid lost-item report can be submitted and displayed                        |
| US-04 | As a finder, I want to report a found item so that its owner can identify it                             | A valid found-item report can be submitted and viewed                          |
| US-05 | As a user, I want to browse item listings so that I can find relevant reports                            | Available reports are displayed with basic information                         |
| US-06 | As a user, I want to search for an item so that I can find matching reports quickly                      | Search results display reports matching the search criteria                    |
| US-07 | As a user, I want to view item details so that I can identify an item correctly                          | The details page displays the available information about the item             |
| US-08 | As a user, I want to view available contact information so that I can contact the report owner or finder | The contact method is displayed when provided                                  |

#### 8.2 Beta User Stories

| ID    | User Story                                                                                               | Acceptance Criteria                                       |
| ----- | -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| US-09 | As a user, I want to filter reports by category or location so that I can narrow my search               | Selected filters refine the displayed results             |
| US-10 | As a report owner, I want to edit or delete my report so that I can keep information up to date          | Authorized users can update or remove their own reports   |
| US-11 | As a user, I want to receive notifications so that I can stay informed about relevant updates            | Notifications are delivered for supported events          |
| US-12 | As an administrator, I want to review inappropriate reports so that the platform remains useful and safe | Authorized administrators can review and moderate reports |

### 9. Success Metrics

| ID    | Metric               | Success Criteria                                                                |
| ----- | -------------------- | ------------------------------------------------------------------------------- |
| SM-01 | Report Creation      | Users can successfully submit valid lost and found reports                      |
| SM-02 | Search Functionality | Keyword searches return relevant reports                                        |
| SM-03 | Data Validation      | Invalid or incomplete required fields are rejected with understandable messages |
| SM-04 | Usability            | Users can navigate the core features without unnecessary difficulty             |
| SM-05 | Access Control       | Restricted actions are available only to authorized users                       |
| SM-06 | Reliability          | Core features work as expected during testing                                   |

These metrics will be evaluated through functional testing, usability checks, and project demonstrations.

### 10. Assumptions and Constraints

#### 10.1 Assumptions

* Users have internet access and a modern web browser.
* Users provide accurate information when submitting reports.
* Users use the platform voluntarily to report lost or found belongings.
* The platform helps users connect but cannot guarantee item recovery.
* Users avoid publishing sensitive personal information in public reports.

#### 10.2 Constraints

* The project is developed as an individual CSE309 academic project.
* Development time and resources are limited by the academic schedule.
* The implementation must satisfy the agreed project requirements.
* Authentication, validation, and access control must be handled appropriately.
* Features planned for Beta or future releases are not guaranteed to be included in the MVP.

#### 10.3 Planned Technology Stack

| Component         | Technology                              |
| ----------------- | --------------------------------------- |
| Frontend          | React with TypeScript                   |
| Backend           | Python with FastAPI                     |
| Database          | To be finalized in the technical design |
| Version Control   | Git and GitHub                          |
| API Communication | REST API over HTTP                      |

### 11. Milestones

| Milestone | Deliverables                                            | Release  |
| --------- | ------------------------------------------------------- | -------- |
| M-01      | Finalize PRD, SRS, and TDD documentation                | Planning |
| M-02      | Set up repository structure and development environment | MVP      |
| M-03      | Implement user authentication                           | MVP      |
| M-04      | Implement lost and found report submission              | MVP      |
| M-05      | Implement listings, search, and item details            | MVP      |
| M-06      | Test core functionality and fix identified defects      | MVP      |
| M-07      | Improve filtering and report management                 | Beta     |
| M-08      | Evaluate additional features and user feedback          | Beta     |

### 12. Release Dependencies

| Dependency       | Description                                                         |
| ---------------- | ------------------------------------------------------------------- |
| Requirements     | PRD and SRS must define the expected system behavior                |
| Technical Design | TDD must describe the architecture, data model, and API approach    |
| Database         | A suitable database must be selected and configured                 |
| Authentication   | User-related features depend on a working authentication mechanism  |
| Backend API      | Frontend functionality depends on the required backend endpoints    |
| Testing          | Core workflows must be tested before the MVP is considered complete |

---

**Document Status:** This PRD describes the planned requirements for the Lost & Found Platform. Features not yet implemented should be considered planned rather than completed.
