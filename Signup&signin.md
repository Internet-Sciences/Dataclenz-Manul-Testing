# Verify user can Sign-in with valid credentials

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC01 | User account exists | User is redirected to DataFlows page | Open Dataclenz (localhost)     Click Sign-in                Enter email: abc@yopmail.com                               Enter password: Test1234!                                Click Sign-in | User should successfully log in and be redirected to DataFlows page Dashboard page should display  | <img width="451" height="472" alt="image" src="https://github.com/user-attachments/assets/12db4620-5edc-4f3c-93b2-925929e396ee" />        <img width="1889" height="752" alt="image" src="https://github.com/user-attachments/assets/ecfdea20-4d10-4be8-a99b-447d16720f07" />

 


# Verify user can create account with valid credentials

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC02 | User should have application aceess to create account | User should be able to create account successfully | Open Dataclenz (localhost)     FirstName: Data                LastName: Test                               Enter password: Test1234!             Confirm Password: Test1234!                    EmailId: Dctest@yopmail.com                                      Click Sign-up | User should successfully sign up and redirected to sign in page  |  <img width="423" height="646" alt="image" src="https://github.com/user-attachments/assets/1deb5362-2df7-4833-a6ad-7551251b8023" />       <img width="460" height="471" alt="image" src="https://github.com/user-attachments/assets/68d25abe-812c-4978-a4ae-9605c68e4e3b" />                       <img width="1889" height="752" alt="image" src="https://github.com/user-attachments/assets/977189f8-d351-4bf6-8094-3c70e9471b07" />



# Verify Sign-in with Incorrect Password

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC03 | User should have application aceess to Signin account | User should not be able to sign-in account with incorrect password | Open Dataclenz (localhost)                   EmailId: Dctest@yopmail.com     Password: Test1234!56                             Click Sign-up | User should receive message like Invalid Credentials and shoud see pop up message   |   <img width="400" height="526" alt="image" src="https://github.com/user-attachments/assets/ea52bff2-c339-44b9-b65b-543c85f47902" />



