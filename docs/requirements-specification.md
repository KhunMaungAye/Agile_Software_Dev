# Smart Campus Lost & Found Website — System Requirements

## 1. System Overview

The **Smart Campus Lost & Found Website** is a web-based system designed to help students and university staff report, search for, and manage lost and found items on campus.

The system provides one central location where users can report missing belongings, register items they have found, and search existing reports. The goal is to reduce the difficulty of finding lost property and replace informal methods such as asking classmates or posting repeatedly on social media.

The system will be developed as an MVP for an Agile Software Development course project.

---

## 2. Project Objectives

The main objectives of the system are to:

- Provide an easy way to report lost belongings.
- Provide an easy way to report found belongings.
- Allow students to search for previously reported items.
- Help users identify items using descriptions, categories, locations, and photos.
- Allow users to update an item when it has been returned.
- Provide a simple and responsive interface for desktop and mobile users.
- Keep user and contact information reasonably protected.
- Organize lost-and-found information in a structured database.

---

## 3. Target Users

| User             | Main Purpose                                                    |
| ---------------- | --------------------------------------------------------------- |
| Student          | Report lost or found items and search existing reports.         |
| University Staff | Report found property and assist with item management.          |
| Reporter         | Person who creates a lost or found item report.                 |
| Administrator    | Reviews reports and manages inappropriate or completed reports. |
| Product Owner    | Prioritizes requirements and accepts completed features.        |
| Development Team | Designs, develops, tests, and demonstrates the website.         |

The initial MVP does not require students to create detailed user profiles.

---

## 4. Core User Needs

The system is designed around the following user needs:

### Need 1 — Report a Lost Item

A student who loses an item should be able to create a report containing information such as the item name, category, location, date, description, and contact information.

### Need 2 — Report a Found Item

A student or staff member who finds an item should be able to register it on the website so that the owner can search for it.

### Need 3 — Find an Existing Report

Users should be able to search reported items using keywords and filters.

### Need 4 — Identify an Item

Users should be able to view detailed information and an optional photo to determine whether a reported item may belong to them.

### Need 5 — Complete a Case

When an item has been successfully returned, the report should be marked as **Returned/Resolved**.

---

## 5. Functional Requirements

### 5.1 Website Navigation

| ID    | Requirement                                                                                                   |
| ----- | ------------------------------------------------------------------------------------------------------------- |
| FR-01 | The website shall provide access to the Home page, Lost Items, Found Items, Search, and Report Item features. |
| FR-02 | Each major feature shall have a clear title and short explanation.                                            |
| FR-03 | Navigation shall remain usable on both desktop and mobile-sized screens.                                      |
| FR-04 | The system shall display appropriate success and error messages after user actions.                           |

### 5.2 Lost Item Reporting

| ID    | Requirement                                                         |
| ----- | ------------------------------------------------------------------- |
| FR-05 | Users shall be able to create a lost-item report.                   |
| FR-06 | A lost-item report shall require an item name or description.       |
| FR-07 | Users shall select an appropriate item category.                    |
| FR-08 | Users shall enter the campus location where the item was lost.      |
| FR-09 | Users shall enter the date the item was lost.                       |
| FR-10 | Users shall be able to provide additional details about the item.   |
| FR-11 | Users shall provide contact information for communication.          |
| FR-12 | Users shall optionally attach a photo of the item.                  |
| FR-13 | The system shall generate a unique report ID.                       |
| FR-14 | A successfully submitted report shall appear in the lost-item list. |

### 5.3 Found Item Reporting

| ID    | Requirement                                                              |
| ----- | ------------------------------------------------------------------------ |
| FR-15 | Users shall be able to create a found-item report.                       |
| FR-16 | A found-item report shall require an item name or description.           |
| FR-17 | Users shall select an item category.                                     |
| FR-18 | Users shall enter where the item was found.                              |
| FR-19 | Users shall enter the date the item was found.                           |
| FR-20 | Users shall provide additional information when necessary.               |
| FR-21 | Users shall provide contact information.                                 |
| FR-22 | Users shall optionally upload an item photograph.                        |
| FR-23 | The system shall generate a unique report ID for each found-item report. |

