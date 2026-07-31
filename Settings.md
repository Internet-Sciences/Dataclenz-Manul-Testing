# Settings - Upload Source Positive Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_001 | User is logged in | Settings page is displayed | Navigate to Settings page | Settings page should load successfully with all sections displayed |<img width="1198" height="1056" alt="image" src="https://github.com/user-attachments/assets/b6a3e10f-0ec6-40f6-8de5-ff4611870b97" /> <img width="1143" height="711" alt="image" src="https://github.com/user-attachments/assets/0732d522-4db8-433f-8728-9f0f0f2914c0" />  | | |
| TC_002 | User is on Settings page | Preferences saved | Check CSV Files checkbox and click Save Preferences | Preferences should be saved successfully | <img width="1073" height="98" alt="image" src="https://github.com/user-attachments/assets/8daacf81-80ee-4b6b-a171-645978ba4a29" />| | |
| TC_003 | User is on Settings page | Preferences saved | Check Excel Files (XLSX) checkbox and click Save Preferences | XLSX upload source should be enabled | <img width="1090" height="108" alt="image" src="https://github.com/user-attachments/assets/268c93d6-1650-4344-b76e-888e009a96f9" />| | |
| TC_004 | User is on Settings page | Preferences saved | Check Excel Files (XLS) checkbox and click Save Preferences | XLS upload source should be enabled |<img width="1105" height="109" alt="image" src="https://github.com/user-attachments/assets/e765b1d8-4909-4d27-8352-98cfac3263c8" /> | | |
| TC_005 | User is on Settings page | Preferences saved | Check JSON Files checkbox and click Save Preferences | JSON upload source should be enabled |<img width="1104" height="99" alt="image" src="https://github.com/user-attachments/assets/90095924-02a7-425a-aaf4-d7e1a20e2e2b" /> | | |
| TC_006 | User is on Settings page | Preferences saved | Check MySQL Databases checkbox and click Save Preferences | MySQL upload source should be enabled |<img width="1102" height="87" alt="image" src="https://github.com/user-attachments/assets/772830d7-a8c3-4a82-aca9-4f62bcc49dbc" /> | | |
| TC_007 | User is on Settings page | Preferences saved | Check Azure Fabric Warehouses checkbox and click Save Preferences | Azure Fabric upload source should be enabled |<img width="1101" height="91" alt="image" src="https://github.com/user-attachments/assets/d596e834-87f1-4bc5-b1db-97a59c40c362" /> | | |
| TC_008 | User is on Settings page | Preferences saved | Check SFTP Servers checkbox and click Save Preferences | SFTP upload source should be enabled | <img width="1109" height="97" alt="image" src="https://github.com/user-attachments/assets/d6f6b0c0-4e0c-4d43-9c2a-371812441f5a" />| | |
| TC_009 | User is on Settings page | Preferences saved | Check Azure Blob Storage checkbox and click Save Preferences | Azure Blob upload source should be enabled |<img width="1092" height="101" alt="image" src="https://github.com/user-attachments/assets/a4d72cb6-641f-4b80-a4a0-94a3d3395817" /> | | |

# Download Format

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_010 | User is on Settings page | Preferences saved | Check CSV Format download option and click Save Preferences | CSV download format should be enabled |<img width="1081" height="104" alt="image" src="https://github.com/user-attachments/assets/65fed47a-d4d7-4f21-97d2-e90f903d121a" /> | | |
| TC_011 | User is on Settings page | Preferences saved | Check Excel Format (XLSX) and save | XLSX download format should be enabled |<img width="1096" height="103" alt="image" src="https://github.com/user-attachments/assets/a195a905-1c18-4574-ad3a-e8db58caadb2" /> | | |
| TC_012 | User is on Settings page | Preferences saved | Check JSON Format and save | JSON download format should be enabled |<img width="1083" height="93" alt="image" src="https://github.com/user-attachments/assets/9079a638-e88f-42c7-b2d1-1f320e5e6c09" /> | | |
| TC_013 | User is on Settings page | Preferences saved | Check TXT Format and save | TXT download format should be enabled |<img width="1109" height="94" alt="image" src="https://github.com/user-attachments/assets/d666185d-cfa9-4b83-b8b2-8b886c969d5b" /> | | |
| TC_014 | User is on Settings page | Decimal precision saved | Enter valid decimal precision value and click Save Preferences | Decimal precision should be saved successfully |<img width="1126" height="213" alt="image" src="https://github.com/user-attachments/assets/c669745a-3d73-41ce-af57-7086434e6147" /> | | |
| TC_015 | User has saved preferences | Preferences retained | Refresh browser | Previously saved preferences should remain selected |<img width="1193" height="750" alt="image" src="https://github.com/user-attachments/assets/3b94c75e-8a30-46b5-9ae6-660c77698bb7" /> | | |
| TC_016 | User has saved preferences | Preferences retained | Log out and log back in | Saved preferences should persist after login | | | |
| TC_017 | CSV upload source is enabled | Upload allowed | Navigate to Upload Data and select CSV file | CSV file should be selectable for upload | | | |
| TC_018 | XLSX upload source is enabled | Upload allowed | Navigate to Upload Data and select XLSX file | XLSX file should be selectable for upload | | | |
| TC_019 | JSON download format is enabled | Download allowed | Download data in JSON format | JSON format should be available for download | | | |

