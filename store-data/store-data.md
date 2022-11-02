# Create your Virtual Cloud Network and Related ComponentsObject Practice


## Introduction

**Create and Load object Storage Bucket**

Create Object Storage Bucket and load Airport Sample database.

_Estimated Time:_ 15 minutes

### Objectives

In this lab, you will be guided through the following tasks:

- Download and unzip airportdb data
- Create Object Storage bucket
- Upload airportdb data



### Prerequisites

- An Oracle Free Tier or Paid Cloud Account
- A web browser
- Login to OCI to and on OCI Dashboard (

## Task 1: Download and unzip airportdb data to your local machine

1. Download the airportdb sample database  The download is approximately 640 MBs in size.

    ```bash
    <copy>wget https://downloads.mysql.com/docs/airport-db.zip</copy>
    ```

2. Unzip  the airportdb sample database  

    ```bash
    <copy>unzip airport-db.zip</copy>
    ```

## Task 2: Create Object Storage bucket

1. Sign in to OCI using your tenant name, user name and password.
2. Once signed in select the compartment assigned to you from drop down menu on left part of the screen
3. From the Console navigation menu, click **Storage**.
4. Under Object Storage, click Buckets

    **NOTE:** Ensure the correct Compartment is selected : Select (root)

    ![cloud storage bucket](./images/cloud-storage-bucket.png "cloud-storage-bucket")

5. Click Create Bucket. The Create Bucket pane is displayed.
6. Enter a Bucket Name. Avoid entering confidential information.
7. Under Default Storage Tier, click Standard. Leave all the other fields at their default values.
8. Click Create

    ![press bucket button](./images/press-bucket-button.png "press-bucket-button")

## Task 3: Upload airportdb data

1. In the Buckets page, click the name of the bucket you are going to load images into. The bucket's details page is displayed.
2. Under Resources, click Objects to display the list of objects in the bucket.
3. Click create folder and set it to **airport-bd**
4. Click Upload. The Upload Objects pane is displayed.
5. Select all of the files from the unzippe airportdb local folder , or click open to load all of the ylocal files

   ![bucket detail](./images/bucket-detail.png"bucket-detail.png")

**You may now proceed to the next lab**

## Acknowledgements

- **Author** - Perside Foster, MySQL Solution Engineering, Harsh Nayak , MySQL Solution Engineering 
- **Contributors** - Frédéric Descamps, MySQL Community  Manager, Orlando Gentil, Principal Training Lead and Evangelist
- **Last Updated By/Date** - Perside Foster, MySQL Solution Engineering, November 2022

