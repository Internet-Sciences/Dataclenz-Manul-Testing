# Lists - Positive Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_LIST_001 | User is logged in | Lists page is displayed | Navigate to the Lists page | Lists page loads successfully with Search, Filters, Upload List section, and uploaded files displayed | | | |
| TC_LIST_002 | User is on Lists page | Search field is available | Verify Search textbox | Search textbox is visible and editable |<img width="1354" height="679" alt="image" src="https://github.com/user-attachments/assets/fcbad844-6c29-4994-9a65-a8a8e24f6484" /> <img width="1402" height="669" alt="image" src="https://github.com/user-attachments/assets/9f4dc4ea-af4b-4ccf-b22a-4266683a0be0" />| | |
| TC_LIST_003 | User has uploaded lists | Matching files are displayed | Enter an existing filename in Search | Only matching file(s) should be displayed |<img width="1400" height="669" alt="image" src="https://github.com/user-attachments/assets/d6c39df7-f339-41f7-b17a-a46dc4724243" />| | |
| TC_LIST_004 | User has uploaded lists | All files displayed | Clear Search field | Complete list should be displayed |<img width="1023" height="590" alt="image" src="https://github.com/user-attachments/assets/c023cdac-96ca-45ec-a9c8-fecd2a97d423" /> | | |
| TC_LIST_005 | Lists exist | Date filter applied | Select a valid Created At date | Only files created on the selected date should be displayed |<img width="1398" height="698" alt="image" src="https://github.com/user-attachments/assets/2083d036-2485-4a54-8e0e-4d84bbf0e97a" /> | | |
| TC_LIST_006 | Lists exist | Files sorted | Select each Sort By option | Files should be sorted according to selected option |<img width="1386" height="661" alt="image" src="https://github.com/user-attachments/assets/d08303f4-f104-4ef1-bf3c-cccfcfb26ca2" /> <img width="1393" height="662" alt="image" src="https://github.com/user-attachments/assets/ce554eaa-9938-43e0-a897-8b4232ad2900" /> | | |
| TC_LIST_007 | User is on Lists page | File selected | Click Select File and choose a valid CSV/XLSX file | Selected filename should appear below Select File | <img width="322" height="230" alt="image" src="https://github.com/user-attachments/assets/07f7c41f-715a-4b14-b88d-35291ef37a55" />| | |
| TC_LIST_008 | Valid file selected | File uploaded | Click Upload | File uploads successfully and appears in the list |<img width="1024" height="114" alt="image" src="https://github.com/user-attachments/assets/a2c25bb6-6d40-44e0-a66e-2b79375195c7" /> | | |
| TC_LIST_009 | Uploaded files exist | File downloaded | Click Download icon | Selected file should download successfully | <img width="182" height="96" alt="image" src="https://github.com/user-attachments/assets/1625f27a-ac29-4ad1-98a9-2487768a9c67" />| | |
| TC_LIST_010 | Uploaded files exist | Rename completed | Click Edit icon, enter new filename, save | File name should update successfully |<img width="419" height="307" alt="image" src="https://github.com/user-attachments/assets/9ffd94cf-ad33-4cd7-83f1-437f6fc1879e" /> <img width="451" height="304" alt="image" src="https://github.com/user-attachments/assets/22f404a2-5712-4c9c-bd24-87c328942725" />
<img width="980" height="109" alt="image" src="https://github.com/user-attachments/assets/78053168-d780-457d-8086-573a90b4aa30" /> | | |
| TC_LIST_011 | Uploaded files exist | File deleted | Click Delete icon and confirm deletion | File should be removed from the list |<img width="567" height="313" alt="image" src="https://github.com/user-attachments/assets/8353cb4f-5ca3-49c3-88db-9c51ae5f8b4d" /> | | |
| TC_LIST_012 | Uploaded files exist | Append operation completed | Click Add (+) icon | User should be able to append/upload additional data to the selected list | <img width="521" height="455" alt="image" src="https://github.com/user-attachments/assets/d8eaec95-6b36-4f15-afac-7ee184a62a64" />| | |
| TC_LIST_013 | Uploaded files exist | View changed | Click Grid/List view toggle | Display should switch between available layouts | <img width="1057" height="415" alt="image" src="https://github.com/user-attachments/assets/63727b27-bec9-45cb-b11a-4386fa76dcbe" />| | |
| TC_LIST_014 | Uploaded files exist | Counts displayed | Verify Total and Filtered count | Counts should accurately reflect displayed records |<img width="274" height="105" alt="image" src="https://github.com/user-attachments/assets/aa0f5d99-6c6b-4c91-9531-cd8f2601b7de" /> | | |

