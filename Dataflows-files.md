# Verify Data Flow Upload Functionality - Positive Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC01 | User is signed in to DataClenz and on DataFlows page | File is uploaded successfully and visible in DataFlows list | 1. Login to DataClenz 2. Navigate to DataFlows 3. Click “Upload Data” 4. Select “Local” 5. Choose valid CSV file 6. Click Open/Upload | File should be successfully uploaded and displayed in DataFlows tab | <img width="1002" height="490" alt="image" src="https://github.com/user-attachments/assets/1c1b8f96-aa3d-4ac6-94ab-6dfa13826fc6" /> <img width="1509" height="425" alt="image" src="https://github.com/user-attachments/assets/51c8dd1b-a847-4a9c-a1ce-1941374796de" /> | Pass |  |
| TC02 | User is on Upload Data modal | File upload process starts from system file picker | 1. Click Upload Data 2. Select Local 3. Open file explorer 4. Select valid XLSX file | System file picker should open and file should be selectable | <img width="1509" height="425" alt="image" src="https://github.com/user-attachments/assets/749f1d1d-51e7-4a51-b2ae-a700e08b658c" /> | Pass |  |
| TC03 | Valid CSV file with proper format exists in local system | File is uploaded and parsed correctly | 1. Select Upload Data 2. Choose Local 3. Upload valid CSV file | File should upload without errors and data should be parsed correctly | <img width="999" height="961" alt="image" src="https://github.com/user-attachments/assets/a27cec59-78dc-4347-8442-f2d4177548ec" /> <img width="1509" height="425" alt="image" src="https://github.com/user-attachments/assets/c384cdee-7025-40ba-8c19-cf5c1c345535" /> | Pass |  |


# Verify Data Flow Upload Functionality - Negative Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC04 | User is on Upload Data screen | Upload should fail with proper error message | 1. Click Upload Data 2. Select Local 3. Try uploading .exe or unsupported file | System should reject file and show validation error (unsupported format) | ⬜ | Pass |  |
| TC05 | User has no file selected | Upload should not proceed | 1. Click Upload Data 2. Select Local 3. Close file picker without selecting file | No upload should happen and user remains on same screen | ⬜ | Pass |  |
| TC06 | Corrupted CSV/XLSX file selected | System should handle error gracefully | 1. Upload corrupted file via Local option | System should show error like “File cannot be processed” | ⬜ | Pass |  |


# Verify Data Flow Upload Functionality - Edge Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC07 | Very large CSV/XLSX file (>100MB) | System should handle upload based on limits | 1. Upload large file via Local option | Either file uploads successfully or shows size limit error | ⬜ | Pass |  |
| TC08 | File with special characters in name | File should upload successfully | 1. Select file like data@#$.csv 2. Upload | System should accept file and not break UI | ⬜ | Pass |  |
| TC09 | Slow network during upload | Upload should not break UI | 1. Start upload 2. Simulate slow network | Upload should show loader and complete or timeout gracefully | ⬜ | Pass |  |


# Optional Scenario - Data Source Integration

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC10 | User is on DataFlows page with GitHub integration enabled | Data can be sourced from GitHub (if feature exists) | 1. Navigate to DataFlows 2. Select GitHub source 3. Authenticate 4. Select repo file | File should be fetched from GitHub and listed in DataFlows | ⬜ |  |  |



