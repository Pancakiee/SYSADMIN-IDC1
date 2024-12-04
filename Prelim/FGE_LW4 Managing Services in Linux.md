![image](https://github.com/user-attachments/assets/76adce06-2a19-41e5-be9b-8b6a65929027)


# SYSADM1 -- Managing Services in Linux

## Requirement: 

-   A virtual machine running Linux

![image](https://github.com/user-attachments/assets/35a17ba2-977d-41a9-8040-357a77a9b6a6)

NOTE TO DEMI (VERSION 22):\
![image](https://github.com/user-attachments/assets/a3326b33-4480-4e70-9cd2-58f8380de17a)

Complete this lab as follows:

1.  Use the service---status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

 ![image](https://github.com/user-attachments/assets/563709e3-f6d1-4f9c-bfc9-0e95d80f137d)


![image](https://github.com/user-attachments/assets/11a98fb3-d9d7-4b22-998d-bc75fe96833b)
![image](https://github.com/user-attachments/assets/734472b2-f342-45ad-85ff-512cc1f90f71)


Note: service --status-all\|grep '\[-\\\]', service --status-all\|grep
'\[-\\\]'

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd (Version 2024)

-   Sudo modprobe Bluetooth\
    ![image](https://github.com/user-attachments/assets/137abe55-cf36-4415-82f9-c4bc40f48f5f)


![image](https://github.com/user-attachments/assets/f77a8aa0-4e66-4c00-9682-32cba795d984)


1.  Check the status of the Bluetooth service. What is its status?

-   We could see from the image below that the Bluetooth is currently
    inactive or dead

SS:

![image](https://github.com/user-attachments/assets/d2e4b24b-edb7-456c-bc44-849cbedcb5d5)


1.  Check the status of the cups services. Since when was it running?

-   Based on the image the service cups Started Running on Wednesday
    2024-09-11 at exactly 8:25 CST, 41mins prior.

SS:
![image](https://github.com/user-attachments/assets/5530609a-ec86-4e6a-8592-2780d4ffcb6c)


1.  Stop cups services. **(SS in NUMBER 6)**

2.  Verify if the service was stopped.
    ![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image11.png){width="7.027083333333334in"
    height="3.3430555555555554in"}

3.  Restart the cups services **(SS in NUMBER 8)**

4.  Verify if the service was restarted.

![](vertopal_4b01ed2bd3704465bd3b9ddcaf6f1324/media/image12.png){width="7.027083333333334in"
height="3.376388888888889in"}
