# Install the Intel® distribution of the OpenVINO™ toolkit with Enterprise Software Hub™

The Intel® Enterprise Software Hub™ (ESH) is a fast, convenient method for OpenVINO™ installation. For complete information on the OpenVINO™ toolkit including an overview, system requirements, OS compatability, use cases and other resources, see [System Requirements](https://software.intel.com/content/www/us/en/develop/tools/openvino-toolkit/system-requirements.html). 

KAT:  DAVID, DID YOU MENTION THIS IS FOR LINUX & WINDOWS ONLY?

## Install OpenVINO™

This guide explains how to:

1. Download the ESH installer from the Intel OpenVINO™ website. KAT:  IS IT FROM THE OV SITE?  OR THE ESH SITE?
2. Run the installer.
3. Run a sample application to verify that the OpenVINO™ toolkit is operational.

## Step 1 - Download the ESH Installer

Download the ESH installer [here:](https://software.intel.com/content/www/us/en/develop/tools/openvino-toolkit/download.html). KAT: I'M CONFUSED, THIS ISN"T ESH...
You will be asked to login or create an Intel Developer Zone account.

1. Select the appropriate **version** and **target OS** options. KAT: I'M SEEING OPERATING SYSTEM THEN DISTRIBUTION. 
2. For Environment, select **Development and Runtime**, which installS the complete toolkit.
3. Read the EULA and press **Accept** when ready.
4. The **OpenVINO.zip** file downloads to your system.

## Step 2 - Run the Installer

Installation will take 10 minutes or longer depending on your network speed.

1. Unzip the installer.  This will create a path similar to:
  OpenVINO
  | - Intel_Distribution_of_OpenVINO_Toolkit_***
  
  **NOTE:** The pathway for the **Intel_Distribution_of_OpenVINO_Toolkit** directory will vary depending on the version. KAT: HOW WILL THEY KNOW THE PATH?
  
 2. Enter the directory with the installer:
  Replace the "\*" *** below with either the full name or use tab-completion.

 ```sh
 cd OpenVINO/Intel_Distribution_of_OpenVINO_Toolkit_***
 ```
3. Change the mode of the installer binary to allow execution:

```sh
chmod +x edgesoftware
```

4. Run the installer:
```sh
./edgesoftware install
```

## Step 3 - Run a sample to verify the Install

When installation is complete verify that the essential tools are operating on your system by running a demo script. KAT: DEMO OR SAMPLE?

**NOTE:** You may see an error about GStreamer during installation which can safely be ignored. It's for logging purposes only.

There are two suitable scripts for testing OpenVINO™; **demo_security_barrier** and **demo_squeezenet**.



