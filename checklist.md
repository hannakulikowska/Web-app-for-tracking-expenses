### Description:
While completing the task, I followed the principle of creating test scenarios based on the requirements. In my understanding, test scenarios include test cases, which, in turn, consist of an ID, a name, steps, input data and expected result. An example test case is provided below:

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

# T1. Сreating an account to track expenses
   
1. Verify that an account can be created with USD, EUR or BYN currency by clicking the "Add Account" button on the Main page.
1. Verify that an account cannot be created with two currencies selected simultaneously.
1. Verify that an account cannot be created if the Currency field is left empty.
1. Verify that an account cannot be created if both the Name and Currency fields are left empty.
1. Verify the application's behavior on the boundary value of the 0-caracter name length (0, 1, 100, 101 characters). There should be a message that the name field cannot be empty. /Not included in requirements/
1. Verify the application's behavior on the boundary value of the 1-caracter name length. 
1. Verify the application's behavior on the boundary value of the 100-caracters name length. 
1. Verify the application's behavior on the boundary value of the 101-caracters name length. There should be a message that the name field cannot be more than 100 chars. /Not included in requirements/
1. Verify that an account can be created with special characters in the name.
1. Verify that a maximum of 20 accounts can be created.
1. Verify that 21 accounts cannot be created.
1. Verify that an account cannot be marked as Default when there is only one account. /Not included in requirements/
1. Verify that one of the accounts can be marked as Default when there are at least two accounts. 
1. Verify that two accounts cannot be marked as Default at the same time.
1. Verify that the Default account can be changed to another Default account.
1. Verify that the Default account can be unmarked as Default.
1. Verify that none of the accounts can be set as Default. /Not included in requirements/
1. Verify that the currency of an account can be changed to another currency. /Question below/

# T2. Creating categories & sub-categories to differentiate expenses
   
1. Verify that a category can be created with a name length of 1 character on the Categories page.
1. Verify that a category can be created with a name length of 50 characters.
1. Verify that a category cannot be created with a name length of 0 characters. /Not included in requirements/
1. Verify that a category cannot be created with a name length of 51 characters.
1. Verify that a category cannot have 0 subcategories.
1. Verify that unlimited numbers of categories can be created. /Not included in requirements/
1. Verify that a category can have unlimited numbers of subcategories. /Not included in requirements/
1. Verify that a subcategory cannot be created with a name length of 0 characters. /Not included in requirements/
1. Verify that a subcategory can be created with a name length of 1 character.
1. Verify that a subcategory can be created with a name length of 50 characters.
1. Verify that a subcategory cannot be created with a name length of 51 characters.
1. Verify that a category and subcategory with maximum name length appear correctly.
1. Verify that categories and sub-categories have unique names.
1. Verify that all created categories and subcategories are visible on the Categories page. /Not included in requirements/

# T3. Adding expense records
   
1. Verify that the amount is added in the currency of the account.
1. Verify that 0 cannot be added as the amount of the expense.
1. Verify that negative whole numbers can be added as the amount of expenses.
1. Verify that negative decimal numbers can be added as the amount of expenses. /Question below/
1. Verify that positive numbers cannot be added as the amount of an expense and they are automatically replaced with negative numbers.
1. Verify that the amount -1 000 000 000 000 can be added. /Question below/
1. Verify that the amount -1 000 000 000 001 cannot be added. /Question below/
1. Verify that the system responds correctly to spaces, dots, or commas when entering the amount. /Not included in requirements/
1. Verify that the system responds correctly to incorrect amounts entered, such as special characters, letters or a zero at the beginning.
1. Verify that the pre-filled fields contain the current date and time. /In the Default account only?/
1. Verify that the time is in the 24h format.
1. Verify that a future date cannot be added.
1. Verify the application's behavior on the boundary values of the optional text field (0, 1, 100, 101 characters).
1. Verify that an existing category can be selected for the expense record.
1. Verify that the total amount of expenses is correct on the Main page.
1. Verify that unlimited numbers of expense records can be added. /Not included in requirements/

# T4. Renaming a category or a subcategory 

1. Verify that an existing category can be renamed and latest name will be shown in previous expense records.
1. Verify that a subcategory can be renamed and latest name will be shown in previous expense records.
1. Verify that an existing category and subcategory can be renamed and latest names will be shown in previous expense records.

# T5. Deleting categories and subcategories

1. Verify that an existing category can be deleted if it's subcategories have not been used in previous records.
1. Verify that when deleting a category with subcategories that were used in records, a pop-up window with the message "Please remove sub-categories first" is displayed. /Question below/
1. Verify that an existing subcategory can be deleted if it has not been used in previous records.
1. Verify that when deleting a subcategory that was used in records, a pop-up window with a message is displayed. /Question below/
1. Verify that another subcategory can be selected when deleting a subcategory that was used in records.

# T6. Updating an existing expense record

1. Verify that the account, amount, category (?), subcategory, date & time and note of an existing expense record can be edited. /Question below/
1. Verify that after editing an expense record, the total expense amounts for accounts are recalculated and updated across the system.

# T7. Deleting an existing expense record

1. Verify that an existing expense record can be successfully deleted.
1. Verify that after deleting an expense record, the total amount of expenses is recalculated and updated accordingly.

# T8. Integration with a bank account to automatically add expense records based on transactions

