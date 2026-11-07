# Feature: Maintain League
**Feature ID:** ML
**Branch pattern:** `feature/ML-maintain-league`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create League
**As a** System Admin
**I want to** input the information of a new league
**So that** the league is created in a database
**Priority:** P1
**Independent test:** add a new league and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove League
**As a** System Admin
**I want to** select an existing league for removal
**So that** the database removes this league's information
**Priority:** P1
**Independent test:** remove a league and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit League
**As a** System Admin
**I want to** input new information for an existing league
**So that** the information for that league is updated in the database
**Priority:** P1
**Independent test:** edit an existing league in the database and have the new information updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit leagues
- **FR-002**: System MUST store information of leagues in a database

---
## Key Entities
- **User**: System Admin; maintains most data for the leagues
- **Database**: information storage; tracks information including leagues and their information

---
## Acceptance Criteria
### US-N.1 - Add League
#### Scenario: Admin adds a new league to the system
* **Given** I am prompted to enter information for the new league
* **When** I enter the league's information
* **And** The league does not already exist in the system
* **Then** The league's information is added to the system
#### Scenario: Manager attempts to add an existing league to the system
* **Given** I am prompted to enter information for the new league
* **When** I enter the league's information
* **And** The league already exists in the system
* **Then** I am informed that the league already exists and am prompted to either edit the league's information or cancel the operation

### US-N.2 - Remove League
#### Scenario: Manager removes an existing league from the system
* **Given** There is an existing league in the system
* **When** I select the league I wish to delete
* **Then** The league's information is removed from the system

### US-N.3 - Edit League
#### Scenario: Manager changes an existing league's information
* **Given** There is an existing league in the system
* **When** I select the league I wish to edit
* **And** I enter new information for the league 
* **Then** The league's information is changed the system

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays league information

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the league.
*   Primary action: **Edit League**.
*   Buttons to save or cancel editing of league
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the league.
*   Primary action: **Add League**.
*   Buttons to save or cancel addition of league
*   Verify pressing of save or cancel button