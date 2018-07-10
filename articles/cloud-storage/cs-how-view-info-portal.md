---
title: How to view Cloud Storage information in the UKCloud Portal | UKCloud Ltd
description: Describes how to access information about your Cloud Storage service in the UKCloud Portal
services: cloud-storage
author: Sue Highmoor

toc_rootlink: How To
toc_sub1:
toc_sub2:
toc_sub3:
toc_sub4:
toc_title: View Cloud Storage information in the UKCloud Portal
toc_fullpath: How To/cs-how-view-info-portals.md
toc_mdlink: cs-how-view-info-portals.md
---

# How to view Cloud Storage information in the UKCloud Portal

## Overview

Cloud Storage is UKCloud's object storage solution based on Dell EMC Elastic Cloud Storage (ECS). Although you'll mostly interact with Cloud Storage through the API, the UKCloud Portal provides access to some information about your service.

Within the UKCloud Portal you can:

- View information about the namespaces within your Cloud Storage environment
- View a list of users with access to a namespace
- Reset the secret key for a Cloud Storage user
- View information about the buckets within a namespace
- View a graphical representation of the storage consumed over the last 30 days

### Intended audience

To complete the steps in this guide you must have been granted access to the relevant namespace.

## Granting Portal permissions for Cloud Storage

To view Cloud Storage information in the Portal, users must be granted access to the relevant namespace. Once access is granted, the user will be able to see the namespace, list the buckets in the namespace and reset the secret key. They will also be able to see consumption data for
namespaces and buckets, with a graphical representation of average consumption for buckets.

To grant Portal permissions for Cloud Storage:

1. Log in to the UKCloud Portal and select your account.

    For more detailed instructions, see the [*Getting Started Guide for UKCloud Portal*](https://portal.ukcloud.com/support/knowledge_centre/0435318d-a94b-41bb-a4ff-a52adbe863e5).

2. In the Portal navigation panel, expand the **CONTACTS** option and select **All Contacts**.

    ![All Contacts menu option in UKCloud Portal](images/cs-portal-mnu-all-contacts.png)

3. Find the contact for whom you want to grant permissions and click the **Edit** button.

    ![Edit contact button](images/cs-portal-btn-edit-contact.png)

4. Click the *Permissions* tab.

    ![Permissions tab](images/cs-portal-tab-permissions.png)

5. Scroll down to the *Permissions for Cloud Storage* section and select the **Access** check box for the relevant namespace.

    ![Cloud Storage permissions](images/cs-portal-permissions.png)

## Viewing namespace and bucket information

In ECS, objects are stored in buckets. In the UKCloud Portal, you can drill down through your namespaces to see the allocated buckets available in your Cloud Storage service. You can also view storage consumption over the last 30 days.

![Structure of objects in ECS](images/cs-namespace-buckets.png)

> [!NOTE]
> It's not possible to view objects within the UKCloud Portal.

1. Log in to the UKCloud Portal and select your account.

    For more detailed instructions, see the [*Getting Started Guide for UKCloud Portal*](https://portal.ukcloud.com/support/knowledge_centre/0435318d-a94b-41bb-a4ff-a52adbe863e5).

2. In the Portal navigation panel, expand the **Cloud Storage** option and select **ECS**.

    ![Cloud Storage menu option in UKCloud Portal](images/cs-portal-mnu-cloud-storage.png)

3. The *Storage* tab lists the namespaces within the currently selected account. You can see:

    - The number of buckets in the namespace
    - The total amount of storage (in GiB) currently consumed by the objects in all the buckets in the namespace
    - The service level of the namespace:
        - STANDARD --- data is stored in a single data centre
        - ENHANCED --- data is stored in a primary named data centre and copied to a second geographically remote data centre

    ![Namespaces page](images/cs-portal-namespaces.png)

4. To list the buckets in a namespace, click the **Buckets** button for the namespace.

    ![Buckets button](images/cs-portal-btn-buckets.png)

5. On the *Buckets* tab, you can see the following information for each bucket in the selected namespace:

    - The type of bucket: S3 or ATMOS
    - The total amount of storage (in GiB) currently consumed by the objects in the bucket
    - The number of objects in the bucket

    ![Buckets page](images/cs-portal-buckets.png)

6. To view a graph that shows the amount of storage (in GiB) consumed by the objects in the bucket over the last 30 days, click the **Show Consumption** button for the bucket.

    ![Consumption information](images/cs-portal-consumption.png)

## Resetting your secret key

Each user who can access Cloud Storage has an associated secret key to enable secure authentication. When attempting to access Cloud Storage, you must specify the appropriate secret key. If you forget the secret key for your user ID, you can reset it in the UKCloud Portal.

> [!NOTE]
> For security purposes, the UKCloud Portal does not display secret keys, if you forget your secret key, you must reset it to generate a new one.

1. Log in to the UKCloud Portal and select your account.

    For more detailed instructions, see the [*Getting Started Guide for UKCloud Portal*](https://portal.ukcloud.com/support/knowledge_centre/0435318d-a94b-41bb-a4ff-a52adbe863e5).

2. In the Portal navigation panel, expand the **Cloud Storage** option and select **ECS**.

    ![Cloud Storage menu option in UKCloud Portal](images/cs-portal-mnu-cloud-storage.png)

3. Click the **Users** button for the namespace for which you want to reset the secret key.

    ![Users button](images/cs-portal-btn-users.png)

4. The *Users* tab lists the different user IDs associated with the namespace.

    ![Users page](images/cs-portal-users.png)

5. Click the **Reset Secret** button next to the appropriate user ID.

6. Click **OK** to confirm that you want to reset the secret key.

    ![Reset Secret dialog box](images/cs-portal-reset-secret.png)

7. Stay on the current page until a popup dialog box displays the new secret key.

    ![New secret key](images/cs-portal-new-key.png)

8. Make a note of the key and then click **Close**.

    > [!NOTE]
    > After you close this dialog box, you will not be able to see the secret key again in the UKCloud Portal. If you do not make a note of the secret key or if you forget or lose it, you will need to reset it again.

## Next steps

This guide has shown you how you can view information about your Cloud Storage service in the UKCloud Portal. For information about how to use the service, see the following articles in the Knowledge Centre:

- [*Getting Started Guide for Cloud Storage*](https://portal.ukcloud.com/support/knowledge_centre/e07b908f-e93e-42f8-b833-aff391511862)
- [*Blueprint -- Using storage gateways with Cloud Storage*](https://portal.ukcloud.com/support/knowledge_centre/85dc54ff-7d21-43ac-9cfa-88e87de7ba27)
- [*Blueprint -- Using file browsers with Cloud Storage*](https://portal.ukcloud.com/support/knowledge_centre/ba19c6c0-a123-4d0b-bc56-b3fdc3513cb0)

## Feedback

If you have any comments on this document or any other aspect of your UKCloud experience, send them to <products@ukcloud.com>.

&copy; [UKCloud Ltd](http://ukcloud.com), 2018. All Rights Reserved. UKC-GEN-581