# Verify DataFlows Page - File Count, Views, and File Actions

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC01 | User is logged in and on DataFlows page with uploaded files | User should see correct total and filtered file count | 1. Login to DataClenz 2. Navigate to DataFlows page 3. Observe file summary section | Total files and filtered files count should match uploaded data | <img width="204" height="84" src="https://github.com/user-attachments/assets/7d0e85c1-a726-4c53-80a5-cf3a5cf50547" /> | ✅ | |
| TC02 | User has multiple uploaded files | Filtered view should update based on applied filters | 1. Login to DataClenz 2. Navigate to DataFlows page 3. Apply filter (if available) 4. Observe file count change | Filtered file count should update dynamically based on selection | ⬜ | ⬜ | |
| TC03 | User is on DataFlows page | User should be able to switch to Grid View | 1. Navigate to DataFlows 2. Click Grid View icon | Files should be displayed in grid layout without UI break | <img width="1525" height="354" src="https://github.com/user-attachments/assets/7623e857-c73b-4ab7-b299-177fe806c510" /> | ✅ | |
| TC04 | User is on DataFlows page in Grid View | User should be able to switch to List View | 1. Navigate to DataFlows 2. Click List View icon | Files should be displayed in list format correctly | <img width="1535" height="481" src="https://github.com/user-attachments/assets/80adb74d-8e56-4125-b857-bbdd912a8694" /> | ✅ | |
| TC05 | File exists in DataFlows list | User should be able to rename file | 1. Click rename option 2. Enter new file name 3. Save changes | File name should be updated successfully and reflected in UI | <img src="https://github.com/user-attachments/assets/26cf0753-f2f3-4db9-b069-35b41ea5f6e9" /> <br> <img src="https://github.com/user-attachments/assets/6018f515-15a0-4b61-a846-af7124752217" /> | ✅ | |
| TC06 | File exists in DataFlows list | File settings should open on gear icon click | 1. Click gear/settings icon | Settings panel/modal should open with file options | <img src="https://github.com/user-attachments/assets/d3f1e389-9128-4a40-b252-b141176161fe" /> | ✅ | |
| TC07 | File exists in DataFlows list | User should be able to download file | 1. Click download icon | File should download successfully to local system | <img src="https://github.com/user-attachments/assets/eafbff05-79d7-496c-9af9-23cce5bc751c" /> | ✅ | |
| TC08 | File exists in DataFlows list | User should be able to delete file | 1. Click delete icon 2. Confirm deletion | File should be removed from DataFlows list permanently | <img src="https://github.com/user-attachments/assets/322fb038-d451-4824-8afb-219129dfdbfb" /> | ✅ | |
| TC09 | File exists and supports execution | User should be able to play/run file | 1. Click play button on file | File should execute successfully or trigger processing workflow | <img src="https://github.com/user-attachments/assets/8342968e-455b-4759-b76b-c16b2eb305f1" /> | ✅ | |
| TC10 | File exists in DataFlows page | User should be able to back up file | 1. Click "+" (backup) icon 2. Confirm action | Backup copy should be created successfully | <img src="https://github.com/user-attachments/assets/54384e6e-4e40-4028-ba19-a8d74fa03e6e" /> | ✅ | |



