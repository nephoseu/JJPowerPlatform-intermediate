---
lab:
    title: 'Lab 3.3.: Configure a model-driven app'
    module: 'Module 3: Get started with Model-Driven Apps'
---

# Lab 3.3. - Configure a model-driven app

## Scenario

In this lab, you will configure a model-driven app.

## What you will learn

- How to configure navigation for a model-driven app
- How to restrict views in a model-driven app

## High-level lab steps

- Add groups to navigation
- Move tables in navigation
- Restrict views in the app
  
## Prerequisites

- Must have completed **Lab 3.1.: Create model-driven app**, and **Lab 3.2.: Configure forms and views**

## Detailed steps

## Exercise 1 - Configure model-driven app

In this exercise, you will configure navigation and tables a model-driven app.

### Task 1.1 – Configure groups

1. Navigate to the Power Apps Maker portal <https://make.powerapps.com>.

1. Make sure you are in the **JJTrainingEnvironment** environment.

1. Select **Solutions**.

1. Open the **Property listings** solution.

1. In the **Objects** pane on the left, select **Apps**.

1. Select the **Property Management** app, select the **Commands** menu (...), and select **Edit** > **Edit in new tab**.

1. Select **New Group** in the **Navigation** pane.

    ![Screenshot of model-driven app group.](../Media/mda-group.png)

1. In the properties pane, enter `Clients` for **Title**.

1. Select **Navigation**, select the **Commands** menu (...) and select **New group**.

1. In the properties pane, enter `Properties` for **Title**.

1. In the **Navigation pane**, select **Showings view**, select the **Commands** menu (...) and select **Move down**.

1. In the **Navigation pane**, select **Real Estate Properties view**, select the **Commands** menu (...) and select **Move down**.

1. In the **Navigation pane**, select **Open Houses view**, select the **Commands** menu (...) and select **Move down** three times.

    ![Screenshot of model-driven app designer with navigation.](../Media/mda-navigation.png)


### Task 1.2 – Restrict views

1. In the **Navigation** pane, select **Showings view**.

1. In the **Showings** pane, select the **Views** tab.

1. Select the **Inactive Showings view**, in the right-hand pane, and select the **Commands** menu (...) and select **Remove**.

    ![Screenshot of removing a view in the model-driven app designer.](../Media/mda-remove-view.png)

1. Select **Save**.

1. Select **Publish**.

1. **Close** the app designer and select **Done**.

## Congratulations!

You have configured model-driven app.

