# "Expensee" is a new web application being developed for expense tracking. 

The requirements for this application can be found in the "__requirements.md__" file. 

The "__checklist.md__" file contains a list of test scenarios that cover these requirements and have been designed based on my own experience and understanding of the system.


### Description:
While completing the task, I followed the principle of creating test scenarios based on the requirements. In my understanding, test scenarios include test cases, which, in turn, consist of an ID, a name, preconditions, steps, input data and expected result. An example test case is provided below:

```
Test Scenario 1: Account creation to track expenses.

Test cases:

1.1. Creating an expense account with a valid currency and a valid name.

Preconditions:
Open the web application "Expensee" in a specific browser on a specific device.

Steps:
1. Click the Add Account button on the Main page.
2. Select currency.
3. Enter an account name.
4. Create an account.

Input data:
A. Currency: USD.
   Name: USD Account.
B. Currency: EUR.
   Name: EUR Account.
C. Currency: BYN.
   Name: BYN Account.

Expected result:
Account with a valid name in a specific currency is created.
```

In this test case, it is unknown what specific actions need to be taken to complete steps 2 and 4. Additionally, it is unknown in which browsers and on which devices the application will be tested.

Since there are still many questions to clarify based on this version of the user stories, I have decided at this stage to compile a list of what needs to be tested in the web application and a list of questions.

In the assignment, I focused primarily on functional testing. During further testing of the web application, non-functional testing is also conducted, which includes performance, reliability, adaptability and other non-functional aspects of the software system.

#
Test cases and bug reports for another web application testing project can be seen in [the "Testing To Do List App" repository.](https://github.com/hannakulikowska/Testing-To-Do-List-app)
