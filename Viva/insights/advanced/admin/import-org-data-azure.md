---
ms.date: 08/6/2024
title: Import organizational data with Azure blob import
description: Learn how to import organizational data into Viva Insights through an Azure blob import.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import organizational data with Azure blob import  

>[!IMPORTANT]
> This feature is for public preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader release.

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of five ways: through Microsoft Entra ID, which is the default source; through individual .csv files that you as an Insights Administrator upload directly to Viva Insights; through an API-based import; through Workday; or through an Azure blob import that you, your source system admin, and your Azure contributor set up.

This article covers the fifth option, Azure blob import.

With an Azure blob import, your Azure contributor creates a blob container on the Azure portal, and your source system admin configures a periodic export of a .csv file to the blob container's location. You can then set up Viva Insights to automatically pull organization data from the .csv file within this location.

### Workflow

1. Setup:

    1. The Azure contributor creates a secure blob container on the Azure portal. The blob store location should be secure for sensitive organizational data, and it needs to be set up in the customer’s Azure subscription.

    2. If the Azure contributor prefers service principal authorization, the Azure contributor authorizes the service principal and provides the blob URL to the Insights admin and source system admin by sharing it in a secure way. If the Azure contributor does *not* prefer service principal authorization, they generate a SAS URL and provide it to the Insights admin and source system admin.

    3. The source system admin prepares the data in a .csv file and .json mapping file, and configures a periodic export of the .csv file from the HR source system to the blob container.

    4. The Insights admin enters the URL in the Viva Insights app to turn on the import from the Azure blob store location. The Insights admin also uploads the .json mapping file provided by the source system admin.

