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

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot |
| --- | --- | --- | --- | --- | --- |
| FP_001 | User is on Sign In page | User is redirected to Forgot Password page | 1. Open Sign In page<br>2. Click Forgot Password | Forgot Password page is displayed successfully | <img width="475" height="114" alt="image" src="https://github.com/user-attachments/assets/d1440228-9f73-413e-bd45-ed4f9b8fefe0" />
|
| FP_002 | User is on Forgot Password page | Password reset email is sent | 1. Enter valid registered email<br>2. Click Submit | Success message is displayed and reset email is sent |<img width="463" height="327" alt="image" src="https://github.com/user-attachments/assets/8f20c4a3-2d7a-4b4d-bec2-eb2abd8699f8" />
 |
| FP_003 | User is on Forgot Password page | No password reset email is sent | 1. Enter unregistered email<br>2. Click Submit | Appropriate error message is displayed | |
| FP_004 | User is on Forgot Password page | Validation message is displayed | 1. Enter invalid email format<br>2. Click Submit | Email format validation message is shown | <img width="471" height="486" alt="image" src="https://github.com/user-attachments/assets/c6fc08b2-f52d-4d0e-88c6-4159fc404a98" />
 |
| FP_005 | User is on Forgot Password page | Validation message is displayed | 1. Leave email field blank<br>2. Click Submit | Required field validation message is shown | |
| FP_006 | User has received a reset email | User is redirected to Reset Password page | 1. Open password reset email<br>2. Click reset link | Reset Password page is displayed | |
| FP_007 | User is on Reset Password page | Password is updated successfully | 1. Enter new password<br>2. Enter confirm password<br>3. Click Save | Password reset is successful | |
| FP_008 | User is on Reset Password page | Password is not updated | 1. Enter different values in Password and Confirm Password<br>2. Click Save | Password mismatch validation message is displayed | |
| FP_009 | Password has been reset successfully | User logs in successfully | 1. Navigate to Sign In page<br>2. Enter new password<br>3. Click Sign In | User is logged in successfully | |
| FP_010 | Password has been reset successfully | Login fails with old password | 1. Navigate to Sign In page<br>2. Enter old password<br>3. Click Sign In | Login is unsuccessful and an appropriate error message is displayed | |
