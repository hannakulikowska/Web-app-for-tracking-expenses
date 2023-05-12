# Requirements

Web application for tracking expenses.

![Home](https://github.com/hannakulikowska/Web-app-for-tracking-expenses/assets/80547490/5cd210a6-050c-4512-b834-9639f27e50a8)

The application provides users with the ability to track their previous expenses by categories and subcategories, so that they can see detailed information about their spending.

This app also offers analytics and reporting by categories and subcategories, allowing users to evaluate their expenses and make more informed financial decisions.

### S1. As a User I want to create an account to track my expenses.

ID  | Acceptance criteria
--- | ---
AC1 | User should be able to create an account to track expenses in a particular currency.
AC2 | There are 2 required fields on account creation: Name, Currency.
AC3 | Currency field is a single-select. Currencies available are USD, BYN, EUR.
AC4 | Name length max 100 chars.
AC5 | User can have maximum 20 accounts.
AC6 | Account can be marked as Default.


### S2. As a User I want to create categories & sub-categories to be able to differentiate my expenses.

ID  | Acceptance criteria
--- | ---
AC1 | <dd>User can create a Category to identify area of expense, for example, Health.</dd> <dd>Required field: Name, max length: 50 chars.</dd>
AC2 | <dd>User can add sub-categories to existing Category.</dd> <dd>Required field: Name, max length: 50 chars.</dd>
AC3 | Category can’t have 0 sub-categories.
AC4 | Caterogies and sub-categories should have unique names.


### S3. As a User I want to add an expense record to track my expenses.

ID  | Acceptance criteria
--- | ---
AC1 | User can enter amount of an expense. Amount added in the currency of the account.
AC2 | <dd>Required fields: account, amount, sub-category, date, time (24h format).</dd> <dd>Default account is pre-filled, current date & time are pre-filled while adding an expense.</dd> <dd>Optional field: Note. Text field, max length 100 char.</dd>
AC3 | Max amount 1 000 000 000 000.
AC4 | User should select existing or create a new sub-category for the expense record.


### S4. As a User I can update categories & sub-categories.

ID  | Acceptance criteria
--- | ---
AC1 | User can rename an existing category or sub-category. Latest name will be shown in previous expense records.


### S5. As a User I can delete categories and sub-categories.

ID  | Acceptance criteria
--- | ---
AC1 | User can delete existing category or sub-category.
AC2 | <dd>There should be a pop-up window in case deleting a sub-category that was used in records.</dd> <dd>User should select other sub-category to be used in previous records.</dd>
AC3 | <dd>There should be a pop-up window with message in case deleting a category with sub-categories which were used in the records. The message is “Please, remove sub-categories first”.</dd> <dd>In the opposite case(sub-categories weren’t used yet), category and it’s sub-categories are removed.</dd>

### S6. As a User I want to update an existing expense record to track my expenses.

ID  | Acceptance criteria
--- | ---
AC1 | User can edit account, amount, sub-category, date & time, note of the existing expense record.
AC2 | Total expense amounts for accounts are recalculated after change & updated across the system.

### S7. As a User I want to delete an existing expense record to track my expenses.

ID  | Acceptance criteria
--- | ---
AC1 | User can delete an existing expense record. Total expense amounts are recalculated.

### S8. As a User I want to integrate with my bank account to automatically add expense records based on my transactions.

ID  | Acceptance criteria
--- | ---
AC1 | <dd>User can add integration only with BANK1, BANK2.</dd> <dd>User can select only bank accounts with the currencies relevant to our application.</dd>
AC2 | There should be a new page named Bank integrations. With option ‘Add new bank integration’.
AC3 | <dd>User can add a new integration with BANK1, BANK2.</dd> <dd>User should pass authorization for his bank.</dd> <dd>After successful authorization user can view & select one or several bank accounts to track expense records.</dd> <dd>After selecting bank account(s) user should select an expense account for each of it.</dd>
AC4 | <dd>Expense records will be created for the transactions with negative amounts.</dd> <dd>Expense records will be created starting from the day of adding the bank integration.</dd>
AC5 | Expense records are created daily at 01.00 for the transactions of previous day.
AC6 | Sub-categories should be automatically added for the expense records from a bank integration. Sub-categories are identified according to the merchant name in the transaction, for example “Pizza Pilgrims” merchant -> Cafes sub-category.
AC7 | User can edit sub-category, amount, date&time, note for the bank expense records.
AC8 | User can’t update account for the individual bank expense record.
AC9 | User can change expense account in the bank integration. All existing transactions will be linked to the latest selected account.
AC10 | User can delete expense record added through integration as any other expense.

### S9. As a User I want to delete an integration with my bank account.

ID  | Acceptance criteria
--- | ---
AC1 | <dd>User can remove an existing integration with the bank account.</dd> <dd>User can select a specific bank account in the bank integration to be deleted.</dd>
AC2 | User can select an option to keep all created expense records or to delete them.

### S10. As a User I want to see my expenses.

ID  | Acceptance criteria
--- | ---
AC1 | There should be a page (Main page) where user can see his accounts.
AC2 | Account name, currency, total amount spent in the current month is shown for each account.
AC3 | Add Expense option is available on the main page.
AC4 | <dd>User can click on the Account and go to account’s Expenses page. Expense transactions for the current month are shown there.</dd> <dd>User sees amount, sub-category, note, date&time for the expense.</dd>
AC5 | User can switch month on the Expenses page to see previous expenses.
AC6 | There’s Edit and Delete option available for each expense record.

### S11. As a User I want to see a pie chart of expenses by categories for a month.

ID  | Acceptance criteria
--- | ---
AC1 | User can select Report in the menu and go to the Report page where he can see a pie chart of expenses by categories for a month.
AC2 | Pie chart is shown for default account. User can switch accounts on the report page.
AC3 | <dd>Default month - current month.</dd> <dd>User can switch month to see stats for other periods.</dd>
AC4 | User sees categories on chart and break-down. Break-down shows categories with expenses shown both ways: in percent and total sum spent in currency.
AC5 | User can click on category and see break-down of expenses by sub-category.
AC6 | User sees total amount spent in a month.

### S12. As a User I want to see a pie chart of expenses by categories for a year.

ID  | Acceptance criteria
--- | ---
AC1 | User can switch between periods month - year on the Report page.
AC2 | When user switches to yearly period he sees a pie chart of expenses by categories for a year.
AC3 | <dd>Default year - current year.</dd> <dd>User can switch year to see stats for other periods.</dd>
AC4 | User sees categories on chart and break-down. Break-down shows categories with expenses shown both ways: in percent and total sum spent in the currency.
AC5 | User can click on a category and see a break-down of expenses by sub-category.
AC6 | User sees total amount spent in a year.