# Verify DataFlows - Processing Panel Functionalities

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC01 | User is logged in and on DataFlows page with files available | Processing panel should open on selecting a file | 1. Navigate to DataFlows page 2. Click on any file 3. View right-hand Processing panel | Processing panel should open with all available processing options | <img width="357" height="823" src="https://github.com/user-attachments/assets/a22e10ce-6383-4c7a-8610-730ef923f1e1" /> | Pass | DF-301 |
| TC02 | User has selected a file in DataFlows | Recipes option should be accessible | 1. Select file 2. Click on "Recipes" under Processing | User should be navigated to Recipes configuration section | <img width="337" height="393" alt="image" src="https://github.com/user-attachments/assets/efdf6b8e-9029-40f3-9cec-e75b77baff17" /> <img width="313" height="266" alt="image" src="https://github.com/user-attachments/assets/6b2a0f10-6491-4088-aa0f-36931c5cfc36" />| Pass | DF-302 |
| TC03 | User is on Processing panel | User should be able to pause automatic reruns | 1. Open Processing panel 2. Click "Pause automatic reruns" | Automatic reruns should be paused successfully | ⬜ | Pass | DF-303 |
| TC04 | User has paused processing actions | User should be able to run paused actions | 1. Click "Run paused actions" | Previously paused actions should execute successfully | ⬜ | Pass | DF-304 |
| TC05 | User is on Processing panel | User should be able to open Build with AI feature | 1. Click "✨ Build with AI" option | AI processing interface should open successfully | <img width="923" height="450" alt="image" src="https://github.com/user-attachments/assets/a97ce7ea-3900-48eb-b6af-e2d736db0dd5" />| Pass | DF-305 |
| TC06 | User is on Processing panel | User should be able to perform Calculations | 1. Click "Calculations" 2. Enter required input | System should process calculations and show correct output | <img width="313" height="910" alt="image" src="https://github.com/user-attachments/assets/e6fbb462-2896-4c75-a0f6-79426acce0ce" />| Pass | DF-306 |
| TC07 | User is on Processing panel | User should be able to Compare and Correct data | 1. Click "Compare and Correct" 2. Select datasets | System should highlight differences and allow corrections | <img width="321" height="1073" alt="image" src="https://github.com/user-attachments/assets/1a5f61fa-4fe7-4004-99f9-0552982f22fd" />| Pass | DF-307 |
| TC08 | User is on Processing panel | User should be able to Edit Columns | 1. Click "Edit Columns" 2. Modify column structure | Columns should update successfully in dataset | <img width="318" height="851" alt="image" src="https://github.com/user-attachments/assets/6716ec8b-e22b-4a44-8df6-6b42d821ce5d" />| Pass | DF-308 |
| TC09 | User is on Processing panel | User should be able to Edit Rows | 1. Click "Edit Rows" 2. Modify row data | Row changes should be saved and reflected in dataset | <img width="322" height="737" alt="image" src="https://github.com/user-attachments/assets/025fdd5a-c4d7-4da0-b004-bacff1b0859a" />| Pass | DF-309 |
| TC10 | User is on Processing panel | User should be able to Format Data | 1. Click "Format Data" 2. Apply formatting rules | Data should be formatted correctly as per selected rules | <img width="332" height="722" alt="image" src="https://github.com/user-attachments/assets/5235e04d-aa8e-4b56-bc1c-6d0f8d0ba33b" /> | Pass | DF-310 |
| TC11 | User is on Processing panel | User should be able to use List Lookup | 1. Click "List Lookup" 2. Provide lookup values | Matching records should be displayed correctly | <img width="306" height="1070" alt="image" src="https://github.com/user-attachments/assets/4330fa02-f941-4403-b905-bf29580b482e" />| Pass | DF-311 |


# Verify Recipe Functionality

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC01 | User is signed in and has an uploaded file in DataFlows | Processing actions should be visible in Recipes section | 1. Sign in to DataClenz 2. Navigate to DataFlows 3. Upload a file or select an existing file 4. Click on the file 5. View the Processing panel on the right side 6. Run any processing functionality | Executed processing action should appear under the Recipes section | <img width="1892" height="691" alt="image" src="https://github.com/user-attachments/assets/8ec13510-88b1-4037-84f8-d4ce80d1a68f" />| Pass |  |
| TC02 | User has executed at least one processing action | User should be able to save a recipe | 1. Perform any processing action 2. Locate the "+" icon next to Recipes 3. Click the "+" icon | Recipe save dialog/block should open successfully | <img width="1892" height="691" alt="image" src="https://github.com/user-attachments/assets/571a3428-4a48-4b2d-b040-fabece945ae0" /> <img width="399" height="297" alt="image" src="https://github.com/user-attachments/assets/065d357a-a181-477b-b41f-f352f6c0dc0c" />| pass |  |
| TC03 | Recipe save dialog is open | Recipe should be saved successfully | 1. Enter a valid recipe name 2. Click Save | Recipe should be saved and added to the Recipes list | <img width="405" height="302" alt="image" src="https://github.com/user-attachments/assets/441acff5-d03a-47b4-9cc0-0ca29e07d86f" /> <img width="201" height="187" alt="image" src="https://github.com/user-attachments/assets/1bacbfcd-5106-49fd-a3da-5af23eafd056" />| Pass |  |
| TC04 | User has one or more saved recipes | User should be able to view saved recipes | 1. Click on Recipes section | All previously saved recipes should be displayed in the Recipes list | ⬜ | Pass |  |
| TC05 | User has saved recipes available | User should be able to select a saved recipe | 1. Open Recipes section 2. Select a saved recipe from the list | Selected recipe should be loaded and available for use | <img width="206" height="262" alt="image" src="https://github.com/user-attachments/assets/f67136f1-672c-4502-8801-832924a699a2" /> | Pass |  |
| TC06 | User has multiple saved recipes | User should be able to select any recipe from the list | 1. Open Recipes section 2. Select different saved recipes one by one | Corresponding recipe should load successfully each time | <img width="206" height="262" alt="image" src="https://github.com/user-attachments/assets/1e196e2e-7e76-40ba-81a2-24cad5a58305" /> <img width="330" height="366" alt="image" src="https://github.com/user-attachments/assets/109a0a10-1d62-40cd-9b30-4b3cc15ce739" />| Pass |  |


