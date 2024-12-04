+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 4b01ed2bd3704465bd3b9ddcaf6f1324 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| BUSONGAN, DEMIRAYE-ANNE          | DATE PERFORMED: 11     |          |
|                                  | SEPT 2024              |          |
+----------------------------------+------------------------+----------+
| IDC1                             | DATE SUBMITTED: 11     |          |
|                                  | SEPT 2024              |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image2.png){width="6.538194444444445in"
height="2.9270833333333335in"}![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image3.png){width="4.135416666666667in"
height="1.8020833333333333in"}\
NOTE TO DEMI (VERSION 22):\
![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image4.png){width="4.624048556430446in"
height="4.548449256342957in"}

Complete this lab as follows:

1.  Use the service---status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  (+) acpid                              (-) alsa-utils

  (+) cups                               (-) bluetooth

  (+) cups-browsed                       (-) speech-dispatcher

  (+) dbus                               (-) keyboard-setup.sh

  (+) openvpn                            (-) hwclock.sh
  -----------------------------------------------------------------------

![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image5.png){width="4.89727580927384in"
height="2.846218285214348in"}![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image6.png){width="4.895329177602799in"
height="3.2737128171478567in"}\
Note: service --status-all\|grep '\[-\\\]', service --status-all\|grep
'\[-\\\]'

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd (Version 2024)

-   Sudo modprobe Bluetooth\
    ![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image7.png){width="5.025758967629046in"
    height="2.646234689413823in"}

![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image8.png){width="4.359946412948381in"
height="1.1875in"}

1.  Check the status of the Bluetooth service. What is its status?

-   We could see from the image below that the Bluetooth is currently
    inactive or dead

SS:
![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image9.png){width="6.084302274715661in"
height="1.4123950131233596in"}

1.  Check the status of the cups services. Since when was it running?

-   Based on the image the service cups Started Running on Wednesday
    2024-09-11 at exactly 8:25 CST, 41mins prior.

SS:
![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image10.png){width="7.027083333333334in"
height="3.2729166666666667in"}

1.  Stop cups services. **(SS in NUMBER 6)**

2.  Verify if the service was stopped.
    ![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image11.png){width="7.027083333333334in"
    height="3.3430555555555554in"}

3.  Restart the cups services **(SS in NUMBER 8)**

4.  Verify if the service was restarted.

![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image12.png){width="7.027083333333334in"
height="3.376388888888889in"}
