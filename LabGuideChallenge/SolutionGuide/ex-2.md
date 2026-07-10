## Task 1:

2. In **Model view (1)**, verify that the **Dim_Region** table contains the **Region (2)** column.

    ![](images1/t1s2.png)

3. On the **Modeling (1)** tab, select **Manage roles (2)**.

    ![](images1/t1s3.png)

4. In the **Manage security roles** window, select **+ New** to create a new row-level security role.

    ![](images1/t1s4.png)

5. Select the **More options (1)** menu for the new role, choose **Rename (2)**, and rename the role as required before configuring the security rules.

    ![](images1/t1s5.png)

6. Rename the role to **RLS - North America**.

   ![](images1/t1s6.png)

7. Select the **Dim_Region (1)** table, and then select **Switch to DAX editor (2)**.

   ![](images1/t1s7.png)

8. In the DAX editor, enter the following filter expression and select the **✔ (2)** icon to validate it.

   ```DAX
   [Region] = "North America"
   ```

   ![](images1/t1s8.png)

9. Repeat the same steps to create the following roles with their corresponding DAX filter expressions, and then select **Save (2)**.

   | Role | DAX Filter |
   |------|------------|
   | RLS - Asia Pacific | `[Region] = "Asia Pacific"` |
   | RLS - Europe | `[Region] = "Europe"` |
   | RLS - Latin America | `[Region] = "Latin America"` |
   | RLS - Middle East & Africa | `[Region] = "Middle East & Africa"` |
   | RLS - North America | `[Region] = "North America"` |

   ![](images1/t1s9.png)

10. On the **Modeling** tab, select **View as (1)**. In the **View as roles** window, select **RLS - North America (2)**, and then select **OK (3)**.

    ![](images1/t1s10.png)

11. Verify that the report displays only **North America** data. Confirm that the slicer contains only **Canada** and **United States (2)**, the bar chart displays only North America regions (3), and then select **Stop viewing (4)**.

    ![](images1/t1s11.png)

12. Select **View as (1)** again, choose **RLS - Europe (2)**, and then select **OK (3)**.

    ![](images1/t1s12.png)

13. Verify that the report displays only **Europe** data. Confirm that the slicer contains only **France**, **Germany**, and **United Kingdom (2)**, the bar chart displays only European regions (3), and then select **Stop viewing (4)**.

    ![](images1/t1s13.png)

## Task 2:

1. On the **Home** tab, select **Copilot (2)** to sign in to Power BI.

    ![](images1/t2s1.png)

2. In the **Enter your email address** dialog box, enter the lab-provided email address (1), and then select **Continue (2)**.

    ![](images1/t2s2.png)

3. Verify the email address (1), and then select **Next (2)**.

    ![](images1/t2s3png)

4. Enter the lab-provided password (1), and then select **Sign in (2)**.

    ![](images1/t2s4.png)

5. When prompted to sign in to all apps and websites on the device, select **No, this app only**.

    ![](images1/t2s5.png)

6. If prompted that a **Power BI free license** has been assigned, select **OK**.

    ![](images1/t2s6.png)

7. If a Fabric workspace does not already exist, create one by selecting **New workspace (1)**, entering a unique workspace name (2), and selecting **Apply (3)**.

    ![](images1/t2s7.png)

8. In Power BI Desktop, select **Copilot (1)**, and then select **Select a workspace (2)**.

    ![](images1/t2s8.png)

9. Select the Fabric workspace (1), and then select **Select workspace (2)**.

    ![](images1/t2s9.png)

10. In the **Copilot** pane, enter the prompt **"Summarize revenue performance by region and call out which regions are below target." (1)**. Review the AI-generated summary (2), and then select **Text box (3)** to add the response to the report canvas.

    ![](images1/t2s10.png)

11. Review the generated summary that has been added to the report canvas.

    ![](images1/t2s11.png)

## Task 3:

12. In the **Data** pane, select the **_Measures (1)** table, and then select **New measure (2)**.

    ![](images1/t3s1.png)

13. Create a new measure by entering the following DAX formula, and then commit the change.

    ```DAX
    Total Target = SUM(Fact_Budget[TargetRevenue])
    ```

    ![](images1/t3s2.png)

14. Select the **Insert (1)** tab, expand **More visuals (2)**, and then select **From AppSource (3)**.

    ![](images1/t3s3.png)

