![image](https://github.com/user-attachments/assets/167082a5-a5a5-4223-a0be-5d28ed6a9c02)


# SYSADM1 -- Managing Services in Windows

## Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

## Instructions:

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below
> ![image](https://github.com/user-attachments/assets/c8b78bed-fed5-41aa-b0d9-0bc411eb5a32)
> ![image](https://github.com/user-attachments/assets/f06965ba-2922-46a0-84d9-619bb9dc689e)


4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
> 
> ![image](https://github.com/user-attachments/assets/10b3cd7b-b317-4d9a-9caf-f69e44825dc7)
> ![image](https://github.com/user-attachments/assets/caa2ebe8-521c-4c12-ae35-35d457fcb43f)

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.
    
> ![image](https://github.com/user-attachments/assets/1628214b-4316-4fab-a5ef-aa4c7f59936e)

7.  Save the batch file in Z:\\lastname_timer.bat

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
![image](https://github.com/user-attachments/assets/26a5d8d6-f938-4b2d-9893-802fa157d142)


10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
![image](https://github.com/user-attachments/assets/b87d24b1-8980-47be-9c12-c5519c5ac092)


**Rubric**

  ![image](https://github.com/user-attachments/assets/d3e3bd54-5314-4a79-9100-2a87e8ccc26c)
