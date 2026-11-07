# Feature: Maintain Season
**Feature ID:** MS
**Branch pattern:** `feature/MS-maintain-season`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Season
**As a** System Admin
**I want to** input the information of a new season
**So that** the season is created in a database
**Priority:** P1
**Independent test:** add a new season and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove Season
**As a** System Admin
**I want to** select an existing season for removal
**So that** the database removes this season's information
**Priority:** P1
**Independent test:** remove a season and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit Season
**As a** System Admin
**I want to** input new information for an existing season
**So that** the information for that season is updated in the database
**Priority:** P1
**Independent test:** edit an existing season in the database and have the new information updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit seasons
- **FR-002**: System MUST store information of seasons in a database

---
## Key Entities
- **User**: System Admin; maintains most data for the seasons
- **Database**: information storage; tracks information including seasons and their information

---
## Acceptance Criteria
### US-N.1 - Add Season
#### Scenario: Admin adds a new season to the system
* **Given** I am prompted to enter information for the new season
* **When** I enter the season's information
* **And** The season does not already exist in the system
* **Then** The season's information is added to the system
#### Scenario: Manager attempts to add an existing season to the system
* **Given** I am prompted to enter information for the new season
* **When** I enter the season's information
* **And** The season already exists in the system
* **Then** I am informed that the season already exists and am prompted to either edit the season's information or cancel the operation

### US-N.2 - Remove Season
#### Scenario: Manager removes an existing season from the system
* **Given** There is an existing season in the system
* **When** I select the season I wish to delete
* **Then** The season's information is removed from the system

### US-N.3 - Edit Season
#### Scenario: Manager changes an existing season's information
* **Given** There is an existing season in the system
* **When** I select the season I wish to edit
* **And** I enter new information for the season 
* **Then** The season's information is changed the system

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays season information

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the season.
*   Primary action: **Edit Season**.
*   Buttons to save or cancel editing of season
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the season.
*   Primary action: **Add Season**.
*   Buttons to save or cancel addition of season
*   Verify pressing of save or cancel button