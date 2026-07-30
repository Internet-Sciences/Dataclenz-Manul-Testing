# Profile Page - Positive Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_PROFILE_001 | User is logged in | Profile page is displayed | Navigate to Profile page | Profile page should load successfully with all user information displayed | <img width="838" height="972" alt="image" src="https://github.com/user-attachments/assets/91674500-8153-4eb5-8bf1-6dbc778d401d" />|Pass | |
| TC_PROFILE_002 | User is on Profile page | User information displayed | Verify Email, First Name, Last Name, and Phone fields | Correct account information should be displayed | <img width="770" height="379" alt="image" src="https://github.com/user-attachments/assets/469a2f06-9636-42cf-bf1e-dd57cfdbbe37" />| | |
| TC_PROFILE_003 | User is on Profile page | Active Since displayed | Verify "Active Since" information | User's account creation/active date should be displayed correctly |<img width="617" height="175" alt="image" src="https://github.com/user-attachments/assets/fb2b19c5-6042-4f50-9606-c64583b1a142" /> | | |
| TC_PROFILE_004 | User is on Profile page | Password page opens | Click Change Password | Change Password page/modal should open | <img width="463" height="508" alt="image" src="https://github.com/user-attachments/assets/6fb90c4f-2a9e-4cb0-bba6-e7650e499b6c" />| | |
| TC_PROFILE_005 | User is on Profile page | Profile downloaded | Click Download Profile | Profile should download successfully in selected format |<img width="332" height="242" alt="image" src="https://github.com/user-attachments/assets/485e585c-4753-425c-847e-35764e410cd9" /> | | |
| TC_PROFILE_006 | User is on Profile page | Export format updated | Select CSV as Default Export Format | CSV should be saved as the default export format | <img width="779" height="212" alt="image" src="https://github.com/user-attachments/assets/54f5a603-422c-4a23-a8b9-81de2593a8fc" />| | |
| TC_PROFILE_007 | User is on Profile page | Export format updated | Select XLSX as Default Export Format | XLSX should be saved as the default export format |<img width="776" height="347" alt="image" src="https://github.com/user-attachments/assets/212daf27-2bf9-47c8-8374-8b739e4c874a" /> | | |
| TC_PROFILE_008 | User is on Profile page | User signed out | Click Sign Out | User should be logged out and redirected to Login page |<img width="436" height="484" alt="image" src="https://github.com/user-attachments/assets/d76c3a44-27f7-42ed-9600-de778c756b42" /> | | |
| TC_PROFILE_009 | User is on Profile page | Delete confirmation displayed | Click Delete Account | Confirmation dialog should appear before deleting the account | <img width="556" height="275" alt="image" src="https://github.com/user-attachments/assets/161b4cf7-7659-4332-857b-bbf1f947743f" />| | |
| TC_PROFILE_010 | User has no phone number | Phone information displayed | Verify Phone field | "Not provided" should be displayed when phone number is unavailable | | | |

# Profile Page - Negative Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_PROFILE_NEG_001 | User is on Profile page | Password not changed | Open Change Password and enter incorrect current password | Appropriate validation message should be displayed | <img width="442" height="526" alt="image" src="https://github.com/user-attachments/assets/94384b59-a6d6-4659-8588-c9cde84cca8b" />| | |
| TC_PROFILE_NEG_002 | User is on Change Password page | Password not changed | Leave required password fields blank and submit | Required field validation messages should appear |<img width="453" height="555" alt="image" src="https://github.com/user-attachments/assets/d7fe3b83-9487-450d-bf08-3603f25965ff" /> | | |
| TC_PROFILE_NEG_003 | User is on Change Password page | Password not changed | Enter mismatched New Password and Confirm Password | System should display password mismatch validation |<img width="492" height="567" alt="image" src="https://github.com/user-attachments/assets/f2aa9aa7-8929-4afa-9420-15f320bc08df" /> | | |
| TC_PROFILE_NEG_004 | User is on Profile page | Download prevented | Attempt to download profile when server is unavailable | Appropriate error message should be displayed | | | |
| TC_PROFILE_NEG_005 | User session has expired | User redirected | Click Download Profile or Change Password after session timeout | User should be redirected to Login page or shown a session expired message | | | |
| TC_PROFILE_NEG_006 | Delete confirmation displayed | Account not deleted | Click Delete Account then Cancel | Account should remain active |<img width="591" height="310" alt="image" src="https://github.com/user-attachments/assets/4a08726a-c20d-461a-9f90-beebb99f2ac0" /> <img width="835" height="591" alt="image" src="https://github.com/user-attachments/assets/e7e6e478-0118-4fbb-8a4e-910ecd3e929b" /> | | |
| TC_PROFILE_NEG_007 | Delete confirmation displayed | Account not deleted | Close Delete Account confirmation without confirming | No changes should occur | | | |
| TC_PROFILE_NEG_008 | User loses internet connection | Request fails gracefully | Attempt to download profile or change password while offline | Appropriate network error message should be displayed | | | |
| TC_PROFILE_NEG_009 | User is on Profile page | Invalid action prevented | Rapidly click Download Profile multiple times | System should prevent duplicate download requests | | | |
| TC_PROFILE_NEG_010 | User is on Profile page | Invalid export selection prevented | Attempt to save without selecting a valid export format (if applicable) | System should display validation or retain previous selection | | | |

# Profile Page - Edge Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC_PROFILE_EDGE_001 | User is on Profile page | Export preference retained | Change default export format, log out, log back in | Selected export format should persist | | | |
| TC_PROFILE_EDGE_002 | User is on Profile page | Download works repeatedly | Download profile multiple times consecutively | Every download should complete successfully | | | |
| TC_PROFILE_EDGE_003 | User has long profile information | UI remains intact | Verify page with long First Name/Last Name values | Profile layout should remain readable without UI issues | | | |
| TC_PROFILE_EDGE_004 | User has special characters in profile | Information displayed correctly | Verify account information containing special characters | Special characters should display correctly | | | |
| TC_PROFILE_EDGE_005 | User changes export format repeatedly | Latest selection saved | Switch between CSV and XLSX multiple times | Last selected format should remain saved | | | |
| TC_PROFILE_EDGE_006 | User refreshes page | Data retained | Refresh browser while on Profile page | Profile information should reload correctly | | | |
| TC_PROFILE_EDGE_007 | User opens Profile in multiple tabs | Data remains synchronized | Change export format in one tab and refresh another | Latest saved settings should be displayed | | | |
| TC_PROFILE_EDGE_008 | Delete confirmation displayed | Confirmation behavior verified | Click Delete Account multiple times rapidly | Only one confirmation dialog should appear | | | |
| TC_PROFILE_EDGE_009 | User is on Profile page | Browser navigation verified | Navigate away and return using browser Back button | Profile page should display correctly without errors | | | |
| TC_PROFILE_EDGE_010 | User signs out from multiple tabs | Session invalidated | Sign out in one tab and refresh another | User should be redirected to Login page in all tabs | | | |
