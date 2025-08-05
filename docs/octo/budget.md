# Budget

Octo's budget management feature allows users to control and monitor spending for their cost groups. It provides tools to create budgets for various periods, set up automated notifications, and track real-time expenditure against the allocated budget.

## Steps on How to Create a Budget

To create a budget in Octo, follow these steps:

### 1. Navigate to the Budget Management Tab:
   * Go to the "Cost Group" section in the left pannel.
   * Select the specific cost group for which you want to create a budget and then head over to the budget tab.

### 2. Initiate Budget Creation:
   * Click the "Create Budget" button. A three-step pop-up dialog will appear.

![create budget](https://lh3.googleusercontent.com/d/1bi12NOoa2XKSEoPKJjaqr_y0Ryc1W5BP)

### 3. Step 1: Select Budget Period:
   * Choose the budget period: "Three Months," "Six Months," or "Twelve Months."
   * Specify the "Customize Starting and Ending Month" by selecting a start date then click **Next**. Note that the end date will automatically be calculated based on the chosen period (e.g., three months minus one day) .

![select period](https://lh3.googleusercontent.com/d/12GvwASXZBLWjpZXlolc0BwAdMoVLpZkx)
![date range](https://lh3.googleusercontent.com/d/1YAKWmBb5T1aAVtZFHCRzCXUPZK5tix2J)

### 4. Step 2: Set Budget Amount:
 Supply the amount of budget you want to set and take a look on the chart above as it simply provides a visual  representation of this data.

   ![budget table](https://lh3.googleusercontent.com/d/1_57RwN5_VmZXKOURVIZG_WNReC-yzP6Z)

   * **Forecast Data:** This is derived from historical usage patterns; more past data leads to more accurate forecasting. This helps to manage the amount of budget you want to allocate for that cost group. Refer to this docs for more information.
   * **Previous Period Spending:** This row displays spending data from the same period one year prior to help identify trends.
   * **Budget:** This is where you configure your budget.
   * **Difference:** This shows the percentage difference between the previous period's spending and the current budget.
   * **Choose Budget Type:**
      * **Distributed Budget:** Enter a "Total Budget" amount, and it will be equally divided across all months in the selected period.
      * **Cumulative Budget:** Toggle this option to manually input a different budget amount for each month. **Warning:** Switching from a cumulative to a distributed budget will reset all manually entered monthly values to zero.
   * Optionally, click "Export Data to CSV" to export the table data.

![budget type](https://lh3.googleusercontent.com/d/1T0gacBO_CM553EPrDPDdic-Rh9sX0GHw)
   

### 6. Save or Create Budget:
   * **Save as Draft:** If you are not yet ready to activate the budget, click "Save as Draft." You can configure or delete drafts later from the main budget view list.

![save as draft](https://lh3.googleusercontent.com/d/1MF1YSAwUyebusGqhZr0FTWRkJYlme0Kq)

   * **Create Budget:** If you are satisfied with the budget, click "Create Budget" to activate it. Once created, the budget will show an "Active" status. Click **Next** after supplying the amount of budget.

![create budget](https://lh3.googleusercontent.com/d/1KvFFExsuXz-HpxmZT04NoH6NZOUAZDWC)

> **Note:** Set Budget Notification (Optional but Recommended):
   * *For detailed steps on setting budget notifications, please refer to the documentation on Budget Alerts.*
## Budget Status

* **Draft Budgets:** Users can save a budget as a draft if they are not yet ready to activate it. Drafts can be configured or deleted later.
* **Active Budgets:** Once a budget is created (not a draft), it becomes active.
* **Expired Budgets:** A checkbox allows users to view past budgets that have exceeded their end date.
* **Reload Button:** This fetches the most up-to-date budget data for the cost group.

![budget status](https://lh3.googleusercontent.com/d/1U_g7af-fT3MHmYaW0VF_XKxRV-OMjGNU)

## Budget Details View

* **Budget Progress:** This indicates the percentage of the total budget that has been spent, offering a snapshot of spending patterns.
* **Summary Cards:** These cards display total actual spending, total budget, budget progress, and the budget period.
* **Actual Cost:** This row shows the current cost for each month, updating in real-time.

![view details](https://lh3.googleusercontent.com/d/1Ii7cb70d4YU7rp8Bc_jl4lzrByn9xu5l)
![budget view](https://lh3.googleusercontent.com/d/1KW3XNTh3x5IX7th4c8JEWAlRND7jPCIC)

## Budget Settings

Users can click the notification bell to create budget alerts. From the budget settings, users can also edit, delete, and view budget information.

![budget settings](https://lh3.googleusercontent.com/d/1aDb6KThA2PQXQo-_3iaJSSrRPTauDNrx)

> **Note:** The "edit budget" and "delete budget" options are only visible to the budget creator or an admin. If a user is neither, these options are hidden.