# Lists - Negative Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_LIST_NEG_001 | User is on Lists page | Upload prevented | Click Upload without selecting a file | Validation message should be displayed | | | |
| TC_LIST_NEG_002 | User is on Lists page | Invalid file rejected | Select unsupported file (.txt, .exe, .zip) | System should reject unsupported file type | | | |
| TC_LIST_NEG_003 | User is on Lists page | Upload prevented | Select an empty CSV/XLSX file and upload | Validation message should be displayed | | | |
| TC_LIST_NEG_004 | User is on Lists page | Upload prevented | Select corrupted file | System should display upload failure message | | | |
| TC_LIST_NEG_005 | Uploaded files exist | No results shown | Search for a filename that does not exist | "No results found" or empty list should be displayed | | | |
| TC_LIST_NEG_006 | Uploaded files exist | Invalid date ignored | Enter invalid Created At date (if allowed) | Validation should prevent invalid date | | | |
| TC_LIST_NEG_007 | Uploaded files exist | Rename rejected | Rename file using blank filename | Validation message should appear | | | |
| TC_LIST_NEG_008 | Uploaded files exist | Rename rejected | Rename using duplicate filename | System should prevent duplicate names or display validation | | | |
| TC_LIST_NEG_009 | Uploaded files exist | Delete cancelled | Click Delete then cancel confirmation | File should remain in the list | | | |
| TC_LIST_NEG_010 | User loses internet connection | Upload fails gracefully | Start upload then disconnect internet | Appropriate network error message should appear | | | |
| TC_LIST_NEG_011 | Session expired | User redirected | Perform Upload/Delete after session timeout | User should be redirected to login or shown session expired message | | | |
| TC_LIST_NEG_012 | Uploaded files exist | Download failure handled | Attempt download when backend is unavailable | Appropriate error message should be displayed | | | |

# Lists - Edge Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_LIST_EDGE_001 | User is on Lists page | Large file uploaded | Upload file at maximum supported size | Upload should complete successfully within expected time | | | |
| TC_LIST_EDGE_002 | User is on Lists page | Upload rejected | Upload file exceeding maximum size | System should reject file and display size limit message | | | |
| TC_LIST_EDGE_003 | User is on Lists page | Long filename handled | Upload file with very long filename | Filename should display correctly or be truncated without affecting upload | | | |
| TC_LIST_EDGE_004 | User is on Lists page | Special characters handled | Upload file with spaces and special characters in filename | Upload should complete successfully if supported | | | |
| TC_LIST_EDGE_005 | User has many uploaded files | Pagination/scroll works | Verify page with large number of uploaded files | Performance should remain acceptable and files should load correctly | | | |
| TC_LIST_EDGE_006 | Uploaded files exist | Duplicate upload handled | Upload the same file twice | System should either allow versioning or prevent duplicates according to business rules | | | |
| TC_LIST_EDGE_007 | Uploaded files exist | Search performance verified | Search while hundreds of files exist | Results should appear quickly and accurately | | | |
| TC_LIST_EDGE_008 | Uploaded files exist | Multiple actions handled | Rapidly click Upload/Delete/Edit buttons | System should prevent duplicate requests and remain stable | | | |
| TC_LIST_EDGE_009 | Upload in progress | Refresh behavior verified | Refresh browser during upload | Upload should resume, fail gracefully, or notify user according to application behavior | | | |
| TC_LIST_EDGE_010 | Uploaded files exist | Unicode supported | Upload file with Unicode characters in filename | Filename should display correctly without corruption | | | |
| TC_LIST_EDGE_011 | Uploaded files exist | Date filter boundary verified | Filter using earliest/latest available upload date | Correct files should be displayed | | | |
| TC_LIST_EDGE_012 | Uploaded files exist | Count accuracy verified | Upload, delete, and search files | Total and Filtered counts should always remain accurate | | | |