### 5.4 Item Search

| ID    | Requirement                                                              |
| ----- | ------------------------------------------------------------------------ |
| FR-24 | The system shall display available lost and found reports.               |
| FR-25 | Users shall be able to search using an item name or keyword.             |
| FR-26 | Users shall be able to filter results by category.                       |
| FR-27 | Users shall be able to filter results by campus location.                |
| FR-28 | Users shall be able to choose between Lost and Found reports.            |
| FR-29 | The search shall not require exact capitalization.                       |
| FR-30 | The system shall display a clear message when no matching report exists. |

### 5.5 Item Information

| ID    | Requirement                                                                        |
| ----- | ---------------------------------------------------------------------------------- |
| FR-31 | Users shall be able to open a detailed view of a report.                           |
| FR-32 | The details page shall display the item name.                                      |
| FR-33 | The details page shall display the item description.                               |
| FR-34 | The details page shall display the category and location.                          |
| FR-35 | The details page shall display the reported date.                                  |
| FR-36 | The details page shall display the item photograph when available.                 |
| FR-37 | The details page shall display whether the report is currently active or resolved. |
| FR-38 | Users shall have a method of contacting the reporter.                              |

### 5.6 Report Status

| ID    | Requirement                                                                            |
| ----- | -------------------------------------------------------------------------------------- |
| FR-39 | Every report shall have a status.                                                      |
| FR-40 | A report shall initially be marked as Lost or Found.                                   |
| FR-41 | The reporter shall be able to mark a successfully recovered item as Returned/Resolved. |
| FR-42 | Resolved reports shall be visually identified.                                         |
| FR-43 | Resolved reports shall not appear in the default active-results view.                  |
| FR-44 | The system shall record when a report becomes resolved.                                |

### 5.7 Administration

| ID    | Requirement                                                          |
| ----- | -------------------------------------------------------------------- |
| FR-45 | Authorized administrators shall be able to review submitted reports. |
| FR-46 | Administrators shall be able to remove inappropriate reports.        |
| FR-47 | Administrators shall be able to update report status when necessary. |
| FR-48 | Normal users shall not have access to administrator functions.       |

---

## 6. User Interface Requirements

| ID    | Requirement                                                                                  |
| ----- | -------------------------------------------------------------------------------------------- |
| UI-01 | The website shall use clear and simple English.                                              |
| UI-02 | Lost and Found reports shall be visually distinguishable.                                    |
| UI-03 | Forms shall clearly indicate required fields.                                                |
| UI-04 | Validation messages shall explain what the user needs to correct.                            |
| UI-05 | Search and filtering controls shall be easy to find.                                         |
| UI-06 | Item cards shall show the most important information before the user opens the details page. |
| UI-07 | The interface shall remain usable on screens from approximately 360 px wide and above.       |
| UI-08 | Buttons and form controls shall have clear labels.                                           |

---

## 7. Data Requirements

The system shall store information related to each lost or found report.

### Report Data

Each report may contain:

- Report ID
- Item name
- Description
- Report type
- Category
- Campus location
- Lost/found date
- Photo
- Contact information
- Report status
- Created date
- Updated date
- Resolved date

### Suggested Categories

- Electronics
- Bags
- Keys
- Wallets
- Student Cards / IDs
- Books
- Stationery
- Clothing
- Accessories
- Other

### Suggested Campus Locations

- Library
- Cafeteria
- Classroom
- Computer Laboratory
- Dormitory
- Sports Area
- Parking Area
- Student Center
- Other

The database shall use UTF-8-compatible storage so that English and Thai text can be stored correctly.

---

## 8. Security and Privacy Requirements

| ID     | Requirement                                                                                |
| ------ | ------------------------------------------------------------------------------------------ |
| SEC-01 | The system shall not store passwords or API keys directly in public source code.           |
| SEC-02 | Users shall be warned not to include sensitive personal information in item descriptions.  |
| SEC-03 | The system shall collect only contact information needed for lost-and-found communication. |
| SEC-04 | Administrative functions shall be restricted to authorized users.                          |
| SEC-05 | Uploaded images shall be checked for supported file types before being stored.             |
| SEC-06 | The system shall not intentionally expose unnecessary private information to other users.  |

