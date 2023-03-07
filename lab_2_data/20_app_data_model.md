---
layout: default
title: Kudos table
parent: 2. Data Model
nav_order: 40
---

# Kudos table

## Duration: 60 minutes

[Next][NEXT]{: .btn .btn-purple }

The first step in creating an application is defining the data model.

We will be creating a Kudos table that will be the basis of our application. The Kudos table will will be built from scratch.

1. Once the **App Home** tab opens, select **Add a table or upload a spreadsheet**

    ![Kudos Table Image 1](../images/base_1.png)

2. Select **Create a table** and then the **Get started** on the next screen
    
    ![Kudos Table Image 2](../images/base_2.png)

    ![Kudos Table Image 3](../images/base_3.png)

3. Select the **Create from scratch** option and then **Continue**

    ![Kudos Table Image 4](../images/base_4.png)

4. Set the **Table label** field to **Kudo** (no need to add the plural as the platform will take care of that for you)\
    Select **Auto number**\
    Set the **Prefix** field to **KUDO**

    ![Kudos Table Image 7](../images/base_7.png)    

5. The next step is to setup permission for the Kudos table. Assign full permissions to the admin role by selecting **All**. Select the **Create**, **Read** and **Write** permissions for the user role

    ![Kudos Table Image 8](../images/base_8.png)

6. Select **Edit table** once the table is created to return to start adding some fields
    If you get a **Welcome to Table builder** messages, click the **X** to close the dialog
    
    ![Kudos Table Image 9](../images/base_9.png)

7. Select the **+ Add new field** link next to the **Table fields** heading

    ![Kudos Table Image 10](../images/base_10.png)

8. In the new row created, add the following values:

    | Recipients | |
    | ---:|:----------- |
    | Column Label | Recipients |
    | Column Name | recipients (auto generated) |
    | Type | List |
    | Reference | User (sys_user) |
   
    ### Sometimes reference tables share the same label. Make sure you select the correct table, in this case sys_user. ###
 
    ![Kudos Table Image 11](../images/base_11.png)

    When Reference is selected from the **Type** drop-down, the Reference selector will open below the field to allow you to designate the table being referenced. Reference fields are just one important method of unlocking the value of the Now Platform. By leveraging data from existing business processes, we streamline application creation and ensure data quality across all solutions that leverage shared data sets.

    ![Kudos Table Image 11](../images/base_13.png)

9.  Once you have updated all the information, press enter to update the row and return to the Table Builder Screen

10. Repeat steps 7-9 for each of the following fields (empty cells indicate no value to enter):
    
    |Column Label|Column Name|Type|Reference|Length
    |-------------|-|-|------------------------|-|
    | Giver | giver (auto generated)|Reference| User (sys_user)||
    | Notify Manager | notify_manager (auto generated)|True/False| ||
    | Achievement | achievement (auto generated)|Reference| User (sys_user)|1024|
    
Excellent! In our next exercise we'll create experiences that will allow employees to submit kudos for their peers!

[Next][NEXT]{: .btn .btn-purple }

[NEXT]: ../lab_3_experience/40_dept_req_table