2. Validation: Viva Insights validates the data. (If validation isn’t successful, you can choose from a few options described in [Validation fails](#validation-fails).)

3. Processing: Viva Insights processes the data. (If processing isn’t successful, you can choose from a few options described in [Processing fails](#processing-fails).)

After the data successfully validates and processes, the overall data-import task is complete.

## Setup

### 1. Create a secure blob container

*Applies to: Azure contributor*

1. Open a browser and sign in to your organization’s Azure portal. 

2. Under **Azure services**, select **Storage accounts**.

3. Under **Storage accounts** at the top left, select **Create** to create a new storage account.

4. Under **Project details**, use the default settings.

5. Under **Instance details**, enter a storage account name and select your region. For Performance and Redundancy, you can use the default settings unless you need to make changes.

6. At the bottom, select **Next: Advanced**.

7. On the Advanced page, select "Require secure transfer for REST API operations," "Enable storage account key access," and "Enable hierarchical namespace." For "Minimum TLS version," select at least **Version 1.2**.

8. For all other Advanced settings, you can use the default settings unless you need to make changes.

9. At the bottom, select **Next: Networking**.

10. Under **Network connectivity**, select **Enable public access from all networks** or **Enabled from selected virtual networks and IP addresses**. If you select the second option, under **Firewall**, select **Add your client IP address** and provide the IP address for the allow list shared by the Insights admin.

11. Under **Network routing**, select your routing preference.

12. At the bottom, select **Next: Data protection**.  

13. On the Data protection page, you can use the default settings unless you need to make changes.

14. At the bottom, select **Next: Encryption**.

15. On the Encryption page, you can use the default settings unless you need to make changes.

16. At the bottom, select **Next: Tags**.

17. Optional: Add tags to the account.  

18. At the bottom, select **Next: Review**.

19. Review your selections. Then, at the bottom left, select **Create**.

20. On the next page, a message will appear that says, “Deployment is in progress.” Once deployment is complete, your storage account and its settings will appear.

21. On the left, under **Data storage**, select **Containers**.

22. To create a new container, at the top, select **Container**. Then, on the right, enter a name for the container, like “hrupload.” At the bottom, select **Create**.

### 2. Authorize the blob container

*Applies to: Azure contributor and Storage Blob Data Contributor*

Next, you’ll need to create a blob SAS URL for authorization, or a blob URL if you’re using service principal authorization. Service principal authorization is the recommended and more secure approach. The blob SAS token does not have any built-in auditing capabilities. Follow the appropriate steps below for the method you choose.

**For service principal authorization:**  

1. On the left panel, select **Access Control**.

2. At the top, select **Role assignments**. Select **Add**, then select **Add role assignment**.  

3. In the list of roles, find and select **Storage Blob Data Reader**.

4. Next to **Members**, select **Select members**. In the search field on the right, enter **Workplace Analytics**, and select it.  

5. At the bottom left, select **Review + assign**.

6. On the left panel, under **Data storage**, select **Containers**. 

7. Select the storage container you created in the above steps. 

8. On the left panel, under **Settings**, select **Properties**. 

9. Copy and securely share the URL with the Insights admin and the source system admin.

**For SAS URL authorization:**

1. When the new storage container you created appears, select it. Then, on the left under **Settings**, select **Access policy**. 

2. Under **Stored access policies**, select **Add policy**. Provide a unique identifier, such as “BlobStore.” Select **Read** and **List** permissions. Select a start time a few minutes in the past and an end time one year from now. 

3. On the left under **Settings**, select **Shared access tokens**. 

4. You can use the default option under **Signing key**. Under **Stored access policy**, select the policy created above. This will auto-populate the expiry window and permissions list. 

5. For **Allowed IP addresses** and **Allowed protocols**, you can use the default settings. 

6. Select **Generate SAS token and URL**. 

7. Copy and securely share the blob SAS URL with the Insights admin. 

8. Let the source system admin know, who will populate the data in this container. They will need Storage Blob Data Contributor access.  


### 3. Set up Viva Insights to import data from the blob location

*Applies to: Insights admin*

1. Start the import from one of two places: the **Data hub** page, or the **Organizational data** page under **Data connections**.

    1. From **Data hub**:
        1. In the **Data source** section, under **Azure blob import**, select **Start**.

    2. From **Data connections**:
        1. Next to **Current source**, select **Manage data sources**.
        1. An Azure blob import window appears. Select **Start**.

2. Under **Connection name**, enter a unique name for the import.

3. Under **Authorization type**, select **Service Principal Authorization**, or **SAS URL Authorization**. Your selection here depends on the authorization method used by your Azure contributor in Step 2 above.  

4. Send your Azure contributor your IP address for the allow list.

5. Enter the **Blob SAS URL** or the **Blob URL** for the import provided to you by the Azure contributor in Step 2. 

6. Upload the .json mapping file provided to you by the Source system admin.

7. Select **Enabled**, then select **Save**. 

8. If you see an error message, check to make sure you followed all the steps outlined above, and check to ensure the blob SAS URL or blob URL you entered is accurate. Select **Retry**. 

### 4. Prepare org data .csv file and .json mapping file and send to blob store

*Applies to: Source system admin*

**Task 1 - Prepare your data**

Before you start exporting and importing your data, make sure you prepare your file according to steps 1 through 4 in [Prepare an organizational data file upload](./prepare-org-data.md). You can also use this document to learn about required and reserved optional attributes.

Tips for preparing your data

* For new data, include full historical data for all employees.

* Import organizational data for all employees in the company, including licensed and non-licensed employees.

* Refer to the [sample .csv template](https://download.microsoft.com/download/7/a/1/7a17695f-d401-4abd-aeef-e72158084160/OrganizationalDataFileTemplateDataImport.xlsx) for data structure and guidelines to avoid common issues like too many or too few unique values, redundant fields, invalid data formats, and more. [Learn more about file rules and validation errors](./rules-validation-errors.md).

**Task 2 - Export data from your source system**

At the frequency you decide (once a month, once a week, etc.) programmatically export organizational data from your source system as a .csv file. Refer to this [sample .csv template](https://go.microsoft.com/fwlink/?linkid=2224590). Format the file according to [our guidelines](./prepare-org-data.md).

To manually upload the file to the blob location created by the Azure contributor in Step 1, send the .csv file to the Azure contributor or Storage Blob Data contributor (unless you're already assigned these roles), and ask them to follow these steps:

1. Open a browser and enter the blob SAS URL provided by the Azure contributor. 

2. At the top, select **Upload**. Then, on the right, upload the .csv file you created using the instructions above.

**Prepare .json mapping file and send it to the Insights admin**

Indicate the type of refresh you're performing and how Viva Insights should map your fields:

* ``` “DatasetType”: “HR” ``` (line 2). Leave this as-is. 

* ``` “IsBootstrap”: ``` (line 3). Use “true” to indicate a full refresh and "false" to indicate an incremental refresh.  

* "Mapping": If you use names other than what Viva Insights uses, change each column header name to match what you use in your source system.

>[!IMPORTANT]
> Remove any fields that aren't present in your .csv file.

**Mapping example**

The following example represents one field you'll find in the sample .json file:

```
"PersonId": { 
    "name": "PersonId", 
    "type": "EmailType"
```

* ``` "PersonId": { ``` corresponds to the source column name. 

* ``` “name” : “PersonId” ```, corresponds to the Viva Insights field name. 

* ``` "type": "EmailType" ``` corresponds to the field’s data type.

Let’s say that instead of PersonId, your source system uses Employee for this field header. To make sure your fields are mapped correctly, you’ll want to edit the first line below, so it looks like this:

```
"Employee": {
    "name": "PersonId",
    "type": "EmailType"
```
When you upload your data, your Employee field will become PersonId in Viva Insights.

Then, send the .json mapping file to the Insights admin to upload in Insights while setting up the connection for the Azure blob import.

### 5. Validation

*Applies to: Insights admin*

After the source system admin exports the data and you set up the import, the app starts validating. In most cases, file validation should complete quickly.

After this phase completes, validation has either succeeded or failed. Depending on the outcome, you'll either receive a success status or a failure status in Import history table in **Organizational data > Data connections**.

For information about what happens next, go to the appropriate section:

* [Validation succeeds](#validation-succeeds)
* [Validation fails](#validation-fails)

#### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you'll see a “Processing” status on the **Import history** table.

After processing completes, it's either succeeded or failed. Depending on the outcome, you'll either find a “Success” or “Failed” status in the **Import history** table.

##### Processing succeeds

When you find the “Success” status in the **Import history** table, the upload process is complete.

After you receive the “Success” status, you can:

* Select the view (eye) icon to see a summary of the validation results.
* Select the mapping icon to see the mapping settings for the workflow.

>[!Note]
> Each tenant can have only one import in progress at a time. You need to complete the workflow of one data file, which means you either guide it to a successful validation and processing or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the **Data connections** tab.

##### Processing fails

If processing fails, you'll find a “Processing failed” status in the **Import history** table. For processing to succeed, the source system admin needs to correct errors and push the data to Viva Insights again.

>[!Note]
> Processing failures are generally due to backend errors. If you're seeing persistent processing failures and you’ve corrected the data in your imported file, [log a support ticket with us](/microsoft-365/admin/get-help-support).

#### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the source system admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the source system admin so they know what to correct before sending the data again.

The source system admin might find the following section helpful to fix data errors in their export file.

#### About errors in data
*Applies to: Source system admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until the data source admin fixes the source data.

Refer to [Prepare organizational data](./prepare-org-data.md) for specific formatting rules that might help resolve errors you encounter.

[Learn more about validation errors and warnings](..//admin/rules-validation-errors.md#validation-errors-and-warnings).

#### Suspended state
If you see a "Suspended" status in the **Import history** table or when you select **Manage data sources**, this means your authorization credentials have expired or access has been revoked. You'll need to update your credentials and reconnect the data source.

### Manage data source and make changes
*Applies to: Insights admin*

After you've set up your data import, use the steps below to make changes like setting a new blob store URL, or turning off automated imports.

1. On the **Organizational data** page under **Data connections**, select **Manage data sources**.
2. Under **Azure blob import**, select **Manage**.

On the next page, you can edit the connection name, the blob SAS URL, or the blob URL. If you update the SAS URL or URI, the new location will be used for future data refreshes. 

You can also turn automated imports on or off. When you're done, select **Save**.

To replace or edit the organizational data using the existing blob SAS URL or blob URL, contact your source system admin. When you import data to Viva Insights, you'll either perform a full or an incremental refresh. If you want to delete fields, you can use a full refresh to do so.

#### How to indicate a full or incremental refresh

1. In the .json mapping file, go to line 3.
1. Update the ``` “IsBootstrap”: ``` property to one of the following:
    1. For a full refresh, use ``` “IsBootstrap” : “true” ```.
    1. For an incremental refresh, use ``` “IsBootstrap” : “false”```.

When your import runs, Viva Insights will start to process your data either as a full or incremental refresh, depending on what you specified in the .json mapping file.

#### Refresh types

**Full**

When you perform a full refresh, you're replacing all your organization's data in Viva Insights—that is, you overwrite what you’ve already imported. When you perform a full refresh, make sure to provide data for all licensed and unlicensed employees (meaning those who have a Viva Insights subscription and those who don't). We describe what fields to provide later in this article.

You can use a full refresh to delete fields, because fields you leave out won't show up in your data. We talk about deleting data in the next section.

**Deleting fields with full refreshes**

To delete fields with a full refresh, export your data as a .csv that contains all fields except the fields you want to delete. Because a full refresh replaces existing data, you'll end up with every field except the ones you left out during the import.

**Incremental**

Perform an incremental refresh when you only want to add some new information to organizational data you’ve already uploaded to Viva Insights. Here's what you can do with an incremental refresh:

* Add new employees
* Add new attributes for existing employees
* Add new attributes for new employees
* Edit existing employees’ attributes 

Here are a couple of examples of when you might perform an incremental refresh:

**Example – adding new hires**

Say you want to add five new hires to your organizational data. During the import, you’d include:

* Five rows that contain new employee data.
* Required attributes: PersonId,  ManagerId, Organization, and EffectiveDate.
* All reserved optional fields (for example, HireDate) that you've already imported to Viva Insights. 

After the import finishes, the only change you'd notice is five new rows and their values.

**Example – adding a new attribute**

Maybe you want to add an optional reserved attribute that wasn’t in your data before—let's say **Location** — for all existing employees. When you go to import your data, you'd only include the **Location**, **PersonId**, and **EffectiveDate**, with current and historical values for each employee, in your .csv file. After the import finishes, you’d find the same data that was there before, with the exception of a new column for each employee, **Location**.

#### Fields to include in the .csv file for full and incremental refreshes

For the refresh types listed below, include the fields in the following table within your .csv file. Format these fields according to our guidelines in [Prepare organizational data](./prepare-org-data.md).

| For this kind of refresh | Include these fields in the .csv file | With these values | For these employees |
|----|----|----|----|
| **Full** | PersonId | Current </br> <br> All historical | All | 
|   | ManagerId | Current </br> <br> All historical | All |
|   | Organization | Current </br> <br> All historical | All |
|   | EffectiveDate | Current </br> <br> All historical | All |
|   | All reserved optional fields (for example, **HireDate**) that you’ve already imported to Viva Insights | Current </br> <br> All historical | All |
| **Full** (for deleting reserved optional fields) | PersonId | Current </br> <br> All historical | All | 
|   | ManagerId | Current </br> <br> All historical | All |
|  | Organization | Current </br> <br> All historical | All |
|   | EffectiveDate | Current </br> <br> All historical | All |
|   | All reserved optional fields (for example, **HireDate**) you’ve already imported to Viva Insights, except the reserved optional fields you want to delete | Current (except for to-be-deleted fields) </br> <br> All historical (except for to-be-deleted fields) | All |
| **Incremental** (for adding new fields or editing existing fields, but *not* adding new employees) | PersonId | Current </br> <br> All since the last upload (refer to note below) | All |
|   | EffectiveDate | Current </br> <br> All since the last upload (refer to note below) | All |
|   | Any reserved optional fields (for example, **HireDate**) you want to add | Current </br> <br> All since the last upload (refer to note below) | All |
| **Incremental** (for adding new employees) | PersonId | Current </br> <br> All since the last upload (refer to note below) | New employees only |
|   | ManagerId | Current </br> <br> All since the last upload | New employees only |
|  | Organization | Current </br> <br> All since the last upload | New employees only |
|   | EffectiveDate | Current </br> <br> All since the last upload | New employees only |
|   | All reserved optional fields (for example, **HireDate**) that you’ve already imported to Viva Insights | Current </br> <br> All since the last upload | New employees only |

>[!Note]
> "All historical": Values for previous time periods. For example, if you include monthly data, then you'd include values for every month leading up to this one. When you're first starting to use Viva Insights, 13 months' worth of data is recommended. After that, it’s recommended to update data regularly so it builds into 27 months' worth of data. </br> <br>
> "All values since the last upload": Values for the period between uploads. For example, if the last upload was in March and now it’s July, include values for April, May, and June.

## Related topics

[Prepare organizational data](prepare-org-data.md)