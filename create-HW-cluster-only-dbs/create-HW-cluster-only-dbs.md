# Create MySQL Database HeatWave Airport Sample database and Cluster

## Introduction

In this lab, you will create, configure, and load a MySQL DB System  Finally you will add a HeatWave Cluster comprise of two or more HeatWave nodes.  

_Estimated Time:_ 20 minutes

### Objectives

In this lab, you will be guided through the following tasks:

- Create MySQL Database for HeatWave (DB System) and Load sample database
- Add a HeatWave Cluster to MySQL Database System

### Prerequisites

- An Oracle Trial or Paid Cloud Account
- Some Experience with MySQL Shell
- Must Complete Lab 1

## Task 1: Create MySQL Database for HeatWave DB System

1. Go to Navigation Menu
         Databases
         MySQL
         DB Systems
    ![MDS](./images/mysql-menu.png "mysql menu")

2. Click 'Create MySQL DB System'
    ![MDS](./images/mysql-create.png "mysql create ")

3. Create MySQL DB System dialog complete the fields in each section

    - Provide basic information for the DB System
    - Setup your required DB System
    - Create Administrator credentials
    - Configure Networking
    - Configure placement
    - Configure hardware
    - Exclude Backups
    - Advanced Options - Data Import

4. Provide basic information for the DB System:

    Select Compartment **heatwave**

    Enter Name

    ```bash
    <copy>MDS-HW</copy>
    ```

    Enter Description

    ```bash
    <copy>MySQL Database Service HeatWave instance</copy>
    ```

    Select **HeatWave** to specify a HeatWave DB System
    ![MDS](./images/mysql-heatwave.png "mysql heatwave ")

5. Create Administrator Credentials

    **Enter Username** (write username to notepad for later use)

    **Enter Password** (write password to notepad for later use)

    **Confirm Password** (value should match password for later use)

    ![MDS](./images/mysql-password.png "mysql password ")

6. On Configure networking, keep the default values

    Virtual Cloud Network: **MDS-VCN**

    Subnet: **Private Subnet-MDS-VCN (Regional)**

    ![MDS](./images/mysql-vcn.png "mysql vcn ")

7. On Configure placement under 'Availability Domain'

    Select AD-3

    Do not check 'Choose a Fault Domain' for this DB System.

    ![MDS](./images/mysql-fault-domain.png "mysql fault domain ")

8. On Configure hardware, keep default shape as **MySQL.HeatWave.VM.Standard.E3**

    Data Storage Size (GB) Set value to:  **1024**

    ```bash
    <copy>1024</copy>
    ```

    ![MDS](./images/mysql-hardware.png "mysql hardware ")

9. On Configure Backups, disable 'Enable Automatic Backup'

    ![MDS](./images/mysql-backup.png "mysql backup ")

10. Click on Show Advanced Options

11. Go to the Networking tab, in the Hostname field enter (same as DB System Name):

    ```bash
        <copy>MDS-HW</copy> 
    ```
12. Go to the Data Import tab - Use the Data Import tab of the Create DB System panel to import data from a MySQL Shell dump in an Object Storage bucket.

13. Click here to create a PAR URL for an existing bucket: (Optional) Click the link to create a PAR URL for an existing bucket, and provide the following information:

14. Select a bucket in CompartmentName: Select the Object Storage bucket that contains your dump.
15. Select the prefix: Select the prefix from the list of valid prefixes.
16. Create and set PAR URL: Click the option to generate the PAR URL and add it to the PAR Source URL option.
17. Your PAR Source URL entry should look like this:

    ![mysql PARA link ](./images/mysql-link.png "mysql link ")

18. Review **Create MySQL DB System**  Screen

    ![MDS](./images/mysql_create_db.png "mysql create db")

    Click the '**Create**' button

19. The New MySQL DB System will be ready to use after a few minutes

    The state will be shown as 'Creating' during the creation
    ![MDS](./images/mysql-create-button.png "mysql create button ")

20. The state 'Active' indicates that the DB System is ready for use

    On MDS-HW Page, check the MySQL Endpoint (Private IP Address)

    ![MDS](./images/mysql-create-button.png"mysql create button ")

## Task 2: Add a HeatWave Cluster to MDS-HW MySQL Database System

1. Open the navigation menu  
    Databases
    MySQL
    DB Systems
2. Choose the root Compartment. A list of DB Systems is displayed.
    ![Connect](./images/mysql-add-heatwave.png "mysql add heatwave ")
3. In the list of DB Systems, click the **MDS-HW** system. click **More Action ->  Add HeatWave Cluster**.
    ![Connect](./images/mysql-add-heat-vcn.png "mysql add heat vcn ")
4. **Set Node Count to 2 for this Lab Click** ???Add HeatWave Cluster??? to create the HeatWave cluster
    ![Connect](./images/mysql-add-heat-estimate.png "mysql add-heat estimate")
5. HeatWave creation will take about 10 minutes. From the DB display page scroll down to the Resources section. Click the **HeatWave** link. Your completed HeatWave Cluster Information section will look like this:
    ![Connect](./images/mysql-heat-cluster-complete.png "mysql heat cluster complete ")

## Acknowledgements

- **Author** - Perside Foster, MySQL Solution Engineering

- **Contributors** - Mndy Pang, Principal Product Manager, Salil Pradhan, Principal Product Manager, Nick Mader, MySQL Global Channel Enablement & Strategy Manager
- **Last Updated By/Date** - Perside Foster, MySQL Solution Engineering, May 2022