# Settings - Negative Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_001 | User is on Settings page | Upload source disabled | Uncheck CSV Files, save preferences, attempt to upload CSV | CSV file should not be selectable/uploadable |<img width="1098" height="100" alt="image" src="https://github.com/user-attachments/assets/17774cb8-d3f3-4d53-a7a5-b38805f33dc7" /> <img width="238" height="215" alt="image" src="https://github.com/user-attachments/assets/15fc2cc9-289c-49b6-ae31-50478ffcdd95" /> | | |
| TC_002 | User is on Settings page | Upload source disabled | Uncheck XLSX Files, save preferences, attempt to upload XLSX | XLSX file should not be selectable/uploadable |<img width="1098" height="103" alt="image" src="https://github.com/user-attachments/assets/8dc18d86-e18b-47ee-a4ab-19b203a42ca4" /> <img width="237" height="203" alt="image" src="https://github.com/user-attachments/assets/f02f4a38-d15c-48b2-af5e-afd75ef80a6d" /> | | |
| TC_003 | User is on Settings page | Upload source disabled | Uncheck XLS Files, save preferences, attempt to upload XLS | XLS file should not be selectable/uploadable | <img width="1092" height="105" alt="image" src="https://github.com/user-attachments/assets/44887035-ed2e-4280-8859-18f3629d57e0" />| | |
| TC_004 | User is on Settings page | Upload source disabled | Uncheck JSON Files, save preferences, attempt to upload JSON | JSON file should not be selectable/uploadable | | | |
| TC_005 | User is on Settings page | Download format disabled | Uncheck CSV Format, save preferences, attempt CSV download | CSV download option should not be available | | | |
| TC_006 | User is on Settings page | Download format disabled | Uncheck XLSX Format and save | XLSX download option should not be available | | | |
| TC_007 | User is on Settings page | Download format disabled | Uncheck JSON Format and save | JSON download option should not be available | | | |
| TC_008 | User is on Settings page | Download format disabled | Uncheck TXT Format and save | TXT download option should not be available | | | |
| TC_009 | User is on Settings page | Invalid input rejected | Enter alphabetic characters in Decimal Precision | Validation message should appear or value should be rejected |<img width="1135" height="252" alt="image" src="https://github.com/user-attachments/assets/07700494-f367-4b97-bc9a-d8d265e08722" /> | | |
| TC_010 | User is on Settings page | Invalid input rejected | Enter negative value in Decimal Precision | System should reject invalid value |<img width="1109" height="248" alt="image" src="https://github.com/user-attachments/assets/a57be506-097b-441a-8ec0-e311d1eb6b9b" /> | | |
| TC_011 | User is on Settings page | Validation displayed | Leave Decimal Precision empty (if required) and save | Appropriate validation should be displayed |<img width="1132" height="237" alt="image" src="https://github.com/user-attachments/assets/565690a1-8ad8-4c3e-9d17-ec573abe6eb7" /> | | |
| TC_012 | User session expires | Save fails | Modify settings after session timeout and click Save Preferences | User should be redirected to login or shown session expired message | | | |

# Settings - Edge Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_001 | User is on Settings page | All upload sources enabled | Select every Upload Source checkbox and save | All upload sources should be enabled successfully | | | |
| TC_002 | User is on Settings page | All upload sources disabled | Uncheck every Upload Source checkbox and save | No upload source should be available for file selection | | | |
| TC_003 | User is on Settings page | All download formats enabled | Select every Download Format checkbox and save | All download formats should be available | | | |
| TC_004 | User is on Settings page | All download formats disabled | Uncheck every Download Format checkbox and save | No download format should be available | | | |
| TC_005 | User is on Settings page | Decimal precision saved | Enter value 0 and save | Values should remain unchanged during export as per specification | | | |
| TC_006 | User is on Settings page | Decimal precision saved | Enter maximum allowed decimal value and save | Maximum supported precision should be accepted | | | |
| TC_007 | User is on Settings page | Latest settings retained | Rapidly check/uncheck multiple options before saving | Final saved state should match the latest selections | | | |
| TC_008 | User is on Settings page | Preferences retained | Save preferences and refresh browser immediately | Saved preferences should persist | | | |
| TC_009 | User is logged in on multiple browser tabs | Preferences synchronized | Change settings in one tab and refresh another | Updated preferences should be reflected | | | |
| TC_010 | User is on Settings page | Application remains stable | Click Save Preferences multiple times rapidly | Only one save operation should occur and no duplicate requests should be made | | | |
