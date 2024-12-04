+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| d46f92d81dc1450e95aa294c8189e71e |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+==================================+========================+==========+
| NAME: BUSONGAN, DEMIRAYE-ANNE    | DATE PERFORMED:25 SEP  | /50      |
|                                  | 2024                   |          |
+----------------------------------+------------------------+----------+
| Section: IDC1                    | DATE SUBMITTED: 25 SEP |          |
|                                  | 2024                   |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Monitoring Print Services in Windows Server 2019 {#sysadm1-monitoring-print-services-in-windows-server-2019 .list-paragraph}

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

> ![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image2.png){width="5.447916666666667in"
> height="1.15625in"}

2.  Connect one client to the recently created domain\
    ![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image3.png){width="3.420138888888889in"
    height="2.279166666666667in"}![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image4.png){width="3.4277777777777776in"
    height="1.3090277777777777in"}

3.  Install Print Services Role:\
    ![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image5.png){width="5.365277777777778in"
    height="2.615972222222222in"}

4.  Search the internet for any printer installer and convert it to iso

5.  Install and deploy it as network printer

![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image6.png){width="7.018055555555556in"
height="4.750694444444444in"}

![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image7.png){width="4.61875in"
height="2.2069444444444444in"}

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

> ![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image8.png){width="5.875694444444444in"
> height="3.685416666666667in"}

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   Monitor performance metrics related to print services.

> ![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image8.png){width="5.990277777777778in"
> height="3.7576388888888888in"}

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

> ![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image9.png){width="5.13675634295713in"
> height="3.4717147856517934in"}

Part 3: Exploring Third-Party Monitoring Tools

Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

## Factors to Consider for Cobra Print Viewer in Windows Server 2019 Environment

**Features:**

-   **Compatibility with Windows Server 2019:** While the information
    provided states compatibility with Windows, it\'s essential to
    verify if Cobra Print Viewer explicitly supports Windows Server
    2019.

-   **Advanced Print Management:** The features offered by Cobra Print
    Viewer, such as viewing print job images, copying, reprinting, and
    redirecting jobs, are valuable for managing print queues in a server
    environment.

-   **Integration with Server Environment:** Consider how Cobra Print
    Viewer integrates with other server management tools or Active
    Directory. This can simplify tasks like group policy management or
    centralized print queue control.

**Pricing:**

-   **Cost-Effectiveness:** The free trial version allows for evaluation
    of the software\'s capabilities. However, the \$45.00 price tag
    should be compared to other print management solutions available for
    Windows Server 2019.

-   **ROI:** Evaluate if the features and benefits offered by Cobra
    Print Viewer justify the cost in terms of improved print management
    efficiency and potential cost savings.

**Compatibility with Windows Server 2019:**

-   **OS Requirements:** Ensure that Cobra Print Viewer meets the
    minimum system requirements for Windows Server 2019, including .NET
    Framework version.

-   **Driver Compatibility:** Verify if the software supports the print
    drivers used in your server environment. Any compatibility issues
    with specific printers or drivers could limit its functionality.

**Additional Considerations:**

-   **Support and Updates:** Assess the developer\'s support services
    and update policy. Regular updates are crucial for addressing
    security vulnerabilities and improving compatibility.

-   **Scalability:** If you manage multiple print servers or have a
    large number of print jobs, consider Cobra Print Viewer\'s
    scalability to handle the workload without performance degradation.

-   **Alternative Solutions:** Research other print management solutions
    available for Windows Server 2019 to compare features, pricing, and
    compatibility.

B.  **Print Inspector for Windows Server 2019: Features, Pricing, and
    Compatibility**

C.  ![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image10.png){width="3.84375in"
    height="3.0729166666666665in"}

**Features:**

-   **Monitoring and Auditing:** Print Inspector offers detailed
    tracking of print jobs, including document name, user, computer,
    date, and number of pages. This provides valuable insights into
    printing habits and resource utilization.  

-   **Print Queue Management:** You can pause, cancel, restart, or
    resume queued jobs. This allows for better control over print flow
    and helps prevent unnecessary printing.

-   **Notifications and Actions:** Set up alerts for specific events
    like printer jams or large print jobs. You can even configure
    automatic actions, like sending emails or suspending large jobs, for
    more efficient management.

-   **Reporting and Cost Analysis:** Generate reports ranging from
    simple job lists to comprehensive user and printer usage statistics.
    Export data to CSV or HTML for further analysis. This can help
    identify areas for cost reduction and optimize printer use.

-   **Lightweight and Scalable:** The software\'s small footprint makes
    it suitable for various environments, including servers.

**Pricing:**

-   **Free:** Print Inspector is a free software solution, making it a
    budget-friendly option for print management on Windows Server 2019.

**Compatibility with Windows Server 2019:**

-   **Limited Information:** The provided information doesn\'t
    explicitly state compatibility with Windows Server 2019. It\'s
    crucial to verify compatibility directly with SoftPerfect, the
    developer.

-   **Potential Challenges:** Since Print Inspector is a desktop
    application, running it directly on a server might not be ideal. It
    might require additional configuration or alternative server-based
    solutions.

**Additional Considerations:**

-   **Server Management Tools:** Investigate native Windows Server 2019
    print management tools for basic print queue control and monitoring.
    These tools might provide sufficient functionality depending on your
    needs.

-   **Security:** Evaluate the security implications of installing a
    desktop application on a server. Consider user access controls and
    potential vulnerabilities before deploying Print Inspector.

-   **Alternative Solutions:** Research dedicated print management
    software solutions designed specifically for Windows Server
    environments. These could offer additional features and better
    server integration.

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

    -   Follow the installation instructions provided by the tool\'s
        documentation.

    -   Configure it to monitor your print services.

![](vertopal_d46f92d81dc1450e95aa294c8189e71e/media/image11.png){width="4.361805555555556in"
height="3.6326388888888888in"}

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

    -   Analyze the collected data (e.g., print volume, errors, user
        activity).

Rubric

  --------------------------------------------------------------------------------------------------------------
  **Criteria**   **1                  **2 (Needs       **3                **4        **5             **Score**
                 (Unsatisfactory)**   Improvement)**   (Satisfactory)**   (Good)**   (Excellent)**   
  -------------- -------------------- ---------------- ------------------ ---------- --------------- -----------

  --------------------------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 1: Setting Up Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Domain         No domain  Domain      Domain       Domain       Domain       
  Installation**   created    created     created      configured   configured   
                              with errors correctly    well         and          
                                                                    documented   
                                                                    thoroughly   
  ---------------- ---------- ----------- ------------ ------------ ------------ --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Client       Client not  Connection   Client       Client      Client        
  Connection**   connected   attempt      connected    connected   connected and 
                             failed       but with     correctly   documented    
                                          issues                   well          
  -------------- ----------- ------------ ------------ ----------- ------------- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Print Services Role not    Role        Role        Role         Role          
  Role             installed   installed   installed   installed    installed,    
  Installation**               with issues correctly   and          configured,   
                                                       configured   and           
                                                                    documented    
                                                                    thoroughly    
  ---------------- ----------- ----------- ----------- ------------ ------------- --

  ----------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Printer      No          Installer    Installer   Installer   Installer     
  Installer      installer   conversion   converted   converted   converted,    
  Conversion**   found       attempted    but not     and used    used, and     
                             but failed   used                    documented    
                                                                  well          
  -------------- ----------- ------------ ----------- ----------- ------------- --

  --------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Network      Printer    Deployment   Printer      Printer     Printer       
  Printer        not        failed       deployed but deployed    deployed,     
  Deployment**   deployed                not          correctly   tested, and   
                                         functional               documented    
                                                                  well          
  -------------- ---------- ------------ ------------ ----------- ------------- --

  --------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 2: Monitoring Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Event      Event     Opened but  Logs reviewed Logs         Logs reviewed   
  Viewer       Viewer    no logs     but           reviewed     with thorough   
  Usage**      not       reviewed    superficial   with some    analysis and    
               opened                              analysis     documentation   
  ------------ --------- ----------- ------------- ------------ --------------- --

  --------------------------------------------------------------------------------

  -----------------------------------------------------------------------------------
  **Performance   Performance   Opened but  Metrics      Metrics     Metrics       
  Monitor Usage** Monitor not   no metrics  monitored    monitored   monitored,    
                  opened        monitored   but not      with some   analyzed, and 
                                            analyzed     analysis    documented    
                                                                     thoroughly    
  --------------- ------------- ----------- ------------ ----------- ------------- --

  -----------------------------------------------------------------------------------

  ------------------------------------------------------------------------------------
  **Print       Console   Opened but      Active jobs     Active jobs Active jobs   
  Management    not       functionality   viewed          viewed with viewed and    
  Console       opened    not used        superficially   some detail documented    
  Usage**                                                             thoroughly    
  ------------- --------- --------------- --------------- ----------- ------------- --

  ------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 3: Exploring Third-Party Tools**                                        
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Research on  No tools     Research     Research on Research on   Research on  
  Tools**        researched   incomplete   one tool    two tools     two tools,   
                                           completed   with some     detailed     
                                                       analysis      analysis,    
                                                                     and          
                                                                     comparison   
  -------------- ------------ ------------ ----------- ------------- ------------ --

  ----------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------
  **Installation    Tool not    Installation   Tool         Tool         Tool           
  and               installed   failed         installed    installed    installed,     
  Configuration**                              but not      and          configured,    
                                               configured   configured   and documented 
                                                            with issues  thoroughly     
  ----------------- ----------- -------------- ------------ ------------ -------------- --

  ----------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Reporting   No report   Report lacks Report      Report      Comprehensive   
  Findings**    generated   detail       generated   generated   report with     
                                         but lacks   with some   thorough        
                                         analysis    analysis    analysis and    
                                                                 documentation   
  ------------- ----------- ------------ ----------- ----------- --------------- --

  ---------------------------------------------------------------------------------
