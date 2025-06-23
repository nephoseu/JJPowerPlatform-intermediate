---
lab:
    title: 'Lab 5: Trigger filters'
    module: 'Module 5: Automate processes with Power Automate'
---

# Practice Lab 7 – Trigger filters

In this lab you will filter on an update trigger.

## What you will learn

- How to filter triggers

## High-level lab steps

- Create an automated flow
- Add column filter
- Add query filter

## Prerequisites

- Must have completed **Lab 0: Validate lab environment**

## Exercise 1 - Import solution


In this excercise, you will import prepared solution located in **Resources** folder.

1. Download solution: TrigerFilters_1_0_0_1 

1. Navigate to the Power Apps Maker portal `https://make.powerapps.com`

1. Make sure you are in the **JJTrainingEnvironment** environment.

1. Select **Solutions**.

1. Select **Import solution**.

1. Choose solution you downloaded.

    ![Screenshot of importing solution.](../Media/import-solution.png)

1. Select **Next**

1. Select **Import**

1. Wait few moments until it is imported.

    ![Screenshot of importing solution in progress.](../Media/import-solution-inprogress.png)

## Exercise 2 - Schema name

### Task 2.1 - Column schema name

1. Navigate to the Power Apps Maker portal `https://make.powerapps.com`

1. Make sure you are in the **Dev** environment.

1. In the left navigation pane, select **Tables**.

1. Select **Opportunity**.

1. Under **Schema**, select **Columns**.

1. Select the **Status** column.

    ![Screenshot of status columns.](../Media/opportunity-status-column.png)

1. Expand **Advanced options**.

    ![Screenshot of column schema name.](../Media/column-schema-name.png)

1. Copy the **Logical name** for use in the flow.

   > **Note:** The prefix for your Status column may be different.


## Exercise 3 – Create automated flow

### Task 3.1 - Create the trigger

1. Navigate to the Power Automate portal `https://make.powerautomate.com`

1. Make sure you are in the **Dev One** environment.

1. Select the **+ Create** tab from the left navigation menu.

1. Select **Automated cloud flow**.

1. Enter `Opportunity Closed` for **Flow name**.

1. Enter `Dataverse` in search all triggers.

1. Select **When a row is added, modified, or deleted**.

1. Select **Create**.


### Task 3.2 - Configure the trigger

1. Select the **When a row is added, modified, or deleted** step.

1. Select the **When a row is added, modified, or deleted** step name and enter `Opportunity changed`

1. Select **Modified** for **Change Type**.

1. Select **Opportunities** for **Table Name**.

1. Select **Organization** for **Scope**.

    ![Screenshot of update row trigger.](../Media/update-trigger.png)


### Task 3.3 - Send email

1. Select the **+** icon under the trigger step and select **Add an action**.

1. Enter `email` in search.

1. Select **Send an email (V2)** under **Office 365 Outlook**.

1. Select **Send an email (V2)** step name and enter `Notify by email`

1. Select **To** field and select **Enter custom value**.

1. Enter your tenant user id for **To**.

1. Select **Subject** field and enter `Opportunity closed`

1. Select **Body** field and select the Dynamic content icon.

1. Select **Opportunity Subject** from **Opportunity changed**.

1. Select **Body** field and select the Dynamic content icon and select **See more**.

1. Select **Status** from **Opportunity changed**.


### Task 3.4 - Column filter

1. Select the **Opportunity changed** trigger step.

1. Select **Show all**

1. Select the **Select Columns** field and enter the **Logical name** from the previous exercise, for example: `cr977_status`

   > **Note:** The prefix for your status column will be different.


### Task 3.5 - Row filter

1. Select the **Opportunity changed** step.

1. Select **Show all**

1. Select the **Filter Rows** field and enter `cr977_status eq 3` using the **Logical name** from the previous exercise.

    ![Screenshot of trigger filter.](../Media/trigger-filter.png)

    > **Note:** The prefix for your status column will be different.

1. Select **Save**.

1. Select the **<-** **Back** button from the top left of the command bar.

