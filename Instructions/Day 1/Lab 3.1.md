---
lab:
    title: 'Lab 3.1.: Create a model-driven app'
    module: 'Module 3: Get started with Model-Driven Apps'
---

# Lab 3.1.: Create a model-driven app

## Scenario

In this lab, you will create model-driven app and add tables to the app.

Contoso Real Estate wants to track two key elements:

- Real estate property listings
- Who is scheduled for showings of real estate properties

## What you will learn

- How to create a model-driven app
- How to add tables to the app

## High-level lab steps

- Create a model-driven app
- Add tables to the app
  
## Prerequisites

- Must have completed **Lab 0: Validate lab environment**


## Detailed steps

## Exercise 1 - Import solution

In this excercise, you will import prepared solution located in **Resources** folder.

1. Download solution: Propertylistings_1_0_0_1 

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


## Exercise 2 - Build model-driven app

In this exercise, you will create a model-driven app.

### Task 2.1 – Create Property Management app

1. Navigate to the Power Apps Maker portal `https://make.powerapps.com`

1. Make sure you are in the **JJTrainingEnvironment** environment.

1. Select **Solutions**.

1. Open the **Property listings** solution.

1. Select **+ New** and then select **App** and select **Model-driven app**.

    ![Screenshot of new model-driven app dialog.](../Media/new-mda.png)

1. Enter `Property Management` for **Name**.

1. Select **Create**.

    ![Screenshot of model-driven app designer.](../Media/mda-designer.png)


### Task 2.2 – Add tables

1. Select **+ Add page**.

    ![Screenshot of add page to model-driven app dialog](../Media/mda-new-page.png)

1. Select **Dataverse table**.

1. Enter `cre_` in **Search**.

    ![Screenshot of add page to model-driven app dialog.](../Media/mda-add-tables.png)

1. Select **Open House**, **Real Estate Property**, and **Showing**.

1. Enter `account` in **Search** and select **Account**.

1. Enter `contact` in **Search** and select **Contact**.

1. Select **Add**.

    ![Screenshot of model-driven app designer with tables.](../Media/mda-designer-with-tables.png)

1. Select **Save**.

1. Select **Publish**.

    ![Screenshot of publishing icon.](../Media/mda-publish-btn.png)

### Task 2.3 – Test

1. With the **Property Management** app designer open, select the **Play** button.

1. Navigate to **Contacts**.

1. Select **+ New**.

1. Enter `Jon` for **First Name**.

1. Enter `Doe` for **Last Name**

1. Select **Save & Close**.

1. Navigate to **Real Estate Properties**

1. Select **+ New**.

1. Enter `Test Property` for **Property Name**.

1. Select **Save**.

1. Select **Related** and **Showings**.

    ![Screenshot of model-driven form related tables.](../Media/mda-related-records.png)

1. Select **+ New Showing**.

1. Enter `First Showing` for **Name**.

1. Select **Save & Close**.

1. Select **Save & Close**.

## Congratulations!

You have created Model-driven app.
