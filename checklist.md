# T1. Сreating an account to track expenses
   
1. Verify that an account can be created with USD, EUR or BYN currency by clicking the "Add Account" button on the Main page.
1. Verify that an account cannot be created with two currencies selected simultaneously.
4. Verify that an account cannot be created if the Currency field is left empty.
5. Verify that an account cannot be created if both the Name and Currency fields are left empty.
6. Verify the application's behavior on the boundary value of the 0-character name length. There should be a message that the name field cannot be empty. /Not included in requirements/
7. Verify the application's behavior on the boundary value of the 1-character name length. 
8. Verify the application's behavior on the boundary value of the 100-characters name length. 
9. Verify the application's behavior on the boundary value of the 101-characters name length. There should be a message that the name field cannot be more than 100 chars. /Not included in requirements/
10. Verify that an account can be created with special characters in the name.
11. Verify that a maximum of 20 accounts can be created.
12. Verify that 21 accounts cannot be created.
1. Verify that all created accounts are visible on the Main page.
2. Verify that account name, currency and total amount spent (negative number) in the current month are shown for each account on the Main page.
3. Verify that account name, currency and total amount spent (negative number) in the current month are shown for each account on the Main page.

Notes:

- Should account names be unique? Test by creating two accounts with the same name.
- How are the accounts sorted on the Main page? Is it possible for users to change the order of the accounts?
- Can an account be created with a name consisting of only whitespace characters?
- What error message should be displayed if the account name field is left empty?
- What are the requirements for the exchange rate used to calculate the total amount for accounts in different currencies?
- There are no requirements regarding the deletion of an account. How can a user delete an account?
- How can a user delete an account that has been marked as Default? Are there any specific considerations for this scenario?
- What are the user registration requirements for the system? What login methods are available (email/phone/social media, etc.)? What information is required for registration (username, password, etc.)? How should the registration process look like?

# T2. Marking an account as Default

1. Verify that an account cannot be marked as Default when there is only one account. /Not included in requirements/
4. Verify that one of the accounts can be marked as Default when there are at least two accounts. 
5. Verify that two accounts cannot be marked as Default at the same time.
6. Verify that the Default account can be changed to another Default account.
7. Verify that the Default account can be unmarked as Default.
8. Verify that none of the accounts can be set as Default. /Not included in requirements/

Notes:

- What should happen if no accounts are marked as Default?
- Where is the Default account located on the Main page? 
- Where is the indication that an account is marked as Default?

# T3. Editing an account

1. Verify that the currency of an account can be changed to another currency after saving. /Not included in requirements/
2. Verify that the account name can be changed after saving. /Not included in requirements/

# T4. Creating categories & sub-categories to differentiate expenses
   
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
1. Verify that categories have unique names.
2. Verify that sub-categories have unique names.
3. Verify that category and subcategory can have the same name. /Not included in requirements/
4. Verify that all created categories and subcategories are visible on the Categories page. /Not included in requirements/

Notes:

- How will the requirement for creating a category with subcategories be implemented? The user stories state that a user can create a category and add a subcategory to an existing category, but the category cannot exist without subcategories. These requirements seem to contradict each other.
- It is not specified how and where the creation of categories and subcategories should take place.

# T5. Renaming a category or a subcategory 

1. Verify that an existing category can be renamed and latest name will be shown in previous expense records.
1. Verify that a subcategory can be renamed and latest name will be shown in previous expense records.
1. Verify that an existing category and subcategory can be renamed and latest names will be shown in previous expense records.
1. Verify the application's behavior on the boundary values of name field of category and subcategory (0, 1, 50, 51 characters).

# T6. Deleting categories and subcategories

1. Verify that an existing category can be deleted if it's subcategories have not been used in previous records.
1. Verify that when deleting a category with subcategories that were used in records, a pop-up window with the message "Please remove sub-categories first" is displayed. /Question below/
1. Verify that an existing subcategory can be deleted if it has not been used in previous records.
1. Verify that when deleting a subcategory that was used in records, a pop-up window with a message is displayed. /Question below/
1. Verify that another subcategory can be selected when deleting a subcategory that was used in records.

Notes:

- If a category cannot exist without subcategories, how can all subcategories be deleted if the category needs to remain?
- How can users identify which subcategories can be deleted if there are a large number of subcategories and it's challenging to find the specific ones?
- What message should appear when attempting to delete a subcategory that has been used in expense records?

# T7. Adding expense records

1. Verify that an expense record can be added by clicking the Add Expense button on the Main Page.
1. Verify that the amount is added in the currency of the account.
1. Verify that 0 cannot be added as the amount of the expense.
1. Verify that negative whole numbers can be added as the amount of expenses.
1. Verify that negative decimal numbers can be added as the amount of expenses. /Question below/
1. Verify that positive numbers cannot be added as the amount of an expense and they are automatically replaced with negative numbers.
1. Verify that the amount -1 000 000 000 000 can be added for each currency. /Question below/
1. Verify that the amount -1 000 000 000 001 cannot be added for each currency. /Question below/
1. Verify that the system responds correctly to spaces, dots, or commas when entering the amount. /Not included in requirements/
1. Verify that the system responds correctly to incorrect amounts entered, such as special characters, letters or a zero at the beginning.
1. Verify that the pre-filled fields contain the current date and time. /In the Default account only?/
1. Verify that the time is in the 24h format.
2. Verify that it's impossible to set a non-existent date&time. 
3. Verify that a future date cannot be added.
4. Verify the application's behavior on the boundary values of the optional text field (0, 1, 100, 101 characters).
5. Verify that an existing category can be selected for the expense record.
6. Verify that the total amount of expenses is correct on the Main page.
7. Verify that unlimited numbers of expense records can be added. /Not included in requirements/

