# Publish, Share, and Enhance User Experience in Power BI

### Overall Estimated Duration: 2 Hours

## 📘 Overview

You are the analyst at **Contoso Retail** who built the **Store Performance report** in Hands-on Lab 1 — a single-page report with KPI cards, a Sales-by-Store bar chart, a Sales Trend line chart, a store-location map, and DAX measures for Total Sales and % of Total Sales. In this lab, you take that report on its next journey: from a local `.pbix` file on the lab VM to a published, shared, refreshed, and design-polished business asset in the **Power BI Service**.

You will first publish the report and its semantic model to a workspace, pin its key visuals into an **Executive Dashboard**, walk through the three primary sharing methods (workspace roles, direct sharing, and Power BI apps), and configure **scheduled refresh** so the data stays current without manual effort. You will then return to the report itself and apply professional design polish — a layout grid and brand theme, conditional formatting, backgrounds and shapes, a certified custom visual from **AppSource**, interactive tooltips, bookmarks, and buttons, and finally an AI-generated narrative summary using **Copilot in Power BI**.

By the end of this lab, you will have transformed a working report into a board-ready, interactive analytics experience that is published, shared, refreshed, and enhanced according to modern Power BI practice.

> **Note**: A pre-built copy of the Store Performance report (`StorePerformanceReport.pbix`) is provided on the lab VM at `C:\LabFiles\`, so you can complete this lab whether or not you finished HOL 1.

## 📋 Objectives

After completing this lab you will be able to:

- Publish a Power BI Desktop report and its semantic model to a workspace in the Power BI Service.
- Build an **executive dashboard** by pinning report visuals as tiles.
- Compare and apply the three primary sharing methods — workspace roles, direct sharing, and Power BI apps.
- Configure **scheduled refresh** so the published semantic model stays current.
- Apply a layout grid and brand theme, add conditional formatting, and use backgrounds, shapes, and card effects to give the report a board-ready look.
- Import a **certified custom visual** from AppSource and configure it against Contoso data.
- Add interactivity with tooltip pages, bookmarks, and buttons.
- Generate an AI-narrative summary of the report using **Copilot in Power BI** and validate the output against the visuals.

## ✅ Pre-requisites

Before starting this lab you should have:

- **Store Performance report** (`StorePerformanceReport.pbix`) — provided for you at `C:\LabFiles\` on the lab virtual machine. No prior lab or setup is required.
- **Basic familiarity with Power BI Desktop** — report pages, visuals, and the Visualizations pane.
- **Basic understanding of the Power BI Service** — workspaces, reports, dashboards, and semantic models (datasets).

> **Note**: Some features used in this lab — sharing, app publishing, scheduled refresh, AppSource visuals, and Copilot — depend on tenant settings, licensing, and administrator permissions. Where a feature is not available in the lab environment, the guide instructs you to review the option and document the dependency instead.

## 🏗️ Architecture

The workflow in this lab follows the standard Power BI publish-and-share lifecycle. A report authored in **Power BI Desktop** is published to a **workspace** in the **Power BI Service**, where it is stored alongside its **semantic model**. Key visuals from the report are pinned as tiles to a **dashboard** for an at-a-glance executive view. Content is then distributed to consumers through **workspace roles**, **direct sharing links**, or a packaged **Power BI app**, while **scheduled refresh** keeps the semantic model up to date from its data source. Finally, the report itself is enhanced in Power BI Desktop with themes, conditional formatting, custom visuals from **AppSource**, interactive elements (tooltips, bookmarks, buttons), and an AI-generated narrative from **Copilot**, and the updated version is republished to the Service.

## 🧩 Architecture Diagram

   ![](./Images/archlab.png)

## 🔍 Explanation of Components

The architecture for this lab involves the following key components:

- **Power BI Desktop**: The free authoring tool where reports are designed, enhanced, and published from. In this lab it is used to open the existing report, apply design polish, add custom visuals and interactivity, and publish to the Service.
- **Power BI Service**: The cloud-based (SaaS) platform where published content lives. It hosts workspaces, reports, dashboards, semantic models, and apps, and provides sharing, refresh, and Copilot capabilities.
- **Workspace**: A collaborative container in the Power BI Service that stores related reports, dashboards, and semantic models, with role-based access control (Admin, Member, Contributor, Viewer).
- **Semantic Model (Dataset)**: The published data model behind the report. It holds the tables, relationships, and measures, and is the object on which scheduled refresh is configured.
- **Dashboard**: A single-page canvas in the Power BI Service composed of tiles pinned from one or more reports, designed for at-a-glance monitoring.
- **Power BI App**: A packaged, read-only distribution mechanism that bundles reports and dashboards for a broad audience with controlled navigation and permissions.
- **AppSource Custom Visuals**: Third-party and Microsoft-built visuals that extend the native visualization library with additional chart types such as gauges, KPI indicators, and word clouds.
- **Copilot in Power BI**: An AI assistant that can generate narrative summaries and insights from report pages, subject to licensing (Fabric capacity) and tenant settings.

## 🚀 Getting Started with the Lab

Welcome to the **Publish, Share, and Enhance User Experience in Power BI** hands-on lab! We've prepared a seamless environment for you to explore and learn about publishing, sharing, and enhancing Power BI content. Let's begin by making the most of this experience.

## 🖥️ Accessing Your Lab Environment

Once you're ready to dive in, your virtual machine and lab guide will be right at your fingertips within your web browser.

![](./Images/images/gs-01.png)

## 🧭 Exploring Your Lab Resources

To get a better understanding of your lab resources and credentials, navigate to the **Environment** tab.

![](./Images/images/gs-02.png)

## 🛠️ Utilizing the Split Window Feature

For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the top right corner.

![](./Images/images/gs-03.png)

## ⚙️ Managing Your Virtual Machine

Feel free to **start, stop, or restart (2)** your virtual machine as needed from the **Resources (1)** tab. Your experience is in your hands!

![](./Images/images/gs-04.png)

## 📖 Lab Guide Zoom In/Zoom Out

To adjust the zoom level for the environment page, click the **A↕ : 100%** icon located next to the timer in the lab environment.

![](./Images/images/gs-05.png)

## Resize the Virtual Machine View

Use the **slider (three vertical dots)** located between the **Virtual Machine** and the **Lab Guide** panes to adjust the display size, allowing you to customize the layout based on your preference.

![slider](./Images/images/gs-06.png)

## 🔑 Let's Get Started with the Power BI Service

1. On the Lab VM, open **Microsoft Edge** from the desktop. In a new tab, navigate to **Microsoft Fabric** by copying and pasting the following URL into the address bar:

   ```
   https://app.powerbi.com/
   ```
   
1. On the **Sign in** page, enter the following email and click **Submit (2)**.

   - **Email: (1)** <inject key="AzureAdUserEmail"></inject>

     ![](./Images/gs-08.png)

1. On the **Enter password** screen, enter the following password and click **Sign in (2)**.

   - **Password: (1)** <inject key="AzureAdUserPassword"></inject>

     ![](./Images/gs-09.png)

1. When prompted with **Stay signed in?**, click **Yes**.

   ![](./Images/gs-10.png)

   > **Note**: If you see a pop-up saying that the Microsoft Fabric trial has been automatically assigned to the user, click **OK**.
   >
   > ![](./Images/images/note.png)


1. From the Power BI home page, select **Account Manager (1)** from the top-right corner and click **Start trial (2)** to activate the Microsoft Fabric trial.

   ![](./Images/gs-11.png)

   > **Note:** The trial is enabled to ensure that your account has access to Power BI Pro and Fabric features, including sharing and Copilot experiences used later in this lab.

1. On the **Your Power BI trial is active** window, click **Got it**.

   ![](./Images/gs-12.png)
   
1. Click the **Account manager (1)** icon again and, under the **Profile** section, verify that the **Trial Status (2)** shows the number of days remaining.

   ![](./Images/gs-14.png)

1. Keep this browser session signed in — you will return to the Power BI Service after publishing your report from Power BI Desktop.

## 📝 Summary

In this lab, you took the Contoso Retail **Store Performance** report from a local `.pbix` file to a published, shared, refreshed, and design-polished business asset in the Power BI Service. You published to a workspace, built an executive dashboard, walked through workspace roles / direct sharing / app-based distribution, and configured scheduled refresh. You then applied a brand theme with conditional formatting, added backgrounds and card effects, brought in a certified custom visual from AppSource, wired up tooltips and bookmarks with a toggle button, and generated an AI-narrative summary with Copilot. The result is a board-ready report that stays current on its own and can be delivered to leadership through the sharing channel that fits their audience.

## 🆘 Lab Support

If you need any assistance at any point during the lab, please contact us at **cloudlabs-support@spektrasystems.com**. We are available 24/7 to help you out.

Learner Support Contacts:

- Email Support: cloudlabs-support@spektrasystems.com
- Live Chat Support: https://cloudlabs.ai/labs-support

Now, click on **Next** from the lower right corner to move on to the next page.

![](./Images/gs-next.png)

### Happy Learning!!