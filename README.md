# Dataclenz-Manul-Testing

## Manual Test Cases for DataClenz Web Application

This document provides focused manual test cases for the core user journeys of the DataClenz web application.

## Test Scope

- Authentication and session handling
- File upload and data ingestion
- Data profiling, validation, and transformation
- Duplicate handling and cleansing workflows
- Export and download flows
- Usability, access control, and error handling

## Test Environment

- Supported browser: Chrome / Edge / Firefox (latest stable)
- Stable internet connection
- Valid test user accounts:
  - Admin user
  - Standard business user
- Test data files:
  - Valid CSV file
  - Valid Excel file
  - Invalid/corrupted file
  - File with missing mandatory fields
  - File with duplicate records
  - Large file within supported size limit

## Manual Test Cases

| TC ID | Module | Test Scenario | Preconditions | Steps | Expected Result |
| --- | --- | --- | --- | --- | --- |
| DC-001 | Login | Login with valid credentials | User is registered and active | 1. Open login page.<br>2. Enter valid email and password.<br>3. Click **Login**. | User is logged in successfully and redirected to the dashboard/home page. |
| DC-002 | Login | Login with invalid password | Registered user exists | 1. Open login page.<br>2. Enter valid email and invalid password.<br>3. Click **Login**. | Login is blocked and a clear error message is displayed. |
| DC-003 | Login | Required field validation on login | None | 1. Open login page.<br>2. Leave email and password blank.<br>3. Click **Login**. | Required field validation messages are shown and login does not proceed. |
| DC-004 | Session | Logout from active session | User is logged in | 1. Click profile/account menu.<br>2. Click **Logout**. | User session ends and user is redirected to login page. |
| DC-005 | Session | Back-button behavior after logout | User has logged out | 1. Log out.<br>2. Press browser back button. | Application does not reopen a protected page without re-authentication. |
| DC-006 | Upload | Upload valid CSV file | User is logged in and upload page is accessible | 1. Navigate to upload/import page.<br>2. Select a valid CSV file.<br>3. Start upload. | File uploads successfully and appears in the processing workspace/list. |
| DC-007 | Upload | Upload valid Excel file | User is logged in | 1. Navigate to upload/import page.<br>2. Select a valid Excel file.<br>3. Start upload. | Excel file uploads successfully and is accepted by the system. |
| DC-008 | Upload | Reject unsupported or corrupted file | User is logged in | 1. Navigate to upload/import page.<br>2. Select unsupported/corrupted file.<br>3. Start upload. | Upload is rejected with an informative validation/error message. |
| DC-009 | Upload | Upload file with missing mandatory columns | Validation rules or required schema is defined | 1. Upload a file missing mandatory fields.<br>2. Continue to validation/preview. | Missing-field errors are shown and the user can identify what needs correction. |
| DC-010 | Upload | Upload large file within allowed limit | Large supported test file is available | 1. Upload a large valid file.<br>2. Wait for processing to complete. | File is uploaded and processed successfully without UI breakage or browser freeze. |
| DC-011 | Preview | Verify uploaded data preview | Valid file has been uploaded | 1. Open uploaded dataset preview.<br>2. Compare rows/columns with source file. | Preview displays correct column names, row values, and record counts. |
| DC-012 | Mapping | Map source columns to expected fields | Uploaded file requires field mapping | 1. Open mapping screen.<br>2. Map source columns to target fields.<br>3. Save mapping. | Mapping is saved successfully and reflected in subsequent processing. |
| DC-013 | Validation | Run data validation rules | Uploaded dataset is available | 1. Open validation/rules page.<br>2. Start validation. | Validation executes successfully and identifies invalid or incomplete records accurately. |
| DC-014 | Validation | Display row-level validation messages | File contains invalid records | 1. Run validation on file with invalid data.<br>2. Open error details. | System shows row-level or field-level issues clearly for user review. |
| DC-015 | Transformation | Apply standard cleansing/formatting rules | Dataset is uploaded and configurable | 1. Choose transformation/cleansing rules.<br>2. Run transformation. | Data is transformed successfully based on configured rules. |
| DC-016 | Transformation | Verify trimming/standardization output | Dataset includes inconsistent casing/spaces/formats | 1. Process dataset with standardization rules.<br>2. Review output. | Output reflects expected formatting changes such as trimmed spaces or normalized values. |
| DC-017 | Duplicates | Detect duplicate records | Dataset with duplicates is available | 1. Upload file containing duplicate records.<br>2. Run duplicate detection. | Duplicate records are identified correctly and surfaced to the user. |
| DC-018 | Duplicates | Resolve/remove duplicate records | Duplicate results are shown | 1. Review duplicate list.<br>2. Apply available merge/remove/resolution action.<br>3. Save changes. | Duplicate resolution is applied correctly and final dataset is updated. |
| DC-019 | Processing | Re-run processing after corrections | Dataset contains fixable issues | 1. Correct mapping/rule selection or source values if supported.<br>2. Re-run processing. | Process completes successfully and previously identified valid corrections are reflected. |
| DC-020 | Export | Export cleaned data to supported format | Dataset has completed processing | 1. Open processed dataset.<br>2. Click export/download.<br>3. Select supported format if prompted. | Cleaned dataset downloads successfully and file content matches processed output. |
| DC-021 | Export | Verify exported file accuracy | Exported file is available | 1. Open downloaded file.<br>2. Compare records with processed data in application. | Exported file contains expected rows, columns, and transformed values. |
| DC-022 | Access Control | Standard user access to authorized modules only | Standard user account exists | 1. Log in as standard user.<br>2. Browse available menus/pages. | User can access allowed modules only; restricted pages/actions are hidden or denied safely. |
| DC-023 | Access Control | Admin access to admin-only functions | Admin account exists | 1. Log in as admin.<br>2. Open administration/configuration areas. | Admin user can access admin functions without errors. |
| DC-024 | Error Handling | User-friendly message for processing failure | Use invalid or conflicting input | 1. Trigger a known processing failure.<br>2. Observe response. | System shows a clear, non-technical error message and remains usable. |
| DC-025 | Usability | Browser refresh during active workflow | Dataset is uploaded or processing has completed | 1. Open active workflow page.<br>2. Refresh browser. | Page reloads safely and preserves/recovers saved state as expected. |
| DC-026 | Navigation | Move between upload, validation, and output pages | User is logged in and dataset exists | 1. Navigate across key workflow pages using menus/buttons.<br>2. Return to previous step. | Navigation works correctly without broken links or unexpected data loss. |
| DC-027 | Security | Direct URL access to protected page without login | User is logged out | 1. Copy a protected page URL.<br>2. Open it in logged-out state. | User is redirected to login page or denied access appropriately. |
| DC-028 | Compatibility | Verify core workflow on supported browsers | Supported browsers are available | 1. Repeat login, upload, process, and export flow in each browser. | Core workflow works consistently across supported browsers. |

## Exit Criteria

- Critical user journeys (login, upload, validate, process, export) pass
- No blocker or critical severity defects remain open
- Validation and error messages are understandable for business users
- Access control works correctly for both admin and standard users

## Notes

- Execute these test cases using business-relevant sample files wherever possible.
- Capture screenshots for failed cases to support defect reporting and retesting.
