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