15. In the **Power BI visuals** window, search for **Bullet Chart by OKVIZ (1)**, and then select the **Bullet Chart by OKVIZ (2)** visual.

    ![](images1/t3s4.png)

16. On the **Bullet Chart by OKVIZ** page, select **Add** to import the visual into the report.

    ![](images1/t3s5.png)

17. In the **Visualizations** pane, select the **Bullet Chart by OKVIZ (1)** visual, and resize the visual on the report canvas (2).

    ![](images1/t3s6.png)

18. From the **_Measures** table, select **Total Revenue** and **Total Target (1)** to populate the bullet chart. Verify that the visual displays both measures (2).

    ![](images1/t3s7.png)

19. With the bullet chart selected, open the **Format visual (1)** pane, expand **Data Colors (2)**, and select the color drop-down for **Total Revenue (3)**.

    ![](images1/t3s8.png)

20. Change the **Total Revenue** color by selecting the highlighted theme color (1, 2).

    ![](images1/t3s9.png)

21. Verify that the bullet chart reflects the updated **Total Revenue** color.

    ![](images1/t3s10.png)

22. In the **Format visual** pane, select the **General (1)** tab, expand **Title (2)**, and change the **Text** to **Revenue vs. Target (3)**.

    ![](images1/t3s11.png)

23. Verify that the bullet chart title has been updated to **Revenue vs. Target**.

    ![](images1/t3s12.png)

## Task 4:

24. Select **File**, and then select **Save as**.

    ![](images1/t4s1.png)

25. Select **Save as (1)**, choose the **Documents** folder from the **Recent (2)** list (or another preferred location), and then select **Documents (3)**.

    ![](images1/t4s2.png)

26. Enter **Board-Ready-Dashboard** as the file name (1), and then select **Save (2)**.

    ![](images1/t4s3.png)

27. Return to the report, select the **Home (1)** tab, and then select **Publish (2)**.

    ![](images1/t4s5.png)

28. In the **Publish to Power BI** dialog, select the **Fabric workspace (1)**, and then select **Select (2)**.

    ![](images1/t4s6.png)

29. If prompted to upgrade your Power BI license, select **Try free** to start the trial.

    ![](images1/t4s7.png)

30. After the report is published successfully, select **Got it**.

    ![](images1/t4s8.png)

31. In the Fabric portal, verify that the **Fabric workspace (1)** contains both the **Board-Ready-Dashboard report** and its associated **semantic model (2)**.

    ![](images1/t4s9.png)

32. Select **File**, and then select **Export**.

    ![](images1/t4s10.png)

33. Select **Export to PDF**.

    ![](images1/t4s11.png)

34. Verify that the report is successfully exported and opens as a PDF containing the completed **Sales Performance – Board View** dashboard.

    ![](images1/t4s13.png)

## Task 5:

1. Open **Model view** and verify the data model. Confirm it follows a clean star schema, all relationships are **Many-to-one**, **Single** cross-filter, and **Active**. Ensure all key ID columns (such as **RegionID**, **ProductID**, **CustomerID**, **SalesRepID**, and **OrderID**) are hidden, and verify that **Dim_Date** is still marked as the date table.

2. Review each KPI card individually. Verify that the DAX measure behind each KPI matches its purpose, and confirm each card displays a clear business-friendly title instead of a default field or measure name.

3. Test the report interactions by selecting different values in the **Country/Region slicer**. Confirm that every KPI card and chart updates correctly, and verify that the regional bar chart is sorted in descending order with meaningful chart titles.

4. Review the report formatting by using **View → Fit to page**. Ensure colors are consistent across all visuals, currency and percentage values use consistent decimal formatting, and no visuals overlap or appear misaligned.

5. Validate Row-Level Security (RLS). Use **Modeling → View as** to test at least two different roles and confirm they display different **Total Revenue** values. If the report has been published, verify that each RLS role has an assigned user in the Power BI Service.

6. Review the Copilot-generated narrative. Confirm that all key figures mentioned match the KPI cards and report visuals, and ensure the narrative is clearly labeled as an **AI-generated summary** (or similar reviewed label).

7. Examine the custom visual (such as the **Bullet Chart**). Verify that it matches the report theme and provides meaningful insight beyond the standard KPI cards and charts.

8. Perform a final board-ready review. Confirm the report has a clear title, displays the data refresh date, follows a consistent layout, and is presentation-ready for business stakeholders.

9. Record any remaining issues or improvements identified during the review. Prioritize fixing data accuracy, relationships, and report interactions before making cosmetic formatting changes.