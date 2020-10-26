﻿# 1. Delete Group

## 1.1 Brief Description
Delete Group is the "Delete" - part of the CRUD "manage Group".
The right to delete a group is reserved to members of the group with the role 'owner'.


# 2. Flow of Events
## 2.1 Basic Flow
- owner clicks on "group settings" button
- owner clicks on "delete group" button and will be sent back to the front page - this action will delete the group entity
### 2.1.1 Activity Diagram
![](https://github.com/placetobeer/documentation/blob/master/manageGroupUML.png)
### 2.1.2 Mock-up

### 2.1.3 Narrative
```gherkin
Feature: new operation

  As a signed in user
  i want to create a new operation
  and provide additional information regarding my intentions
  in order to find willing helpers.

  Background:
    And I am on the homepage

  Scenario: open new operation dialog
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "main" page
    When I press the "new operation" button
    Then I am on the "new operation" page

  Scenario: enter valid data and save the operation
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "new operation" page
    When I enter "operation XY" in the field "title"
    And I enter "Karlsruhe" in the field "location"
    And I enter "01.01.2018" in the field "date"
    And I enter "public description" in the field "public_descripion"
    And I enter "private description" in the field "private_description"
    And I press the "save" button
    Then I am on the "details" page
    And I receive a "success" message

  Scenario: enter invalid data and save the operation
    Given I am signed in with username "USER" and password "PASSWORD"
    And I am on the "new operation" page
    When I enter "operation XY" in the field "title"
    And I enter "Karlsruhe" in the field "location"
    And I enter "no date" in the field "date"
    And I enter "" in the field "public_descripion"
    And I enter "" in the field "private_description"
    And I press the "save" button
    Then I am on the "new operation" page
    And I receive a "error" message
```



## 2.2 Alternative Flows
(n/a)

# 3. Special Requirements
(n/a)

# 4. Preconditions
tbd

# 5. Postconditions
(n/a)
 
# 6. Extension Points
(n/a)


