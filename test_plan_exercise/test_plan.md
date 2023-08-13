# Manual EXERCISE  
  
## Thank you for taking the time to do an interview with us, in the following document you have different requirements to solve some questions we would like to evaluate. Please, send us back the solution once you have finished.
  
  
### We are working in a new app called HolidaysToMiami, and the first scenario we must cover is **Registration **Requirements**.

### 1. From the companFirst time users open the app, they need to register into the app by filling in these fields and requirements:  

- FIRST NAME* (10 chars max)
- LAST NAME* (60 chars max)
- ADDRESS 1 (120 numbers and chars)
- ADDRESS 2 (120 numbers and chars)
- DATE OF BIRTH* (YYYY-MM-DD, only numbers)
- USER NAME* (10 chars max. no especial chars)
- PASSWORD* (8 to 14 chars max. Must include uppercase and lowercase
letters, a especial char and numbers)
- REPEAT PASSWORD*

**Note**: identifies all mandatory fields.

### 2. If a mandatory field is sent empty in the registration process, it should display an error message: “Registration process went wrong, we need all mandatory information”.
  
  
### 3. If a field is not properly written as requirement, it should display an error message: “Registration process went wrong, please, review all information sent”.  
  
### 4. Once the user has completed their registration, they can login into the app using their USER NAME and Password
- If USER NAME, password or both are incorrect, it should display an error message: “We can’t recognize you, sorry, try it again.”
  
  
## **Questions:**  
  
### 1. Considering all previous requirements, do the Test Plan (cover as many scenarios as you can, including main validations)

[Test Plan](./test_plan_deliverable.md)


### 2. Once Test Plan is done and testing has started, you find an error. What should you do?
### 3. In the process of USER NAME validation, you discover it accepts more than 10 chars. What kind of information would you include in the defect report?
### 4. What’s the defect life cycle? Differences between bug and defect?
### 5. Imagine that now you want to automate some test cases of your Test Plan. Could you describe the steps you have to do to have your repository ready and what’s the workflow you’d follow to open a pull request with the new test cases in GitHub?