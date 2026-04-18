US-01
As a User, I want to input income into a selected account, so that my account balance increases correctly.
Acceptance Criteria:
Given: User is on the add income form.
When: User inputs nominal, category, selects the destination account, and saves.
Then: System adds the nominal to the selected account balance and records it in the history.

US-02
As a User, I want to see a summary of my total balance from all accounts, so that I can monitor my financial condition.
Acceptance Criteria:
Given: User opens the dashboard/home page.
When: The page loads.
Then: System calculates and displays the combined total balance from all active accounts.

US-03
As a User, I want to filter transaction history by date, so that I can review financial activity.
Acceptance Criteria:
Given: User is on the transaction history page.
When: User selects a specific start and end date.
Then: System only displays transactions that occurred within that date range.

US-04
As a User, I want to edit transaction data, so that incorrect inputs can be fixed.
Acceptance Criteria:
Given: User opens a saved transaction detail.
When: User changes the nominal or category and clicks save.
Then: System updates the transaction data, shows a success notification, and automatically adjusts the account balance accordingly.

US-05 
As a User, I want to categorize my expenses and view them in a chart, so that I understand my spending patterns.
Acceptance Criteria:
Given: User has recorded several expenses with categories.
When: User navigates to the statistics page.
Then: System generates and displays a chart (e.g., pie chart) showing the percentage of expenses per category.

US-06
As a User, I want to allocate balance into Brankas, so that I can save money for specific goals.
Acceptance Criteria:
Given: User has sufficient balance in the main account.
When: User inputs a nominal to allocate to a specific Brankas and saves.
Then: System successfully transfers the allocation target to the Brankas.

US-07
As a User, I want Brankas balance to be isolated, so that it is not used in daily transactions.
Acceptance Criteria:
Given: User has money inside a Brankas.
When: User wants to add a new daily expense.
Then: The Brankas balance is hidden/locked and cannot be selected as a source account for that expense.

US-08
As a User, I want to see saving progress, so that I know how far I am from my target.
Acceptance Criteria:
Given: User has set a target nominal for a Brankas.
When: User views the Brankas detail.
Then: System displays a progress bar or percentage indicating how much has been saved versus the target.

US-09
As a User, I want to record daily expenses from a selected account, so that my balance updates correctly.
Acceptance Criteria:
Given: User opens the add expense form.
When: User inputs nominal, category, selects the source account, and saves.
Then: System deducts the nominal from the selected account balance and saves the transaction.

US-10
As a User, I want to manage multiple accounts (e.g., Cash, BCA), so that I can separate my money sources.
Acceptance Criteria:
Given: User is on the account settings page.
When: User clicks "Add Account", inputs the account name, and initial balance.
Then: System creates the new account and makes it available as a source/destination in transactions.

US-11
As a User, I want to transfer balance between accounts, so that I can manage money distribution without affecting expense stats.
Acceptance Criteria:
Given: User opens the transfer menu.
When: User inputs nominal, source account, destination account, and saves.
Then: System deducts from the source, adds to the destination, and records it specifically as a Transfer (not an expense).