# Verify user can Sign-in with valid credentials

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC01 | User account exists | User is redirected to DataFlows page | Open Dataclenz (localhost)     Click Sign-in                Enter email: abc@yopmail.com                               Enter password: Test1234!                                Click Sign-in | User should successfully log in and be redirected to DataFlows page Dashboard page should display  | <img width="451" height="472" alt="image" src="https://github.com/user-attachments/assets/12db4620-5edc-4f3c-93b2-925929e396ee" />        <img width="1889" height="752" alt="image" src="https://github.com/user-attachments/assets/ecfdea20-4d10-4be8-a99b-447d16720f07" />

 


# Verify user can create account with valid credentials

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC02 | User should have application aceess to create account | User should be able to create account successfully | Open Dataclenz (localhost)     FirstName: Data                LastName: Test                               Enter password: Test1234!             Confirm Password: Test1234!                    EmailId: Dctest@yopmail.com                                      Click Sign-up | User should successfully sign up and redirected to sign in page  |  <img width="423" height="646" alt="image" src="https://github.com/user-attachments/assets/1deb5362-2df7-4833-a6ad-7551251b8023" />       <img width="460" height="471" alt="image" src="https://github.com/user-attachments/assets/68d25abe-812c-4978-a4ae-9605c68e4e3b" />                       <img width="1889" height="752" alt="image" src="https://github.com/user-attachments/assets/977189f8-d351-4bf6-8094-3c70e9471b07" />



# Verify Sign-in with Incorrect Password

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC03 | User should have application aceess to Signin account | User should not be able to sign-in account with incorrect password | Open Dataclenz (localhost)                   EmailId: Dctest@yopmail.com     Password: Test1234!56                             Click Sign-up | User should receive message like Invalid Credentials and shoud see pop up message   |   <img width="400" height="526" alt="image" src="https://github.com/user-attachments/assets/ea52bff2-c339-44b9-b65b-543c85f47902" />



# Verify Sign-in with Incorrect EmailID

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC04 | User should have application aceess to Signin account | User should not be able to sign-in account with incorrect Emaild | Open Dataclenz (localhost)                   EmailId: Dctest34@yopmail.com     Password: Test1234!                             Click Sign-up | User should receive message like Invalid Credentials and shoud see pop up message   |             <img width="423" height="538" alt="image" src="https://github.com/user-attachments/assets/ff2d7205-6207-41a5-9a6a-08c0d798b087" />


# Verify Login with Only Password Filled

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC05 | User should have application aceess to Signin account | User should not be able to sign-in account with blank Emaild | Open Dataclenz (localhost)                   EmailId:      Password: Test1234!    |  User should not be able to signin account and should not be able to click on sign in button    |<img width="391" height="450" alt="image" src="https://github.com/user-attachments/assets/723f0e90-9883-4cca-ad20-7953fad9c9cd" />



# Verify Login with Only Email Filled

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC06 | User should have application aceess to Signin account | User should not be able to sign-in account with blank Password | Open Dataclenz (localhost)                   EmailId: Dctest@gmail.com     Password:     |  User should not be able to signin account and should not be able to click on sign in button  User can see message like password is required | <img width="422" height="476" alt="image" src="https://github.com/user-attachments/assets/242af6de-ecb2-4c27-a99a-d659246ccb48" />




# Verify Forgot Password Functionality

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC07 | User should have application aceess to Signin account. | User should not be able to sign-in account with blank Password |


# Forgot Password Test Cases

| Test Case ID | Test Scenario | Precondition | Test Steps | Expected Result |   Screenshots/video  |  Logs
|--------------|---------------|--------------|------------|-----------------|
| FP_001 | Verify Forgot Password link is available | User is on Sign In page | 1. Open Sign In page | Forgot Password link is visible and clickable |
| FP_002 | Verify navigation to Forgot Password page | User is on Sign In page | 1. Click Forgot Password link | User is redirected to Forgot Password page |
| FP_003 | Verify password reset with valid registered email | Registered user account exists | 1. Enter valid registered email<br>2. Click Submit | Password reset email is sent successfully |
| FP_007 | Verify email field accepts leading/trailing spaces | Registered user account exists | 1. Enter email with spaces<br>2. Click Submit | Spaces are trimmed and reset email is sent |
| FP_008 | Verify email field is case-insensitive | Registered user account exists | 1. Enter email in uppercase/lowercase<br>2. Click Submit | Reset email is sent successfully | <img width="462" height="318" alt="image" src="https://github.com/user-attachments/assets/487133e3-284b-4f73-8ad0-4a6cc999a9b6" />  |

| FP_009 | Verify reset email contains valid reset link | Password reset email received | 1. Open email<br>2. Click reset link | User is redirected to Reset Password page |     <img width="475" height="114" alt="image" src="https://github.com/user-attachments/assets/5fd1665e-101d-4245-af7a-05f0131420f3" />  |

| FP_010 | Verify reset link expires after configured time | Reset email received | 1. Wait until link expires<br>2. Click reset link | Expired link message is displayed |  <img width="1269" height="853" alt="image" src="https://github.com/user-attachments/assets/9e3d686d-0f87-405c-b738-833d9c6708b9" />
 

| FP_011 | Verify user can reset password with valid link | Valid reset link available | 1. Enter new password<br>2. Confirm password<br>3. Click Save | Password is updated successfully |
| FP_012 | Verify password and confirm password mismatch validation | User is on Reset Password page | 1. Enter different passwords<br>2. Click Save | Validation message is displayed |
| FP_013 | Verify password policy validation | User is on Reset Password page | 1. Enter invalid password<br>2. Click Save | Appropriate validation message is displayed |
| FP_014 | Verify successful login with new password | Password has been reset | 1. Login using new password | User logs in successfully |  <img width="1889" height="599" alt="image" src="https://github.com/user-attachments/assets/e6e9b255-0c40-4bff-958d-0d2c6007d71d" />   |

| FP_015 | Verify old password no longer works | Password has been reset | 1. Login using old password | Login fails with appropriate error |
| FP_016 | Verify reset link cannot be reused | Password already reset | 1. Open previously used reset link | Link is invalid and cannot be reused |
| FP_017 | Verify multiple password reset requests | Registered user account exists | 1. Request password reset multiple times | Latest reset link works successfully |
| FP_018 | Verify Submit button behavior | User is on Forgot Password page | 1. Enter valid email | Submit button is enabled and functional |
| FP_019 | Verify rate limiting/security protection | User is on Forgot Password page | 1. Submit multiple reset requests rapidly | System handles excessive requests securely |
| FP_020 | Verify success message after password reset request | Registered user account exists | 1. Enter valid email<br>2. Click Submit | Success confirmation message is displayed |