# Verify Recipe Functionality - Negative Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC07 | User is signed in and has an uploaded file but no recipe has been saved | No recipes should be available for selection | 1. Sign in to DataClenz 2. Navigate to DataFlows 3. Upload or select a file 4. Perform processing actions 5. Do not save the recipe 6. Open Recipes section | No saved recipes should be displayed | <img width="211" height="337" alt="image" src="https://github.com/user-attachments/assets/1752181e-4800-4984-8268-4be22b070d01" />| Pass |  |
| TC08 | User has no saved recipes | User should not be able to select a recipe | 1. Open Recipes section without saving any recipe | Recipe selection should be unavailable or an appropriate message should be displayed | <img width="211" height="337" alt="image" src="https://github.com/user-attachments/assets/eedba2d2-11b3-4fc8-a8fe-842d80d1245c" /> | | |
| TC09 | Recipe save dialog is open | Recipe should not be saved without a valid name | 1. Click "+" next to Recipes 2. Leave Recipe Name blank 3. Click Save | Validation message should be displayed and recipe should not be saved | <img width="419" height="333" alt="image" src="https://github.com/user-attachments/assets/43657602-7848-4543-9acd-d6ecc10a77b0" />|  |  |




# Verify Calculation Functionality

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC01 | User is signed in and has an uploaded file containing Weight and Height columns | Addition calculation should be executed successfully and results should be generated in a new column | 1. Sign in to DataClenz 2. Navigate to DataFlows 3. Upload a file or select an existing file 4. Click on the file 5. Open Processing panel 6. Click Calculations 7. Select Weight column 8. Select "+" operation 9. Select Height column as second operand 10. Enter output column name "My Test" 11. Click Add to Recipe 12. Go to Output > Local 13. Click Save 14. Select Run Now | File should be processed successfully and the "My Test" column should contain Weight + Height values for each row | <img width="324" height="1017" alt="image" src="https://github.com/user-attachments/assets/fedf4d06-9a53-4751-81fe-de0ab825ab9f" /> <img width="336" height="662" alt="image" src="https://github.com/user-attachments/assets/caa0ff65-ed84-4548-9b13-dfcfc026fd27" /> <img width="330" height="932" alt="image" src="https://github.com/user-attachments/assets/4d101f0c-befa-4629-87f9-777bc3fe25a7" />| Pass |  |
| TC02 | User is signed in and has an uploaded file containing Weight and Height columns | Subtraction calculation should be executed successfully | 1. Repeat TC01 steps 1-6 2. Select Weight column 3. Select "-" operation 4. Select Height column 5. Enter output column name "My Test" 6. Add to Recipe 7. Save output locally 8. Click Run Now | "My Test" column should contain Weight - Height values for each row | <img width="306" height="914" alt="image" src="https://github.com/user-attachments/assets/d7393d33-de1d-4f45-a091-ff4e7cde6594" /> <img width="200" height="474" alt="image" src="https://github.com/user-attachments/assets/7a8871d9-e7c1-4b5e-9fd8-f12ed5741171" / | Pass |  |
| TC03 | User is signed in and has an uploaded file containing Weight and Height columns | Multiplication calculation should be executed successfully | 1. Repeat TC01 steps 1-6 2. Select Weight column 3. Select "X" operation 4. Select Height column 5. Enter output column name "My Test" 6. Add to Recipe 7. Save output locally 8. Click Run Now | "My Test" column should contain Weight × Height values for each row | <img width="200" height="474" alt="image" src="https://github.com/user-attachments/assets/c58c85ba-002b-4c06-aeac-2b154580127b" /> <img width="200" height="474" alt="image" src="https://github.com/user-attachments/assets/e03b0472-77c4-4169-a5fc-05ec6b86d413" /> | Pass |  |
| TC04 | User is signed in and has an uploaded file containing Weight and Height columns | Division calculation should be executed successfully | 1. Repeat TC01 steps 1-6 2. Select Weight column 3. Select "/" operation 4. Select Height column 5. Enter output column name "My Test" 6. Add to Recipe 7. Save output locally 8. Click Run Now | "My Test" column should contain Weight ÷ Height values for each row | <img width="309" height="920" alt="image" src="https://github.com/user-attachments/assets/2434abf8-1020-4a69-aab5-409a5eab4ec1" /> <img width="203" height="470" alt="image" src="https://github.com/user-attachments/assets/6d82df98-b509-4694-bc60-01dc5a7112c3" /> | Pass |  |


