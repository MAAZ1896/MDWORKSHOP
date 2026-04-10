# Control-M Workload Archiving 9.0.20 Setup Guide

- Control-M Workload Archiving Setup 
- Prerequisite 
- Installing Control-M Workload Archiving on Windows .
- To install Control-M Workload Archiving on Windows
  

# Control-M Workload Archiving Setup
Control-M Workload Archiving is a Control-M add-on that helps you to meet organizational audit and compliance requirements, and troubleshoot your environment using historical data.

Control-M Workload Archiving automatically collects and archives job log and output data in a secure, central repository that is separate from the production environment. The archive data is accessible to users via the Control-M client and Control-M Self Service based on Control-M/EM authorizations.

You can define Workload Archiving collection policies to determine the period of job log and output data in the Workload Archiving server.

Control-M Workload Archiving uses a dedicated PostgreSQL database that is preinstalled. You can use the default database or connect to an existing Oracle or PostgreSQL database, even if Control-M/EM and Control-M/Server use a different database type. XYZ recommends that you install Control-M Workload Archiving on a separate server.

# Control-M Workload Archiving installation
The following procedure describes how to install Control-M Workload Archiving on Windows enabling you to archive job logs and outputs in a secure and central repository:
+ Installing Control-M Workload Archiving on Windows.

Control-M Workload Archiving uses a dedicated PostgreSQL database that is preinstalled.
Do not install it on a computer that already hosts another database server. Install a secondary instance of the Control-M/EM server in a distributed configuration, as described in Control-M/Enterprise Manager installation guide. The installation process installs a dedicated GUI Server.  

>**Note:**  
> + To avoid slow performance on Control-M/EM, set the Control-M/Server IOALOGLM system parameter to 7 or less. 
>+ To upgrade to version 9.0.20, upgrade the Control-M/EM server first, and then upgrade the
Control-M/EM Distributed component, as described in Upgrading Control-M/EM on UNIX and Upgrading Control-M/EM on Windows. The system automatically upgrades the Workload Archiving server during the Control-M/EM Distributed upgrade.

# Prerequisite
1. Verify that the Control-M/EM database server is running.
2. Verify that you have installed a primary Control-M/Enterprise Manager version 9.0.20 or later, as described in Control-M/Enterprise Manager installation.
3. Verify that you have installed a distributed Control-M/EM, as described in
Control-M/Enterprise Manager installation.
4. Download the Control-M Workload Archiving activation CD (see Product Distribution in the Control-M Workload Archiving Release Notes).
   
# Installing Control-M Workload Archiving on Windows

This procedure describes how to install Control-M Workload Archiving on Windows on a distributed Control-M/EM.

>**Note**: If you are using an Oracle database, you do not need to install the fix pack

 ## To install Control-M Workload Archiving on Windows:
1. Log in to the Control-M/EM distributed computer.
2. From the Control-M Workload Archiving activation CD, double-click the setup.exe file.
The Control-M Workload Archiving Installation wizard appears.
3. Create a parameter file and then run the automatic install in a non-interactive mode, as follows:
    - Follow the on-screen instructions until the Summary window.
     - Click Generate and select the location to create the XML parameter file.
     - Click Yes to quit the installation.
        A confirmation message appears.
     - Click Yes.
   - Copy automatic installation parameters file to a network location that is accessible to all computers where you want to perform an automatic installation.
   - Log in using a user ID that has Administrator permissions on the current computer.
   - Ensure that the installation DVD is still in the DVD drive, and run the following command:
  
  ```
  <source_path>\Setup.exe -silent <xml_path>\<filename.xml>
The installation log can be found at the following location:
<installFolder>\<Control-M/EM/home dir>BMCINSTALL\log\BMC_ControlM_Workload_Archiving_Install_<date-time>.log

```
 4. Click **Done**.
 5. A sucessfull message will appear in the left bottom pane, click **Complete** to finish and click **Report** to generated detailed report.

   




