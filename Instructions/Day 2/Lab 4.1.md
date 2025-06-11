---
lab:
    title: 'Lab 4.1: Calculated and rollup columns'
    module: 'Module 4: Advanced Model-Driven App concepts'
---

# Lab 4.1: Calculated and rollup columns

## Prerequisites

- Must have completed **Lab 0: Validate lab environment**

## Exercise 1 - Import solution


In this excercise, you will import prepared solution located in **Resources** folder.

1. Download solution: FabrikamEnvironmental_1_0_0_1 

1. Navigate to the Power Apps Maker portal `https://make.powerapps.com`

1. Make sure you are in the **Dev** environment.

1. Select **Solutions**.

1. Select **Import solution**.

1. Choose solution you downloaded.

    ![Screenshot of importing solution.](../media/import-solution.png)

1. Select **Next**

1. Select **Import**

1. Wait few moments until it is imported.

    ![Screenshot of importing solution in progress.](../media/import-solution-inprogress.png)



### Exercise 2  – Add a calculated column
1.  Navigate to the Power Apps Maker portal `https://make.powerapps.com`

1.  Make sure you are in the **Dev** environment.

1.  Select **Solutions**.

1.  Open the **Fabrikam Environmental** solution.

1.  In the **Objects** pane on the left, expand **Tables**, and select **Project**.

1.  Under **Schema**, select **Columns**.

1.  Select **+ New column**.

1.  Enter `Length of Project` for **Display name**.

1.  Enter `Number of days` for **Description**.

1.  Select **Number** in the **Data type** drop-down. The Data type will be set to **Whole Number** and the Format will be set to **None**.

1.  Change the **Behavior** drop-down to **Calculated**.

1.  Select **Save and edit**.

    ![Add calculated column.](../media/add-calculated-column.png)

    > **Note:** You may need to disable the pop-up blocker in your browser first, then open the **Length of Project** column and select **Edit**.

1.  When a new browser window opens, select **+ Add condition**.

1.  Select **Scheduled Start** for **Field**.

1.  Select **Contains data** for **Operator**.

1.  Select the green check mark to save changes.

    > **Note:** You may need to resize the window to see the check mark.

1.  Select **+ Add condition**.

1.  Select **Estimated End** for **Field**.

1.  Select **Contains data** for **Operator**.

1.  Select the green check mark.

1.  Select **+ Add action**.

1.  Enter the following formula:

    ```DIFFINDAYS(contoso_scheduledstartdate,contoso_estimatedenddate)```

    > NOTE: You can use intellisense to type and select the elements in the formula.

1.  Select the blue check mark to save changes.

1.  Select **SAVE AND CLOSE**.

    ![Calculated column.](../media/calculated-column.png)



### Exercise 3 -  Rollup column for the project one-to-many relationship

1.  In the **Objects** pane on the left, expand **Tables**.

1.  Select the **Project** table.

1.  Select **+ New** > **Column**.

1.  Enter `Total Project Funding` for **Display name**.

1.  Select **Currency** in the **Data type** drop-down.

1.  Change the **Behavior** drop-down to **Rollup**.

1.  Select **Save and edit**.

1.  When the new browser window opens, select **+ Add related entity**.

1.  Select **Project Funding (Project)** for **Related**.

1.  Select the blue check mark.

1.  Select **+ Add condition**.

1.  Choose **Status** for **Field**.

1.  Choose **Equals** for **Operator**.

1.  Verify **Active** is selected for **Value**.

1.  Select the green check mark.

1.  Select **+ Add aggregation**.

1.  Select **SUM** for **Aggregate Function**.

1.  Select **(Project Funding) Funding Amount** for **Aggregate Related Entity Field**.

1.  Select the green check mark.

1.  Select **SAVE AND CLOSE**.

    ![Add rollup column.](../media/add-rollup-column.png)
