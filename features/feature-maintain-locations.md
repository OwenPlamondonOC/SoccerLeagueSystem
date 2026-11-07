# Feature: Maintain Location
**Feature ID:** MLO
**Branch pattern:** `feature/MLO-maintain-location`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Location
**As a** System Admin
**I want to** input the information of a new location
**So that** the location is created in a database
**Priority:** P1
**Independent test:** add a new location and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove Location
**As a** System Admin
**I want to** select an existing location for removal
**So that** the database removes this location's information
**Priority:** P1
**Independent test:** remove a location and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit Location
**As a** System Admin
**I want to** input new information for an existing location
**So that** the information for that location is updated in the database
**Priority:** P1
**Independent test:** edit an existing location in the database and have the new information updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit locations
- **FR-002**: System MUST store information of locations in a database

---
## Key Entities
- **User**: System Admin; maintains most data for the locations
- **Database**: information storage; tracks information including locations and their information

---
## Acceptance Criteria
### US-N.1 - Add Location
#### Scenario: Admin adds a new location to the system
* **Given** I am prompted to enter information for the new location
* **When** I enter the location's information
* **And** The location does not already exist in the system
* **Then** The location's information is added to the system
#### Scenario: Manager attempts to add an existing location to the system
* **Given** I am prompted to enter information for the new location
* **When** I enter the location's information
* **And** The location already exists in the system
* **Then** I am informed that the location already exists and am prompted to either edit the location's information or cancel the operation

### US-N.2 - Remove Location
#### Scenario: Manager removes an existing location from the system
* **Given** There is an existing location in the system
* **When** I select the location I wish to delete
* **Then** The location's information is removed from the system

### US-N.3 - Edit Location
#### Scenario: Manager changes an existing location's information
* **Given** There is an existing location in the system
* **When** I select the location I wish to edit
* **And** I enter new information for the location 
* **Then** The location's information is changed the system

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays location information

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the location.
*   Primary action: **Edit Location**.
*   Buttons to save or cancel editing of location
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the location.
*   Primary action: **Add Location**.
*   Buttons to save or cancel addition of location
*   Verify pressing of save or cancel button