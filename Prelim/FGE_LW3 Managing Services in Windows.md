+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| b1d9278aa86d42ce89df6f0af721019d |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+==================================+========================+==========+
| BUSONGAN, DEMIRAYE-ANNE          | DATE PERFORMED: 28 AUG |          |
|                                  | '24                    |          |
+----------------------------------+------------------------+----------+
| IDC1                             | DATE SUBMITTED: 28 AUG |          |
|                                  | '24                    |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

  ---------------------------------------------------------------------------------------------------------------------------------------
  **Status**   **Name of Service**         **Screenshot**
  ------------ --------------------------- ----------------------------------------------------------------------------------------------
  Start        App Readiness               ![](vertopal_b1d9278aa86d42ce89df6f0af721019d/media/image2.png){width="2.5541666666666667in"
                                           height="1.1770833333333333in"}

  Stop         App Readiness               ![](vertopal_b1d9278aa86d42ce89df6f0af721019d/media/image3.png){width="2.526388888888889in"
                                           height="1.1652777777777779in"}

  Restart      App Readiness               ![](vertopal_b1d9278aa86d42ce89df6f0af721019d/media/image4.png){width="2.6666666666666665in"
                                           height="1.25in"}

  Pause        Themes                      ![](vertopal_b1d9278aa86d42ce89df6f0af721019d/media/image5.png){width="2.9493055555555556in"
                                           height="1.1027777777777779in"}
  ---------------------------------------------------------------------------------------------------------------------------------------

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:

+---------------------------------+------------------------------------+
| **DHCP Client\                  | **Remote Desktop Configuration**   |
| **![](vertopal_b1d92            |                                    |
| 78aa86d42ce89df6f0af721019d/med | ![](vertopal_b1d9278aa86           |
| ia/image6.png){width="2.8625in" | d42ce89df6f0af721019d/media/image7 |
| height="3.3319444444444444in"}  | .png){width="3.3430555555555554in" |
|                                 | height="3.832638888888889in"}      |
+=================================+====================================+
| **User Manager Properties**     | **Network Connection\              |
|                                 | **![](vertopal_b1d9278aa86         |
| ![](vertopal_b1d9278aa86d42ce8  | d42ce89df6f0af721019d/media/image9 |
| 9df6f0af721019d/media/image8.pn | .png){width="3.1166666666666667in" |
| g){width="2.8229166666666665in" | height="3.5618055555555554in"}     |
| height="3.2395833333333335in"}  |                                    |
+---------------------------------+------------------------------------+
| **Print Spooler\                |                                    |
| *                               |                                    |
| *![](vertopal_b1d9278aa86d42ce8 |                                    |
| 9df6f0af721019d/media/image10.p |                                    |
| ng){width="2.964583333333333in" |                                    |
| height="3.4451388888888888in"}  |                                    |
+---------------------------------+------------------------------------+

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_b1d9278aa86d42ce89df6f0af721019d/media/image11.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

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
> ![](vertopal_b1d9278aa86d42ce89df6f0af721019d/media/image12.png){width="7.023611111111111in"
> height="0.6590277777777778in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**![](vertopal_b1d9278aa86d42ce89df6f0af721019d/media/image13.png){width="5.458333333333333in"
> height="2.125in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **50 /50**                                         
  ---------------------------------------------------------------------------------------
