# Verify Filters, Search, Status and Sort Functionality

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot |
|--------------|--------------|---------------|------------|-----------------|------------|
| TC13 | User should have access to Filters/Search page | User should be able to filter data using search | Open application page, locate Search field, enter valid keyword, click Search | System should display only matching records based on search input | <img width="333" height="619" alt="image" src="https://github.com/user-attachments/assets/02dcc321-d754-4283-a885-215bc841a069" />|
| TC14 | User should have access to Filters section | User should be able to filter records by Last Saved date | Open Filters, select Last Saved date range (mm/dd/yyyy), apply filter | System should display records matching selected Last Saved date range |  ![DF_001]|
| TC15 | User should have access to Filters section | User should be able to filter records by Last Executed date | Open Filters, select Last Executed date range (mm/dd/yyyy), apply filter | System should display records matching selected Last Executed date range | <img width="1892" height="1022" alt="image" src="https://github.com/user-attachments/assets/d0bb21af-9e80-4854-9626-6c6284b9749f" />
|
| TC16 | User should have access to status filter options | User should be able to filter by Inactive status | Select status filter = Inactive | System should display only Inactive records | <img width="1889" height="673" alt="image" src="https://github.com/user-attachments/assets/bf17775e-7144-4ece-b706-dd39e18d3f95" />
|
| TC17 | User should have access to status filter options | User should be able to filter by Queued status | Select status filter = Queued | System should display only Queued records | <img width="711" height="855" alt="image" src="https://github.com/user-attachments/assets/7d4e9bc2-97e3-4f93-8532-cb5b0a7adb38" />
|
| TC18 | User should have access to status filter options | User should be able to filter by Active status | Select status filter = Active | System should display only Active records | |
| TC19 | User should have access to status filter options | User should be able to filter by Completed status | Select status filter = Completed | System should display only Completed records | |
| TC20 | User should have access to status filter options | User should be able to filter by Error status | Select status filter = Error | System should display only Error records | <img width="1874" height="732" alt="image" src="https://github.com/user-attachments/assets/ee24dc39-854f-4f74-ab57-60aae662c7c0" />
|
| TC21 | User should have access to status filter options | User should be able to filter by Scheduled status | Select status filter = Scheduled | System should display only Scheduled records | <img width="1550" height="357" alt="image" src="https://github.com/user-attachments/assets/47c7c544-0bb7-4a6d-9355-ba4101770d74" />
|
| TC22 | User should have access to Sort functionality | User should be able to sort records | Open Sort dropdown, select sorting option (Last Saved / Last Executed / Name), apply sort | System should reorder records based on selected sorting option | |
