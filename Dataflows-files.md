Verify DataFlows Upload Functionality (CSV/XLSX via Local Source)
Test Case ID	Precondition	Postcondition	Test Steps	Expected Result	Screenshot	Status	Ticket
✅ Positive Test Cases

| TC01 | User is signed in to DataClenz and on DataFlows page | File is uploaded successfully and visible in DataFlows list | 1. Login to DataClenz 2. Navigate to DataFlows 3. Click “Upload Data” 4. Select “Local” 5. Choose valid CSV file 6. Click Open/Upload | File should be successfully uploaded and displayed in DataFlows tab | Yes | Not Executed | DF-101 |

| TC02 | User is on Upload Data modal | File upload process starts from system file picker | 1. Click Upload Data 2. Select Local 3. Open file explorer 4. Select valid XLSX file | System file picker should open and file should be selectable | Yes | Not Executed | DF-102 |

| TC03 | Valid CSV file with proper format exists in local system | File is uploaded and parsed correctly | 1. Select Upload Data 2. Choose Local 3. Upload valid CSV file | File should upload without errors and data should be parsed correctly | Yes | Not Executed | DF-103 |