Users should not enter passport numbers, passwords, banking information, or other highly sensitive information into item descriptions.

---

## 9. Performance and Reliability

| ID     | Requirement                                                                                     |
| ------ | ----------------------------------------------------------------------------------------------- |
| NFR-01 | Normal item searches should return results within approximately two seconds.                    |
| NFR-02 | The website should remain usable when no search results are available.                          |
| NFR-03 | A failed database or server operation shall display a meaningful error message.                 |
| NFR-04 | A temporary failure shall not cause previously stored reports to disappear.                     |
| NFR-05 | Images should be optimized so that item pages load within a reasonable time.                    |
| NFR-06 | The website shall support current versions of Chrome, Edge, Firefox, and Safari during testing. |

---

## 10. Business Rules

- BR-01: Every submitted report must have a unique report ID.
- BR-02: A report must contain sufficient information to identify the item.
- BR-03: Users are responsible for providing truthful information.
- BR-04: A report may be changed to Returned/Resolved after the item has been recovered.
- BR-05: Resolved reports should not appear in the default active search.
- BR-06: Users must not upload offensive, illegal, or unrelated images.
- BR-07: Users should not publish sensitive personal information.
- BR-08: Administrators may remove false, inappropriate, or invalid reports.
- BR-09: The website does not guarantee that a lost item will be recovered.
- BR-10: Users should verify ownership before giving an item to another person.
- BR-11: Valuable items may be transferred through an appropriate university office or security department.

---

## 11. System Limitations

The first version of the system will focus only on basic lost-and-found functionality.

The MVP will **not** include:

- AI-based image recognition.
- Automatic item matching.
- GPS tracking.
- Live campus maps.
- Online payments or rewards.
- Delivery services.
- Native Android or iOS applications.
- Social media integration.
- Facial recognition.
- Automatic identity verification.
- University ID-card system integration.
- Advanced push notifications.

These features can be considered as future improvements after the MVP is evaluated.

---

## 12. MVP Acceptance Requirements

The website will be considered ready for demonstration when:

1. A user can successfully submit a lost-item report.
2. A user can successfully submit a found-item report.
3. Required fields are validated before submission.
4. Users can search for reported items.
5. Users can filter results by category and location.
6. Users can open and view item details.
7. Optional item photos can be displayed correctly.
8. Users can identify whether an item is active or resolved.
9. A report can be marked as Returned/Resolved.
10. The website works on desktop and mobile-sized screens.
11. Appropriate error messages are displayed when operations fail.
12. Administrative functions cannot be accessed by normal users.
13. No critical defects remain before the final demonstration.

---

## 13. Requirement Traceability

| User Need                     | Related Requirements | Acceptance Area |
| ----------------------------- | -------------------- | --------------- |
| Report a lost item            | FR-05–FR-14          | AC-01–AC-03     |
| Report a found item           | FR-15–FR-23          | AC-04–AC-06     |
| Search for items              | FR-24–FR-30          | AC-07–AC-09     |
| View item information         | FR-31–FR-38          | AC-10–AC-11     |
| Update item status            | FR-39–FR-44          | AC-12–AC-13     |
| Manage reports                | FR-45–FR-48          | AC-14           |
| Use website on mobile         | UI-01–UI-08          | AC-15           |
| Protect user information      | SEC-01–SEC-06        | AC-16           |
| Maintain reliable performance | NFR-01–NFR-06        | AC-17           |

---

## 14. Final MVP Statement

The **Smart Campus Lost & Found Website** will provide a centralized and easy-to-use platform for reporting and finding lost property on campus.

The MVP will concentrate on the essential user journey:

**Report → Search → View Details → Contact → Return/Resolve**

Additional advanced functions will be considered only after the core MVP has been completed and evaluated through the Agile development process.
