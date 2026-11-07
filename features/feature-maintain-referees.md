# Feature: Maintain Referee
**Feature ID:** MR
**Branch pattern:** `feature/MR-maintain-referee`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Referee
**As a** System Admin
**I want to** input the information of a new referee
**So that** the referee is created in a league
**Priority:** P1
**Independent test:** add a new referee and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove Referee
**As a** System Admin
**I want to** select an existing referee for removal
**So that** the league removes this referee's information
**Priority:** P1
**Independent test:** remove a referee and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit Referee
**As a** System Admin
**I want to** input new information for an existing referee
**So that** the information for that referee is updated in the league
**Priority:** P1
**Independent test:** edit an existing referee in the league and have the new information updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit referees
- **FR-002**: System MUST store information of referees in a league

---
## Key Entities
- **User**: System Admin; maintains most data for the referees
- **Database**: information storage; tracks information including referees and their information

---
## Acceptance Criteria
### US-N.1 - Add Referee
#### Scenario: Admin adds a new referee to the league
* **Given** I am prompted to enter information for the new referee
* **When** I enter the referee's information
* **And** The referee does not already exist in the league
* **Then** The referee's information is added to the league
#### Scenario: Manager attempts to add an existing referee to the league
* **Given** I am prompted to enter information for the new referee
* **When** I enter the referee's information
* **And** The referee already exists in the league
* **Then** I am informed that the referee already exists and am prompted to either edit the referee's information or cancel the operation

### US-N.2 - Remove Referee
#### Scenario: Manager removes an existing referee from the league
* **Given** There is an existing referee in the league
* **When** I select the referee I wish to delete
* **Then** The referee's information is removed from the league

### US-N.3 - Edit Referee
#### Scenario: Manager changes an existing referee's information
* **Given** There is an existing referee in the league
* **When** I select the referee I wish to edit
* **And** I enter new information for the referee 
* **Then** The referee's information is changed the league

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays referee information

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the referee.
*   Primary action: **Edit Referee**.
*   Buttons to save or cancel editing of referee
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the referee.
*   Primary action: **Add Referee**.
*   Buttons to save or cancel addition of referee
*   Verify pressing of save or cancel button