Notes:

- Is the category field a required field when adding an expense record?
- Is only the Default account pre-filled on the expense record form?
- Is there a limit on the number of digits allowed after the decimal point when entering the amount?
- Regarding the requirements, there seems to be a discrepancy between S8 AC4 and S3 AC3. It's necessary to reconcile them and determine the maximum amount allowed, such as -1 000 000 000 000.
- What notification will be displayed when attempting to enter an expense more than -1 000 000 000 000?
- Can a specific expense be transferred from one account to another?
- Is there a dedicated option to add an expense record on the Expenses page?

# T8. Updating an existing expense record

1. Verify that it is possible to edit an expense record by clicking Edit.
1. Verify that the account, amount, category (?), subcategory, date & time and note of an existing expense record can be edited. /Question below/
1. Verify that after editing an expense record, the total expense amounts for accounts are recalculated and updated across the system.

Notes:

- Can a user edit a category?
- What happens to the existing expense records associated with a category when it is edited?

# T9. Deleting an existing expense record

1. Verify that it is possible to delete an expense record by clicking Delete.
1. Verify that it is possible to delete all expense records.
1. Verify that after deleting an expense record, the total amount of expenses is recalculated and updated accordingly.

Notes:

- Where are the options to edit and delete expense records located? How are they visually represented? What fields can be edited?

# T10. Integration with a bank account to automatically add expense records based on transactions

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
1. Verify that all bank integrations are visible on the Bank integrations page. /Not included in requirements/
1. Verify that a category can be edited for bank expense records. /Not included in requirements/
1. Verify that a subcategory can be edited for bank expense records.
1. Verify that amount can be edited for bank expense records.
1. Verify that date&time can be edited for bank expense records.
1. Verify that note can be edited for bank expense records.
1. Verify that the total amount of expenses is correct.
1. Verify that an expense account can be changed in the bank integration, and all existing transactions will be linked to the latest selected account.
1. Verify that an expense account cannot be changed in the bank integration if it is not in the relevant currency with the application.
1. Verify that an expense record added through integration can be deleted.
1. Verify that it's impossible to change account for the individual bank expense record (transaction).
1. Verify that the amount -1 000 000 000 000 for each currency can be added as a bank expense record.
1. Verify that the amount -1 000 000 000 001 for each currency cannot be added as a bank expense record.
1. Verify date&time for the transactions received from the bank.

Notes:

- Is the option "Add new bank integration" presented as a button?
- Are there any specific requirements or restrictions on the country of the bank for adding integration?
- How are income records handled in the system? Are they excluded?
- Clarify the exact time format for the creation of expense records daily at 01.00. Is it 1 pm or 1 am? Is the dot a typo?
- What is the time zone?
- Provide more details on how bank transactions are retrieved and integrated into the system.
- Clarify the maximum allowed time for creating expense records in the integration account based on the number of transactions.
- Clarify the maximum allowed time for creating expense records in 20 integration accounts based on the number of transactions.
- Can users manually add expense records to an account integrated with a bank?
- What is the contingency plan if a bank encounters technical issues preventing the creation of expense records at 01:00?

# T11. Deleting an integration with a bank account

1. Verify that a specific bank account in the bank integration can be selected and deleted.
1. Verify that all bank accounts in the bank integration can be deleted.
1. Verify that all created expense records can be retained during integration removal.
1. Verify that all created expense records can be deleted during integration removal.

Notes:

- Is it possible for a user to select and delete all bank accounts in the bank integrations simultaneously?
- How should an expense account with a bank integration be deleted? What steps should be followed?

# T12. Viewing expenses

1. Verify that it's possible to go to the Expenses page by clicking on the account.
2. Verify that it's possible to go to the Expenses page by clicking the Expenses page on the menu. /Not included in requirements/
3. Verify that there amount, category (?), subcategory, note and date&time for each expense on the Expenses page. /Question below/
4. Verify that all expenses for the current month are displayed on the Expenses page.
5. Verify that Month and Year (?) options are available to select previous periods of expenses on the Expenses page. /Question below/
6. Verify that it is not possible to select future periods of expenses.

Notes:

- Are expense recordes displayed on the Main page? How many expense records are displayed on the Main page? Is there a limit or pagination?
- How does a user navigate to an account's Expenses page? Is it by clicking on the account card?
- Is the Expenses page accessible from the application menu?
- Are the category details shown for expenses on the Expenses page?
- Are users able to switch to previous years on the Expenses page to view expenses for specific months in previous years?

# T13. Viewing a pie chart of expenses by categories & subcategories for a month

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

Notes:

- Should users be able to switch to previous years to view expenses for specific months in those years, or is the view limited to the current year only?
- When viewing expenses by subcategories, is there a breakdown of expenses displayed in both percentage and total sum?
- How should the percentages be calculated? Are they whole numbers rounded to the nearest integer value?

# T14. Viewing a pie chart of expenses by categories & subcategories for a year

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

#

I believe it is necessary to refine the structure of the requirements - the order of describing the requirements and provide detailed descriptions for all buttons and field names. The documentation doesn't provide information about the consequences if the user fails to perform the required actions.
