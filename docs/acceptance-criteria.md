# Acceptance Criteria

## 1. Purpose

This document defines the conditions that the **Smart Campus Lost & Found Website** must satisfy before it can be accepted as an MVP.

The criteria are derived from the project's **Project Charter, Requirements Specification, and Database Design**. They provide a practical checklist for the development team to verify each feature after implementation.

Because the application is still under development, all criteria are initially marked **Not Tested**. The results can be updated as features are completed.

---

## 2. Feature Acceptance Checklist

| ID        | Feature              | Requirement to Satisfy                                                         | Expected Result                                                                                | Status     |
| --------- | -------------------- | ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- | ---------- |
| **AC-01** | Lost Item Report     | Users must be able to report an item they have lost                            | A Lost Item report can be submitted and saved successfully                                     | Not Tested |
| **AC-02** | Found Item Report    | Users must be able to report an item they have found                           | A Found Item report can be submitted and saved successfully                                    | Not Tested |
| **AC-03** | Item Information     | Reports must contain the necessary item information                            | Item name, description, date, category, and location can be entered and saved                  | Not Tested |
| **AC-04** | Category             | Each report must have an item category                                         | The selected category is correctly associated with the report                                  | Not Tested |
| **AC-05** | Campus Location      | Each report must identify where the item was lost or found                     | The selected campus location is correctly stored                                               | Not Tested |
| **AC-06** | Report Type          | The system must distinguish Lost and Found reports                             | Each report is correctly identified as `LOST` or `FOUND`                                       | Not Tested |
| **AC-07** | Photo Upload         | Users should be able to add an optional item photo                             | A supported image can be uploaded and displayed with the report                                | Not Tested |
| **AC-08** | Image Validation     | Unsupported image files must not be accepted                                   | An invalid file is rejected with a clear message                                               | Not Tested |
| **AC-09** | Required Fields      | Required information must be completed before submission                       | The website prevents incomplete reports from being submitted                                   | Not Tested |
| **AC-10** | Unique Report ID     | Every report must have a unique identifier                                     | Each saved report receives a unique ID                                                         | Not Tested |
| **AC-11** | Initial Status       | New reports must have an active status                                         | A newly created report is stored with `OPEN` status                                            | Not Tested |
| **AC-12** | Report Listing       | Users must be able to browse reported items                                    | Available Lost and Found reports are displayed in an organized list                            | Not Tested |
| **AC-13** | Keyword Search       | Users must be able to search for items                                         | Relevant reports are returned when a keyword is entered                                        | Not Tested |
| **AC-14** | Category Filtering   | Users must be able to narrow results by category                               | Only reports matching the selected category are displayed                                      | Not Tested |
| **AC-15** | Location Filtering   | Users must be able to narrow results by campus location                        | Only reports matching the selected location are displayed                                      | Not Tested |
| **AC-16** | Lost/Found Filtering | Users must be able to separate Lost and Found reports                          | The selected report type is displayed correctly                                                | Not Tested |
| **AC-17** | Combined Filtering   | Users should be able to use multiple filters                                   | Search results satisfy all selected filter conditions                                          | Not Tested |
| **AC-18** | Empty Results        | The system must handle searches with no matches                                | A clear "No items found" message is displayed                                                  | Not Tested |
| **AC-19** | Item Details         | Users must be able to inspect a report                                         | Complete item information is displayed on the details page                                     | Not Tested |
| **AC-20** | Report Status        | Users must be able to see the current state of an item                         | The report displays its current status clearly                                                 | Not Tested |
| **AC-21** | Resolve Report       | Completed cases must be identifiable                                           | An authorized user can change an active report to `RESOLVED`                                   | Not Tested |
| **AC-22** | Resolution Date      | The database should record when a case is completed                            | The resolution date is stored when an item is resolved                                         | Not Tested |
| **AC-23** | Active Reports       | Resolved reports should not appear as active                                   | Active searches exclude resolved reports                                                       | Not Tested |
| **AC-24** | Edit Report          | Existing report information should be editable by an authorized user           | Updated information is saved and displayed correctly                                           | Not Tested |
| **AC-25** | Remove Report        | Unnecessary or inappropriate reports should be removable by an authorized user | The selected report no longer appears in normal results                                        | Not Tested |
| **AC-26** | Navigation           | Users need simple access to the main functions                                 | Home, Lost Items, Found Items, Report Item, and Search are accessible                          | Not Tested |
| **AC-27** | Error Handling       | System errors must be understandable to users                                  | An appropriate error message is shown without crashing the website                             | Not Tested |
| **AC-28** | Data Validation      | Invalid information must not enter the database                                | Invalid or incomplete data is rejected before storage                                          | Not Tested |
| **AC-29** | Responsive Layout    | Students may access the website from different devices                         | The main functions work without horizontal scrolling on mobile-sized screens                   | Not Tested |
| **AC-30** | Security and Privacy | User and project data must be protected                                        | No passwords, database credentials, API keys, or unnecessary sensitive information are exposed | Not Tested |

---

## 3. Database Verification Criteria

The following criteria are used to confirm that the website correctly follows the database design.