# Verify Calculation Functionality with Schedule Action

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC05 | User has configured a valid calculation | Calculation should be scheduled successfully | 1. Configure calculation 2. Add to Recipe 3. Go to Output > Local 4. Click Save 5. Select Schedule Action Set 6. Enter Date 7. Select Timezone 8. Enter Run Time 9. Enter Times value 10. Select Repeat = Daily 11. Save schedule | Calculation job should be scheduled successfully and appear in scheduled actions | <img width="334" height="879" alt="image" src="https://github.com/user-attachments/assets/6d4a1d43-cb15-4caa-823f-1cc4ca07a9d1" /> |  |  |
| TC06 | User has configured a valid calculation | Weekly schedule should be created successfully | 1. Configure calculation 2. Save output 3. Select Schedule Action Set 4. Enter Date, Timezone, Run Time and Times 5. Select Repeat = Weekly 6. Save schedule | Weekly calculation job should be scheduled successfully | <img width="327" height="827" alt="image" src="https://github.com/user-attachments/assets/dd01d804-dfec-45d9-8150-59c19a9f8178" />|  |  |
| TC07 | User has configured a valid calculation | One-time schedule should be created successfully | 1. Configure calculation 2. Save output 3. Select Schedule Action Set 4. Enter Date, Timezone, Run Time and Times 5. Select Repeat = Once 6. Save schedule | One-time calculation job should be scheduled successfully | <img width="341" height="897" alt="image" src="https://github.com/user-attachments/assets/7b1888d3-8f77-4cb7-b2cd-c759eb53bfd9" /> <img width="378" height="139" alt="image" src="https://github.com/user-attachments/assets/43601245-a3a6-448e-a173-a5593d77ddcc" /> <img width="451" height="211" alt="image" src="https://github.com/user-attachments/assets/6554774e-9560-4ed9-bf22-ac2326eb73f4" /> |  |  |

# Verify Calculation Functionality - Negative Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC08 | User is on Calculations screen | Calculation should not be saved without selecting source column | 1. Open Calculations 2. Do not select source column 3. Select operation 4. Enter output column name 5. Click Add to Recipe | Validation message should be displayed and calculation should not be saved | ⬜ |  |  |
| TC09 | User is on Calculations screen | Calculation should not be saved without selecting operation | 1. Select source column 2. Do not select operation 3. Select second operand 4. Enter output column name 5. Click Add to Recipe | Validation message should be displayed | ⬜ |  |  |
| TC10 | User is on Calculations screen | Calculation should not be saved without output column name | 1. Configure calculation completely 2. Leave output column name blank 3. Click Add to Recipe | Validation message should be displayed and recipe should not be created | ⬜ |  | |
| TC11 | User has selected Division operation | System should handle division by zero gracefully | 1. Select source column 2. Select "/" operation 3. Select column containing zero values 4. Add to Recipe 5. Run calculation | System should display an error or handle division-by-zero values without crashing | ⬜ |  |  |
| TC12 | User is scheduling a calculation | Schedule should not be saved with missing required fields | 1. Configure calculation 2. Select Schedule Action Set 3. Leave Date, Timezone or Run Time blank 4. Click Save | Validation message should be displayed and schedule should not be created | ⬜ |  |  |
| TC13 | User has no uploaded file selected | Calculation option should not execute | 1. Navigate to Processing panel without selecting a file 2. Click Calculations | System should prevent calculation setup and display an appropriate message | ⬜ |  |  |


