# Feature: Maintain Users
**Feature ID:** MU
**Branch pattern:** `feature/MU-maintain-users`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Users
**As a** System Admin
**I want to** input the information and access level of a new users
**So that** the users is created in a database
**Priority:** P1
**Independent test:** add a new users and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove Users
**As a** System Admin
**I want to** select an existing users for removal
**So that** the database removes this users's information
**Priority:** P1
**Independent test:** remove a users and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit Users
**As a** System Admin
**I want to** input new information and access level for an existing users
**So that** the information and access level for that users is updated in the database
**Priority:** P1
**Independent test:** edit an existing users in the database and have the new information and access level updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit users
- **FR-002**: System MUST store information and access level of users in a database

---
## Key Entities
- **User**: System Admin; maintains most data for the users
- **Database**: information storage; tracks information including users and their information and access level

---
## Acceptance Criteria
### US-N.1 - Add Users
#### Scenario: Admin adds a new users to the system
* **Given** I am prompted to enter information and access level for the new users
* **When** I enter the users's information and access level
* **And** The users does not already exist in the system
* **Then** The users's information and access level is added to the system
#### Scenario: Manager attempts to add an existing users to the system
* **Given** I am prompted to enter information and access level for the new users
* **When** I enter the users's information and access level
* **And** The users already exists in the system
* **Then** I am informed that the users already exists and am prompted to either edit the users's information and access level or cancel the operation

### US-N.2 - Remove Users
#### Scenario: Manager removes an existing users from the system
* **Given** There is an existing users in the system
* **When** I select the users I wish to delete
* **Then** The users's information and access level is removed from the system

### US-N.3 - Edit Users
#### Scenario: Manager changes an existing users's information and access level
* **Given** There is an existing users in the system
* **When** I select the users I wish to edit
* **And** I enter new information and access level for the users 
* **Then** The users's information and access level is changed the system

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays users information and access level

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the users.
*   Primary action: **Edit Users**.
*   Buttons to save or cancel editing of users
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the users.
*   Primary action: **Add Users**.
*   Buttons to save or cancel addition of users
*   Verify pressing of save or cancel button