| ID        | Database Area     | Verification Requirement                      | Expected Result                                                | Status     |
| --------- | ----------------- | --------------------------------------------- | -------------------------------------------------------------- | ---------- |
| **DB-01** | Users             | Reports must be connected to their reporter   | Each item contains the correct `user_id` reference             | Not Tested |
| **DB-02** | Categories        | Items must use valid categories               | Each item contains a valid `category_id`                       | Not Tested |
| **DB-03** | Locations         | Items must use valid campus locations         | Each item contains a valid `location_id`                       | Not Tested |
| **DB-04** | Items             | Item information must be stored correctly     | Name, description, type, date, and status are stored correctly | Not Tested |
| **DB-05** | Item Type         | Only supported report types should be stored  | `item_type` contains `LOST` or `FOUND`                         | Not Tested |
| **DB-06** | Item Status       | Only supported statuses should be stored      | Status follows the defined database rules                      | Not Tested |
| **DB-07** | Unique Identifier | Every item needs a unique database identifier | Each item receives a unique `item_id`                          | Not Tested |
| **DB-08** | Required Values   | Required database fields cannot be empty      | Invalid records are rejected                                   | Not Tested |
| **DB-09** | Timestamps        | Changes to reports should be trackable        | `created_at` and `updated_at` contain appropriate timestamps   | Not Tested |
| **DB-10** | Relationships     | Foreign-key relationships must remain valid   | Items reference existing users, categories, and locations      | Not Tested |

---

## 4. Quality Acceptance Criteria

| ID        | Quality Area    | Acceptance Requirement                                                                | Status     |
| --------- | --------------- | ------------------------------------------------------------------------------------- | ---------- |
| **QA-01** | Usability       | A first-time student can understand how to report and search for an item              | Not Tested |
| **QA-02** | Interface       | Buttons, forms, labels, and messages are clear and consistent                         | Not Tested |
| **QA-03** | Mobile          | Core features remain usable on mobile-sized screens                                   | Not Tested |
| **QA-04** | Accessibility   | Forms and interactive elements are usable with keyboard navigation                    | Not Tested |
| **QA-05** | Performance     | Normal searches and filters provide results within the project's target response time | Not Tested |
| **QA-06** | Reliability     | A failed operation does not crash the application                                     | Not Tested |
| **QA-07** | Browser Support | The website works in supported modern browsers                                        | Not Tested |
| **QA-08** | Security        | Secrets and credentials are excluded from the GitHub repository                       | Not Tested |
| **QA-09** | Privacy         | The system does not unnecessarily collect sensitive personal information              | Not Tested |
| **QA-10** | Maintainability | Project code and database components are organized clearly for future changes         | Not Tested |

---

## 5. Traceability

The acceptance criteria are connected to the project's other documents.

| Source Document                | What Is Verified                                                                            |
| ------------------------------ | ------------------------------------------------------------------------------------------- |
| **Project Charter**            | Project vision, MVP scope, users, goals, risks, and delivery approach                       |
| **Requirements Specification** | Functional and non-functional system requirements                                           |
| **Database Design**            | Tables, fields, relationships, constraints, and data integrity                              |
| **Acceptance Criteria**        | Practical conditions used to determine whether the planned requirements have been satisfied |

### Document Relationship

```text
Project Charter
      ↓
Requirements Specification
      ↓
Database Design
      ↓
Acceptance Criteria
      ↓
Testing Evidence
      ↓
MVP Review
```

---

## 6. MVP Completion Checklist

The MVP can be submitted for final review when the following conditions are satisfied:

- [ ] Lost Item reporting works.
- [ ] Found Item reporting works.
- [ ] Required fields are validated.
- [ ] Item categories are stored correctly.
- [ ] Campus locations are stored correctly.
- [ ] Lost and Found report types are stored correctly.
- [ ] Optional item photos work correctly.
- [ ] Reports receive unique IDs.
- [ ] Users can browse reports.
- [ ] Keyword search works.
- [ ] Category filtering works.
- [ ] Location filtering works.
- [ ] Lost/Found filtering works.
- [ ] Item details can be viewed.
- [ ] Report status is displayed.
- [ ] Reports can be marked as resolved.
- [ ] Resolved reports are separated from active reports.
- [ ] Database relationships work correctly.
- [ ] Invalid information is rejected.
- [ ] The website is responsive.
- [ ] Error messages are understandable.
- [ ] No critical defects remain.
- [ ] No passwords, API keys, or database credentials are committed to GitHub.

---

## 7. Testing Evidence

After development begins, the team should record evidence for important acceptance criteria.

| Criterion | Result     | Evidence | Tester | Date |
| --------- | ---------- | -------- | ------ | ---- |
| AC-01     | Not Tested |          |        |      |
| AC-02     | Not Tested |          |        |      |
| AC-03     | Not Tested |          |        |      |
| AC-04     | Not Tested |          |        |      |
| AC-05     | Not Tested |          |        |      |
| AC-06     | Not Tested |          |        |      |
| AC-07     | Not Tested |          |        |      |
| AC-08     | Not Tested |          |        |      |
| AC-09     | Not Tested |          |        |      |
| AC-10     | Not Tested |          |        |      |
| AC-11     | Not Tested |          |        |      |
| AC-12     | Not Tested |          |        |      |
| AC-13     | Not Tested |          |        |      |
| AC-14     | Not Tested |          |        |      |
| AC-15     | Not Tested |          |        |      |
| AC-16     | Not Tested |          |        |      |
| AC-17     | Not Tested |          |        |      |
| AC-18     | Not Tested |          |        |      |
| AC-19     | Not Tested |          |        |      |
| AC-20     | Not Tested |          |        |      |
| AC-21     | Not Tested |          |        |      |
| AC-22     | Not Tested |          |        |      |
| AC-23     | Not Tested |          |        |      |
| AC-24     | Not Tested |          |        |      |
| AC-25     | Not Tested |          |        |      |
| AC-26     | Not Tested |          |        |      |
| AC-27     | Not Tested |          |        |      |
| AC-28     | Not Tested |          |        |      |
| AC-29     | Not Tested |          |        |      |
| AC-30     | Not Tested |          |        |      |

---
