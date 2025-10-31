# Forecasting

Octo’s Forecasting helps you **predict future cloud costs** from the **historical spend** of a chosen **Cost Group**. See expected totals and trends in **daily** or **monthly** views, and quickly **compare forecasts with actuals**. If you already know about a launch, migration, or seasonal spike, use **External adjustments** to set the number for those months. The result: **clear budgets**, better **commitment planning**, and **early variance detection**—keeping engineering and finance in sync.


## Create a Forecast

Use this flow to add a new **Forecast** for an existing **Cost Group**—you’ll pick a period and granularity, optionally apply **adjustments** for known events (launches, migrations, seasonality), and save it for ongoing tracking.

**Prerequisites**

- You already have a **Cost Group** (forecasts are always scoped to one).  
  **New to Cost Groups?** See the guide: <https://labs.alphaus.cloud/docs/octo/costgroup/>

  You’ll see one of two entry views when opening **Forecast**:

### First-time (empty state)

If your org has no forecasts yet, you’ll see a welcome card with a short description and a **Create forecast** button.  
![Forecast Empty State](https://lh3.googleusercontent.com/d/1W9RXuyptCs87k7dfgvh3_zMX9b6YUaAx)

### Forecast list (when forecasts already exist)

If your org already has forecasts, you’ll see a table of existing items with columns like **Forecast**, **Cost group**, **Period**, **Creator**, **Created on**, **Last updated on**, and **Actions**. Use **Sort**, **Search**, or **Refresh**. To add another one, click **+ Create new forecast** (top-right).  
![Forecast List](https://lh3.googleusercontent.com/d/18axiEU6RnwjsR-eRQ7n-Ng_kKUIiAnJG)

### Configure the forecast (builder view)

After clicking **Create forecast**, you’ll land on the **builder** where you configure the basics and preview results.

> **Default selection:** The **Cost group** defaults to **All Accounts**.  
> This cost group is system-generated during onboarding and **cannot be deleted**.

![Forecast builder](https://lh3.googleusercontent.com/d/1gkH007thrXeZGPiM1fGwPNo9hzP872Ey)

### What’s on this page

- **Name** — The forecast title (defaults to **Untitled forecast** until renamed).
- **Data sufficiency banner** — Indicates when cost groups with < 1 month of history are temporarily hidden.
- **Cost group** — The scope of the forecast; Defaults to the system-generated **All Accounts** group.
- **Look-forward period** — The forecast horizon (e.g., 3/6/12 months or custom).
- **Include current month** — Option to include the in-progress month in the forecast window.
- **Lookback period** — How much historical cost to display for context (e.g., last 6 months); does not change the forecast horizon.
- **History overlay** — Quick toggle to show the last 6 months of actual cost for context.
- **Granularity** — Time bucket for values: **Daily** (detail) or **Monthly** (planning).
- **External adjustments settings** — Area to add increases/decreases for specific dates or months; applied on top of the base model.
- **Preview chart & totals** — Visualization of actuals vs. forecast with running totals.

### Name the forecast

- **Default title:** Displays as **Untitled forecast** until you rename it.
- **Rename:** Click the (pencil) icon beside the title to open the rename dialog.
- **Save:** Enter your desired name, then click **Confirm and save**.

![Edit forecast name](https://lh3.googleusercontent.com/d/1y__GtbZ70Xzo1RDmZi7B7y8YzKe1DXMo)

> **Tip:** Use a clear, unique title that includes the cost group and period, e.g.,  
> `All Accounts — 6-Month Forecast (with adjustments)`.

### Select a cost group

- **Default:** **All Accounts** (system-generated during onboarding; not deletable).
- **Change:** Open the **Cost group** dropdown and pick any available cost group.
- **Scope:** The forecast inherits the selected group’s filters (vendor, accounts, services, tags).
- **Availability note:** Cost groups with less than **1 month** of history are hidden until sufficient data exists.

![Select cost group](https://lh3.googleusercontent.com/d/1InvxO6SJfvo5kbNKuIbk58ZLrzLfAkCP)

### Look-forward period

- Defines how far into the future the forecast projects.
- Options: **1 month**, **3 months**, **6 months**, **12 months (Max)**.
- The picker shows the exact **date range** for each option before you apply it.
- Works with **Include current month**: when enabled, the current in-progress month is part of the window; when disabled, the window starts from the next full period.
- Affects the **forecast line, bounds, and totals** shown in the chart and header; it doesn’t change the historical lookback.

![Look-forward period](https://lh3.googleusercontent.com/d/1pivZH8gFtKvc6cU5hjUZp08YeOCDAZcO)

### Include current month

- **Purpose** — Controls whether the in-progress month is part of the forecast window.
- **When OFF** — The forecast starts **next month**;
- **When ON** — The forecast includes **this month**;
- **Why use it** — Turn **OFF** for clean, future-only projections; turn **ON** when you want this month’s picture (actuals + remaining forecast) in a single view.

![Include current month — OFF](https://lh3.googleusercontent.com/d/1H9_MRWD87Y-VLRziFaTr850XTcni60NC)

### Lookback period

- **What it does** — Controls how much **historical actual cost** is shown for context above the chart.
- **Options** — **Last 1 month**, **Last 3 months**, **Last 6 months**, **Last 12 months (Max)**. The menu shows the exact date range for each choice.
- **Scope** — Visual-only. It does **not** change the forecast horizon, calculations, or totals; it simply adjusts the history you see.
- **Granularity-aware** — History is displayed in the currently selected **Daily** or **Monthly** view.
- **Use it for** — Quick trend context (short lookback) or seasonality checks (long lookback).

![Lookback period](https://lh3.googleusercontent.com/d/1pivZH8gFtKvc6cU5hjUZp08YeOCDAZcO)

### Granularity

- **What it is** — The time bucket for viewing and totaling values: **Daily** (per day) or **Monthly** (per month).
- **Daily** — Fine-grained view for near-term monitoring and spotting spikes; tooltips and totals reflect daily buckets.  
  _Note:_ Adjustments are defined monthly; when viewing **Daily**, the monthly adjustment is **evenly distributed across days** in the adjustment period.
- **Monthly** — Smoothed, month-over-month view suited for budgeting and executive reviews; totals reflect monthly buckets.
- **Scope** — Switching granularity doesn’t change your look-forward or lookback windows; it only changes how values are bucketed and displayed.

![Granularity — Daily view](https://lh3.googleusercontent.com/d/121X_yFkeMGA5P9ua7JETFan5Doi5-2Bo)

### External adjustments

Use **External adjustments** to set the **monthly forecast value(s)** for specific months when you already know the outcome will differ from the model. Adjustments are **monthly**; in **Daily** view their effect is **evenly distributed across days**.

![External adjustments dialog](https://lh3.googleusercontent.com/d/1jCYvEU7Wg2JIfdL4Vfg79lRnfWhsOqIZ)

**What you define**

- **Adjustment name** — A clear label (e.g., “Q4 Launch Ramp”).
- **Period** — **Custom period** (start/end month) or **Entire period** (the whole look-forward window).
- **Amount** — The **absolute monthly amount** you want applied to each selected month.  
  _(You can add more than one adjustment for the same month.)_

**How it behaves**

- If a month has **no adjustments**:  
  `Final Forecast (month m) = Baseline (month m)`
- If a month has **one or more adjustments**:  
  `Final Forecast (month m) = SUM(all adjustments for month m)`  
  _(This **replaces** the baseline for that month.)_

**Example**

- Baseline for next month = **$400**
- Add Adjustment A = **$450** → Final = **$450**
- Add Adjustment B = **+$20** → Final = **$470** (450 + 20)

**Tips**

- Add a **single absolute** number when you already know the target (e.g., “June = 450”).
- Add **incremental adjustments** (e.g., `20`, or `50`) if expectations change; they **stack** by summation.
- Name adjustments descriptively so teammates understand the assumptions.

---

External adjustments can be applied over a **Custom period** or the **Entire period** of the forecast. In both modes you enter **absolute monthly values** that override the model for the selected months. If multiple adjustments target the same month, their **values are summed** and the sum becomes that month’s final forecast.

#### Custom period

Apply an adjustment to a **specific window** inside the look-forward period.

- **Select range:** Choose **Start period month** and **End period month**.
- **Per-month inputs:** A table lists the months in that range with **Original value** (baseline) and an editable **New value**.
- **Confirm:** Click **Confirm and add** to create the adjustment.

![External adjustments — Custom period](https://lh3.googleusercontent.com/d/1QWNgwS6_NLbUsQJbp6n4F9I2wOLqcmZ1)

#### Entire period

Apply an adjustment across the **whole look-forward window** at once.

- **All months visible:** The table shows every month in the forecast horizon with **Original value** and **New value**.
- **Confirm:** Click **Confirm and add** to apply.

![External adjustments — Entire period](https://lh3.googleusercontent.com/d/1CJLTVK-kcFlqG3dLXMhzJUPEenp5Y0Vz)

---

### Review before saving

This preview reflects your current configuration (cost group, look-forward, include current month, granularity, and any external adjustments).

- **Forecast (total amount)** — Sum of all months in the look-forward window, using your **overrides** where present and the **baseline** elsewhere.
- **Total actual cost in forecast period** — Sum of actuals within the same window (shown when the period includes months with actual spend).
- **Chart** — Solid line for **Actual**, dashed line for **Forecast**. Months with **adjustments** are highlighted with markers.
- **Table** —
  - **Forecast** row shows the final per-month values. A small note icon indicates a month has adjustments.
  - **Actual** row shows realized spend for months that have elapsed (or are in progress when “Include current month” is on).

> When everything looks right, click **Save forecast** (top-right) to create it. You can edit or add more adjustments later.

![Review before saving](https://lh3.googleusercontent.com/d/14E0Vgn2XN5kxQIIxHnLRNTghmFHAVjDG)

### Save the forecast

Click **Save forecast** (top-right). A confirmation note explains that some settings become locked to keep the forecast comparable over time.

![Save forecast confirmation](https://lh3.googleusercontent.com/d/1_kYCkjfpseYovwbjpbq-4mddOeOZi5js)


> **Note – Forecast availability**
> After creating/saving a forecast, results may **not appear immediately**—especially if the Cost Group is new or hasn’t generated forecast data yet. Octo refreshes forecasts on a daily schedule, so values should populate **within the next day (≈24 hours)**.

---

## View a Forecast

On the **Forecast** page you’ll see a table of saved items with columns for **Forecast**, **Cost group**, **Period**, **Creator**, **Created on**, and **Last updated on**.  
To open a forecast, **click the red-circled View icon (ℹ︎) in the Actions column**.

![Forecast list — click the red-circled View icon to open details](https://lh3.googleusercontent.com/d/1tFDpZdN3brztIinky8VPX9Pu6ZJdxN6R)

---

## Edit a forecast

Editing uses the same builder as **Create**, with most fields editable.

1. In the **Forecast** list, click the **pencil** icon (✏️) in the **Actions** column.
2. Update fields as needed:
   - **Name**
   - **Look-forward period**
   - **Include/Exclude from lookback display**
   - **External adjustments** (add, edit, remove)
3. Click **Save forecast**.

> **Locked after creation:**  
> You **cannot** change the **Cost group** or the **Include current month** toggle on an existing forecast.

![Forecast list — click the pencil icon to edit](https://lh3.googleusercontent.com/d/1tXGL1I5a-_vWzLncbuf6XrFh-3d_BZ4O)
*Screenshot: the edit (pencil) icon is encircled in red.*

---

## Delete a forecast

1. In the **Forecast** list, click the **trash** icon (🗑️) in the **Actions** column.
2. Confirm the deletion.

> **Note:** Deleting a forecast removes only the forecast configuration.  
> It does **not** delete your Cost Group or any historical cost data.

![Forecast list — click the trash icon to delete](https://lh3.googleusercontent.com/d/1_j63MzCyVu-lfOsryUFyv1P6RMeKorSL)
*Screenshot: the delete (trash) icon is encircled in red.*


## View Forecast Data in CostGroup Overview

Other way to view forecast data, follow these steps:

1. **Navigate to the CostGroup Overview Page:**

   - The forecasting data is primarily displayed on the "Overview" page within the cost group.

2. **Adjust the Date Range to Include Future Dates:**

   - The forecast cost will only appear if the selected date range includes future dates.
   - Click on the date range selector.
   - Choose a date range that extends into the future (e.g., select the current month to the end of the month, or a future month).
   - Click "Apply" to update the view.

3. **Identify Forecasted Costs:**

   - Once the date range is adjusted, you will see a "Forecast Cost" line or section, typically colored gray, on the cost chart and in the data table.
   - This "Forecast Cost" represents the predicted future spending.

4. **Understand Grouping Limitations:**
   > **Note:**
   >
   > - A text indicator is displayed to inform users that the graph includes forecast data.
   > - There's a forecast data shown in the graph for the current day since the Cost and Usage Report (CUR) is still being processed.
