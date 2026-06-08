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
