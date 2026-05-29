# Verify user can Sign-in with valid credentials

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC01 | User account exists | User is redirected to DataFlows page | Open Dataclenz (localhost)     Click Sign-in                Enter email: abc@yopmail.com                               Enter password: Test1234!                                Click Sign-in | User should successfully log in and be redirected to DataFlows page Dashboard page should display  | NA | NA |


# Verify user can create account with valid credentials

| Test Case ID | Precondition | Postcondition | Steps | Expected Result | Screenshot | Logs |
|--------------|--------------|---------------|-------|-----------------|------------|------|
| TC02 | User should have application aceess to create account | User should be able to create account successfully | Open Dataclenz (localhost)     FirstName: Data                LastName: Test                               Enter password: Test1234!             Confirm Password: Test1234!                    EmailId: Dctest@yopmail.com          Click Sign-up | User should successfully sign up and redirected to sign in page  |  <img width="423" height="646" alt="image" src="https://github.com/user-attachments/assets/1deb5362-2df7-4833-a6ad-7551251b8023" />       <img width="460" height="471" alt="image" src="https://github.com/user-attachments/assets/68d25abe-812c-4978-a4ae-9605c68e4e3b" />

