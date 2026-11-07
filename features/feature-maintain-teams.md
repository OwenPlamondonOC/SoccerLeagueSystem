# Feature: Maintain Teams
**Feature ID:** MT
**Branch pattern:** `feature/MT-maintain-teams`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Team
**As a** System Admin
**I want to** input the information of a new team
**So that** the team is created in a league
**Priority:** P1
**Independent test:** add a new team and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove Team
**As a** System Admin
**I want to** select an existing team for removal
**So that** the league removes this team's information
**Priority:** P1
**Independent test:** remove a team and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit Team
**As a** System Admin
**I want to** input new information for an existing team
**So that** the information for that team is updated in the league
**Priority:** P1
**Independent test:** edit an existing team in the league and have the new information updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit teams
- **FR-002**: System MUST store information of teams in a league

---
## Key Entities
- **User**: System Admin; maintains most data for the teams
- **Database**: information storage; tracks information including teams and their information

---
## Acceptance Criteria
### US-N.1 - Add Team
#### Scenario: Admin adds a new team to the league
* **Given** I am prompted to enter information for the new team
* **When** I enter the team's information
* **And** The team does not already exist in the league
* **Then** The team's information is added to the league
#### Scenario: Manager attempts to add an existing team to the league
* **Given** I am prompted to enter information for the new team
* **When** I enter the team's information
* **And** The team already exists in the league
* **Then** I am informed that the team already exists and am prompted to either edit the team's information or cancel the operation

### US-N.2 - Remove Team
#### Scenario: Manager removes an existing team from the league
* **Given** There is an existing team in the league
* **When** I select the team I wish to delete
* **Then** The team's information is removed from the league

### US-N.3 - Edit Team
#### Scenario: Manager changes an existing team's information
* **Given** There is an existing team in the league
* **When** I select the team I wish to edit
* **And** I enter new information for the team 
* **Then** The team's information is changed the league

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays team information

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the team.
*   Primary action: **Edit Team**.
*   Buttons to save or cancel editing of team
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the team.
*   Primary action: **Add Team**.
*   Buttons to save or cancel addition of team
*   Verify pressing of save or cancel button