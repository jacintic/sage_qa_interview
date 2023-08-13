# Test Plan  
## Strategy  
This purpose of this Test Plan is to ensure the quality of the App called **Holidays to Miami**.  
To keep this document structured it will present 2 main categories. **Register** and **Login**.  
  
## Schedule, estimation and deliverables  
This process will be performed in a full sprint (2 weeks), with a realistic estimation of half a spring (1 week).  
The results of this plan, will be delivered through JIRA Xray Testing suite. The Test Plans will be detailed there, the Test Cases will be linked in the Test Plan, and finally the Test Execution Results will be displayed in the same structure (Visible in the Test Plan document).  
The Testing Approaches will be 3 types of testing:  
1. API Unit Tests
2. Manual UI testing 
3. End to End Testing
Automated Testing Solutions will be decided by the Team Assigned to this project.
  
## Resources required  
For this task, there will be 1 member from the Product Owners team that will provide the project requirements and will follow the process of this project. 2 QA members in charge of Testing and the Tech Lead, and a Senior Dev from the Dev team.  
The journey will start with a meeting between all of the Project Members. There they will decide the Project's duration, the resources required (for example, more Dev members will be required to provide the App being tested), and the Testing Software solutions to employ. For example, they might want to use Cypress for End to End Testing.  
Every monday there will be a meeting where the process of the project will be monitored and handled accordingly.
  
  
# Register, Test Cases  
0. Basic Requirements
   1. It should
      1. have Front End solution do the following
         1. Each field that is required marked with an asterisk
         2. A clear message near the Submit button explaining that the (*) fields are required
         3. All fields with validation must have a toggable "validation requirements" small button underneath the field clearly explaining the validation rules that apply to the field
      2. API/Back End should have rules for required and validation and proper response messages 
1. Register with Empty Data
   1. It should 
      1. have Front End solution do the following
         1. avoid submitting the te form
         2. report mandatory fields with 
            1. UI field highlighting
            2. Error message explaining that the field is required
      2. API should 
         1. return a status on the 400 range
         2. return an error message saying all fields are empty
2. Register with all required (correct) fields except one
   1. It should
      1. Front End part
         1. avoid submitting the form
         2. report the mandatory field with
            1. UI field highlighting
            2. Error message explaining that the field is required
      2. API should 
         1. return a status on the 400 range
         2. return an error message naming the required field
3. Register with the required fields but with validation errors **REPEAT FOR EACH FIELD WITH VALIDATION**
   1. It should
      1. Front End part
         1. avoid submitting the form
         2. report the validation error fields with
            1. UI field highlighting
            2. Error message explaining the validation rules that apply and why they failed
   2. API should
      1. return a status on the 400 range
      2. return an error message naming the required, the validation rules it failed and why it failed
4. Register with all required (correct) fields except 3 of them with validation errors
   1. It should
      1. Front End part
         1. avoid submitting the form
         2. report the validation error fields with
            1. UI field highlighting
            2. Error message explaining the validation rules that apply and why they failed
   2. API should
      1. return a status on the 400 range
      2. return an error message naming the required, the validation rules it failed and why it failed
      3. ensure that all fields that failed are listed with their proper explanation of the error
5. Register with all required (correct) fields, but a few validation error in a non required field
   1. It should
     1. Front End part
        1. avoid submitting the form
          1. report the validation error field with
             1. UI field highlighting
             1. Error message explaining the validation rules that apply and why they failed
   2. API should
      1. return a status on the 400 range
      2. return an error message naming the required, the validation rules it failed and why it failed
      3. ensure that all fields that failed are listed with their proper explanation of the error
6. Register with all required (correct) fields, non required fields empty
   1. It should
      1. Front End part
         1. load the Login page
         2. display a highlighted UI block element with the title "Register process complete!
         3. the UI element should be clearly standing out from the login page visually
         4. the UI element should provide an option to close it
      2. API should
         1. response with a 201 code for successfully created
7.  Register with all required (correct) fields, non required fields too.
    1. It should
      1. Front End part
        1. load the Login page
        2. display a highlighted UI block element with the title "Register process complete!
        3. the UI element should be clearly standing out from the login page visually
        4. the UI element should provide an option to close it
      2. API should
        1. response with a 201 code for successfully created

# Login, Test Cases  
0. Basic Requirements
   1. It should
     1. have Front End solution do the following
        1. provide clear instruction in the UI, like for example "enter credentials to login" or "enter user and password to login"
   2. API/Back End should 
      1. avoid error responses detailing which specific field was not found or with errors
1. Sending empty form
   1. It should 
      1. have Front End solution do the following
         1. avoid submitting the te form
         2. report mandatory fields with 
            1. UI field highlighting
            2. Error message explaining that the field is required
      2. API should 
         1. return a status on the 400 range
         2. return an error message saying credentials are empty
2. Sending form with only USERNAME
   1. It should 
      1. have Front End solution do the following
      2. avoid submitting the te form
      3. report mandatory fields with 
         1. UI field highlighting
         2. Error message explaining that the field is required
   2. API should 
      1. return a status on the 400 range
      2. return an error message saying password is required
3. Sending from with only PASSWORD
   1. It should 
      1. have Front End solution do the following
      2. avoid submitting the te form
      3. report mandatory fields with 
         1. UI field highlighting
         2. Error message explaining that the field is required
   2. API should 
      1. return a status on the 400 range
      2. return an error message saying username is required
4. Sending from with wrong **USERNAME**
   1. It should 
      1. have Front End solution do the following
      2. credentials error with 
         1. UI elments highlighting 
         2. Error message simply stating "wrong credentials", to avoid specifying which field is right or wrong (basic security measure)
   2. API should 
      1. return a status on the 400 range
      2. return an error message saying "wrong credentials"
5. Sending from with wrong **PASSWORD**
   1. It should 
      1. have Front End solution do the following
      2. credentials error with 
         1. UI elments highlighting 
         2. Error message simply stating "wrong credentials", to avoid specifying which field is right or wrong (basic security measure)
   2. API should 
      1. return a status on the 400 range
      2. return an error message saying "wrong credentials" 
6. Sending from with both correct credentials 
   1. It should
      1. Front End part
         1. load the Home page
         2. display a highlighted UI block element with the title "Login successful!"
         3. the UI element should be clearly standing out from the Home page visually
         4. the UI element should provide an option to close it
            1. consider if the UI element should fade away from visibility once a countdown has been reached to avoid residual elements in UI
   2. API should
      1. response within a 200 range code for successfully Logged In