# Verify Sign-in with Incorrect EmailID

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC07 | User should have access to Sign In page | User should not be able to sign in with invalid email ID | Open Dataclenz (localhost), navigate to Sign In page, enter incorrect/unregistered Email ID, enter valid Password, click Sign In button | User should not be able to sign in. System should display error message like "Invalid email or password" and user should remain on Sign In page | ![IE_001](https://github.com/user-attachments/assets/14d8a3f9-a27b-40f0-b0ae-0b8c1d0304bb)
| TC08 | User should have access to Sign In page | User should not be able to sign in with badly formatted email | Open Dataclenz (localhost), navigate to Sign In page, enter invalid email format (example: test@), enter valid Password, click Sign In button | System should show validation message like "Enter a valid email address" and prevent login |  ![IE_001](https://github.com/user-attachments/assets/14d8a3f9-a27b-40f0-b0ae-0b8c1d0304bb)
| TC09 | User should have access to Sign In page | User should not be able to sign in with unregistered email ID | Open Dataclenz (localhost), navigate to Sign In page, enter unregistered Email ID, enter valid Password, click Sign In button | System should display error message like "User does not exist" or "Invalid credentials" and login should fail | 
           
           
           
           
    



# Verify Login with Only EmailId Filled

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC06 | User should have access to Sign In page | User should not be able to sign in with only Email filled | Open Dataclenz (localhost), navigate to Sign In page, enter Email ID: Dctest@gmail.com, leave Password field empty, click Sign In button | User should not be able to sign in. System should block login and display validation message like "Password is required" |  ![EF_001](https://github.com/user-attachments/assets/08ceed94-bf73-43ff-95ba-79fd709361aa)






# Verify Login with Only Password Filled

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC05 | User should have access to Sign In page | User should not be able to sign in with only Password filled | Open Dataclenz (localhost), navigate to Sign In page, enter only Password, leave Email field empty, click Sign In button | User should not be able to sign in. System should block login and display validation message like "Email is required" | ![PF_001](https://github.com/user-attachments/assets/723f0e90-9883-4cca-ad20-7953fad9c9cd)





# Forgot Password Test Cases

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| FP_001 | User is on Sign In page | User is redirected to Forgot Password page | 1. Open Sign In page<br>2. Click Forgot Password | Forgot Password page is displayed successfully | ![FP_001]( https://github.com/user-attachments/assets/18534993-e008-4deb-8314-aacf14a519f9 />
) |
| FP_002 | User is on Forgot Password page | Password reset email is sent | 1. Enter valid registered email<br>2. Click Submit | Success message is displayed and reset email is sent | ![FP_002](images/FP_002.png) |
| FP_003 | User is on Forgot Password page | No password reset email is sent | 1. Enter unregistered email<br>2. Click Submit | Appropriate error message is displayed | ![FP_003](images/FP_003.png) |
| FP_004 | User is on Forgot Password page | Validation message is displayed | 1. Enter invalid email format<br>2. Click Submit | Email format validation message is shown | ![FP_004](images/FP_004.png) |
| FP_005 | User is on Forgot Password page | Validation message is displayed | 1. Leave email field blank<br>2. Click Submit | Required field validation message is shown | ![FP_005](images/FP_005.png) |
| FP_006 | User has reset email | User is redirected to Reset Password page | 1. Open email<br>2. Click reset link | Reset Password page is displayed | ![FP_006](https://github.com/user-attachments/assets/90d11ce8-d64d-4c4a-9632-275a354bcaf6) |
| FP_007 | User is on Reset Password page | Password is updated successfully | 1. Enter new password<br>2. Enter confirm password<br>3. Click Save | Password reset is successful | ![FP_007](images/FP_007.png) |
| FP_008 | User is on Reset Password page | Password mismatch error | 1. Enter different passwords<br>2. Click Save | Password mismatch validation message | ![FP_008](https://github.com/user-attachments/assets/856df13f-4e58-401b-8bf7-8d64fc6818ff) |
| FP_009 | Password reset done | User logs in successfully | 1. Open Sign In page<br>2. Enter new password<br>3. Click Sign In | Login successful | ![FP_009](https://github.com/user-attachments/assets/b2d98526-bf1b-4e5b-9d2b-84cabd8f7d97) |
| FP_010 | Password reset done | Login fails with old password | 1. Open Sign In page<br>2. Enter old password<br>3. Click Sign In | Login fails with error | ![FP_010](https://github.com/user-attachments/assets/ab836c41-c32b-4590-9ebd-1c0ea798edce) |


# Verify Signin with unregistered email

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC10 | User should have access to Sign In page | User should not be able to sign in with unregistered email | Open Dataclenz (localhost), navigate to Sign In page, enter unregistered Email ID (example: testuser123@gmail.com), enter valid Password, click Sign In button | User should not be able to sign in. System should display an error message like "User does not exist" or "Invalid credentials". Login should be blocked and user should remain on Sign In page | ![TC10 Unregistered Email Validation](https://github.com/user-attachments/assets/a761f110-afab-41fa-b13e-f801066fcd5d) |

# Verify Signin with both fields empty

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC11 | User should have access to Sign In page | User should not be able to sign in with both fields empty | Open Dataclenz (localhost), navigate to Sign In page, leave Email field empty, leave Password field empty, click Sign In button | User should not be able to sign in. System should display validation messages like "Email is required" and "Password is required". Login should be blocked |   ![BFE_009](https://github.com/user-attachments/assets/31446fe2-5f2a-4043-9899-5b71750ea419)


# Verify Account Lock after Multiple Failed Login Attempts

| Test Case ID | Precondition | Postcondition | Test Steps | Expected Result | Screenshot | Status | Ticket |
|--------------|--------------|---------------|------------|-----------------|------------|--------|--------|
| TC12 | User should have a registered account in the system and access to Sign In page | User account should be locked after multiple failed login attempts | Open Dataclenz (localhost), navigate to Sign In page, enter valid Email ID with incorrect Password repeatedly (e.g., 5 consecutive attempts), click Sign In each time | After exceeding maximum allowed attempts, system should lock the account and display message like "Account locked due to multiple failed login attempts. Please try again later or reset password." User should not be able to log in even with correct password until account is unlocked |  ![MS_009](https://github.com/user-attachments/assets/699a8779-64de-4d6c-b5b8-da6871e9c0c7)