# Verify Compare and Correct Functionality

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC01 | User is signed in and has an uploaded file with data in the Age column | Comparison should execute successfully and create output column | 1. Sign in to DataClenz 2. Navigate to DataFlows 3. Upload a file or select an existing file 4. Click on the file 5. Open Processing panel 6. Click Compare and Correct 7. Select source column = Age 8. Select comparison operator = Equal to (==) 9. Select Comparison Data = Value 10 10. Select Exact Match = Yes 11. For True action select Output Value and enter 20 12. For False action select Output Value and enter 20 13. Enter Output Column Name = MyTest 14. Click Add to Recipe 15. Go to Outputs and run the recipe | Output column "MyTest" should be created successfully and contain configured values based on comparison results | ⬜ |  |  |
| TC02 | User has uploaded a file containing Age values | Greater Than comparison should execute successfully | 1. Configure Compare and Correct 2. Select Age column 3. Select operator > 4. Enter comparison value 10 5. Configure True and False outputs 6. Add to Recipe 7. Run recipe | Rows with Age > 10 should receive the configured True output value | ⬜ |  |  |
| TC03 | User has uploaded a file containing Age values | Less Than comparison should execute successfully | 1. Select Age column 2. Select operator < 3. Enter value 10 4. Configure outputs 5. Add to Recipe and run | Rows with Age < 10 should receive the configured True output value | ⬜ |  |  |
| TC04 | User has uploaded a file containing Age values | Greater Than or Equal comparison should execute successfully | 1. Select Age column 2. Select operator >= 3. Enter value 10 4. Configure outputs 5. Run recipe | Rows with Age >= 10 should receive the configured True output value | ⬜ |  |  |
| TC05 | User has uploaded a file containing Age values | Less Than or Equal comparison should execute successfully | 1. Select Age column 2. Select operator <= 3. Enter value 10 4. Configure outputs 5. Run recipe | Rows with Age <= 10 should receive the configured True output value | ⬜ |  |  |
| TC06 | User has uploaded a file containing Status values | Not Equal comparison should execute successfully | 1. Select Status column 2. Select operator != 3. Enter comparison value 10 4. Configure outputs 5. Run recipe | Rows not matching the comparison value should receive the configured True output value | ⬜ |  |  |
| TC07 | User has uploaded a file with multiple columns | Output from Column option should work correctly | 1. Configure comparison 2. Select True Action = Output from Column 3. Select source column 4. Run recipe | Output column should contain values copied from the selected source column when condition is true | ⬜ |  |  |
| TC08 | User has uploaded a file with multiple rows | Output Zeroes option should work correctly | 1. Configure comparison 2. Select True Action = Output Zeroes 3. Run recipe | Output column should contain 0 for rows matching the condition | ⬜ |  |  |
| TC09 | User has uploaded a file with multiple rows | Remove Rows option should work correctly | 1. Configure comparison 2. Select True Action = Remove Rows 3. Run recipe | Rows matching the condition should be removed from output dataset | ⬜ |  |  |
| TC10 | User has uploaded a file | Comparison using another column should execute successfully | 1. Select source column = Age 2. Select operator > 3. Select Comparison Data = Column 4. Select another column 5. Configure outputs and run | Comparison should be performed using values from both columns | ⬜ |  |  |


