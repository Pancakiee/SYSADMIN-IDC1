+--------------------------------+--------------------------+----------+
| ![](vertopal_43e2              |                          |          |
| 9b24ee064f8bad9924cc867d6832/m |                          |          |
| edia/image1.png){width="2.4in" |                          |          |
| height="0.5881944444444445in"} |                          |          |
|                                |                          |          |
| SCHOOL OF INFORMATION AND      |                          |          |
| TECHNOLOGY                     |                          |          |
+--------------------------------+--------------------------+----------+
| NAME: BUSONGAN, DEMIRAYE-ANNE  | DATE PERFORMED:13 NOV    | /50      |
|                                | 2024                     |          |
+--------------------------------+--------------------------+----------+
| Section: IDC1                  | DATE SUBMITTED: 13 NOV   |          |
|                                | 2024                     |          |
+--------------------------------+--------------------------+----------+

# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

**Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos
manages secure logins through ticket-based access.

**Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

**Step 1: Initial Setup and Package Installation**

1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

*bash*

*sudo apt update*

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  *ls --l                                                                                                      ![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image3.png){width="3.542508748906387in"
  /etc/krb5.conf*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image2.png){width="3.536440288713911in"   height="1.3194706911636045in"}
  height="0.9949617235345581in"}                                                                               
  ------------------------------------------------------------------------------------------------------------ ---------------------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

*sudo apt upgrade --y*

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image4.png){width="3.35792760279965in"   ![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image5.png){width="2.8298140857392826in"
  height="0.9978532370953631in"}                                                               height="1.1731463254593175in"}
  -------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

*bash*

*sudo apt install krb5-kdc krb5-admin-server --y\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image6.png){width="7.027083333333334in"
height="2.067361111111111in"}*\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image7.png){width="7.027083333333334in"
height="3.4833333333333334in"}*\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
*

3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

*bash*

*sudo apt install krb5-user --y\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image8.png){width="7.027083333333334in"
height="4.375694444444444in"}

-   During installation, when prompted, enter the Kerberos realm you
    plan to set up, e.g., MYLAB.LOCAL.

**Step 2: Configure the Kerberos Server (VM1)**

1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

*bash*

*sudo nano /sudetc/krb5.conf*

-   Set the realm as MYLAB.LOCAL. You should also specify the KDC and
    admin server as VM1's hostname or IP address:

ini

\[libdefaults\]

default_realm = MYLAB.LOCAL

\[realms\]

MYLAB.LOCAL = {

kdc = \<VM1_IP_or_hostname\>

admin_server = \<VM1_IP_or_hostname\>

}\
![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image9.png){width="6.0737642169728785in"
height="2.448257874015748in"}

-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

*bash*

*sudo krb5_newrealm\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image10.png){width="7.027083333333334in"
height="1.3666666666666667in"}

-   You will be prompted to set a password for the Kerberos database.

3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:

*bash*

*sudo systemctl start krb5-kdc*

*sudo systemctl start krb5-admin-server*

*sudo systemctl enable krb5-kdc*

*sudo systemctl enable krb5-admin-server\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image11.png){width="7.027083333333334in"
height="1.7756944444444445in"}

**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

*bash*

*sudo kadmin.local -q \" te@MYLAB.LOCAL\"\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image12.png){width="6.625925196850393in"
height="1.1251574803149607in"}

-   Set a password for testuser.

2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

*bash*

*sudo kadmin.local -q \"listprincs\"\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image13.png){width="6.167527340332459in"
height="0.9376312335958005in"}

**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

*Bash*

*sudo nano /etc/krb5.conf\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image14.png){width="6.584251968503937in"
height="2.635784120734908in"}

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set on VM1.

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit testuser@MYLAB.LOCAL*

![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image15.png){width="7.027083333333334in"
height="0.4152777777777778in"}

-   Enter the password you set for testuser.

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*klist\
*![](vertopal_43e29b24ee064f8bad9924cc867d6832/media/image16.png){width="5.719548337707787in"
height="3.0316732283464565in"}

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.
