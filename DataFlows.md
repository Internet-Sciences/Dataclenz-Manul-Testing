# Verify Filters, Search, Status and Sort Functionality

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot |
|--------------|--------------|---------------|------------|-----------------|------------|
| TC13 | User should have access to Filters/Search page | User should be able to filter data using search | Open application page, locate Search field, enter valid keyword, click Search | System should display only matching records based on search input | (<img width="333" height="619" alt="image" src="https://github.com/user-attachments/assets/02dcc321-d754-4283-a885-215bc841a069" />
)
|
| TC14 | User should have access to Filters section | User should be able to filter records by Last Saved date | Open Filters, select Last Saved date range (mm/dd/yyyy), apply filter | System should display records matching selected Last Saved date range |  ![DF_001]|
| TC15 | User should have access to Filters section | User should be able to filter records by Last Executed date | Open Filters, select Last Executed date range (mm/dd/yyyy), apply filter | System should display records matching selected Last Executed date range | |
| TC16 | User should have access to status filter options | User should be able to filter by Inactive status | Select status filter = Inactive | System should display only Inactive records | |
| TC17 | User should have access to status filter options | User should be able to filter by Queued status | Select status filter = Queued | System should display only Queued records | |
| TC18 | User should have access to status filter options | User should be able to filter by Active status | Select status filter = Active | System should display only Active records | |
| TC19 | User should have access to status filter options | User should be able to filter by Completed status | Select status filter = Completed | System should display only Completed records | |
| TC20 | User should have access to status filter options | User should be able to filter by Error status | Select status filter = Error | System should display only Error records | |
| TC21 | User should have access to status filter options | User should be able to filter by Scheduled status | Select status filter = Scheduled | System should display only Scheduled records | |
| TC22 | User should have access to Sort functionality | User should be able to sort records | Open Sort dropdown, select sorting option (Last Saved / Last Executed / Name), apply sort | System should reorder records based on selected sorting option | |