1. Verify that integration with BANK1 can be added by clicking "Add new bank integration" on the Bank integration page and successfully authorizing the account.
1. Verify that integration with BANK2 can be added by clicking "Add new bank integration" on the Bank integration page and successfully authorizing the account.
1. Verify that a bank account can be selected after authorization.
1. Verify that a bank account can be reselected.
1. Verify that a multiple currency bank account can be selected.
1. Verify that an expense account can be selected for each bank account.
1. Verify that an expense account can be reselected.
1. Verify that integration with BANK3 cannot be added.
1. Verify that expense accounts have the same currency as the integrated bank accounts.
1. Verify that integration with BANK1 and/or BANK2 cannot be added if the currency is not relevant to the application.
1. Verify that integration of the same expense account with BANK1 and BANK2 simultaneously is not possible, even if the currencies are the same (USD, EUR, or BYN).
1. Verify that expense records are created for transactions with negative amounts.
1. Verify that income records from a bank account are not included in the application.
1. Verify that expense records are created starting from the day of adding the bank integration.
1. Verify that expense records are created daily at 01:00 for transactions from the previous day. /Question below/
1. Verify that subcategories are automatically and correctly added for expense records from a bank integration.
1. Verify that subcategories are correctly integrated with previously created subcategories before integrating with the bank account.
1. Verify that the time of creating expense records meets the requirements. /Question below/
1. Verify that all bank integrations are visible on the Bank integrations page. /Not added to requirements/
1. Verify that a category can be edited for bank expense records. /Not added to requirements/
1. Verify that a subcategory can be edited for bank expense records.
1. Verify that amount can be edited for bank expense records.
1. Verify that date&time can be edited for bank expense records.
1. Verify that note can be edited for bank expense records.
1. Verify that the total amount of expenses is correct.
1. Verify that an expense account can be changed in the bank integration, and all existing transactions will be linked to the latest selected account.
1. Verify that an expense account cannot be changed in the bank integration if it is not in the relevant currency with the application.
1. Verify that an expense record added through integration can be deleted.

# T9. Deleting an integration with a bank account

1. Verify that a specific bank account in the bank integration can be selected and deleted.
1. Verify that all bank accounts in the bank integration can be deleted.
1. Verify that all created expense records can be retained during integration removal.
1. Verify that all created expense records can be deleted during integration removal.

# T10. Viewing expenses

1. Verify that all created accounts are visible on the Main page.
1. Verify that recent expense records are visible on the Main page. /Question below/
1. Verify that account name, currency and total amount spent (negative number) in the current month are shown for each account on the Main page.
1. Verify that an expense record can be added by clicking the Add Expense button on the Main Page.
1. Verify that there amount, category (?), subcategory, note and date&time for each expense on the Expenses page. /Question below/
1. Verify that all expenses for the current month are displayed on the Expenses page.
1. Verify that Month and Year options are available to select previous periods of expenses on the Expenses page.
1. Verify that it is not possible to select future periods of expenses.
1. Verify that it is possible to edit an expense record by clicking Edit.
1. Verify that it is possible to delete an expense record by clicking Delete.
1. Verify that it is possible to delete all expense records.

# T11. Viewing a pie chart of expenses by categories for a month

1. Verify that the Report page opens when clicking on "Report" in the menu.
1. Verify that the pie chart on the Report page displays expenses by categories for the default account for the current month.
1. Verify that it is possible to switch accounts on the Report page, and after switching, the pie chart and break-down show expenses for the selected account.
1. Verify that it is possible to switch the month on the Report page, and after switching, the pie chart and break-down show expenses by categories for the selected month.
1. Verify that it is possible to switch the year for a month on the Report page, and after switching, the pie chart and break-down show expenses by categories for the selected month of the selected year. /Not added to requirements/
1. Verify that break-down of expenses for the current month by categories displays in both percentage and total sum spent in the specific currency.
1. Verify that the total amount for the selected month is correct on the Report page for each account.
1. Verify that the currency displayed in the monthly report is correct.
1. Verify that the total amount for each category for the selected month is correct.
1. Verify that the total amount for each subcategory for the selected month is correct.
1. Verify that the percentage for each category for the selected month is correct.
1. Verify that the percentage for each subcategory for the selected month is correct.
1. Verify that the sum of all percentages for the month's expenses equals 100%.
1. Verify that clicking on a selected category displays expenses by subcategories for selected current month.
1. Verify that clicking on a selected category displays expenses by subcategories for selected earlier month.
1. Verify that clicking on a category displays expenses by subcategories for a selected month of previous years.

# T12. Viewing a pie chart of expenses by categories for a year.

1. Verify that after switching the period to a year on the Report page, the pie chart and break-down display expenses by categories for the default account for the current year.
1. Verify that the break-down displays expenses for the current year by categories in both percentage and total sum spent in the specific currency.
1. Verify that it is possible to switch the year on the Report page and after switching the pie chart and break-down show expenses by categories for the selected year.
1. Verify that the total amount for the selected year is correct on the Report page.
1. Verify that the currency displayed in the yearly report is correct.
1. Verify that the total amount for each category for the selected year is correct.
1. Verify that the total amount for each subcategory for the selected year is correct.
1. Verify that the percentage for each category for the selected year is correct.
1. Verify that the percentage for each subcategory for the selected year is correct.
1. Verify that the sum of all percentages for the year's expenses equals 100%.
1. Verify that clicking on a selected category displays expenses by subcategories for the current year.
1. Verify that clicking on a selected category displays expenses by subcategories for selected year.
