# Install the Intel® distribution of the OpenVINO™ toolkit with Edge Software Hub™

The Intel® Edge Software Hub™ (ESH) is a fast, convenient method for OpenVINO™ installation. For complete information on the OpenVINO™ toolkit including an overview, system requirements, OS compatibility, use cases and other resources, see [System Requirements](https://software.intel.com/content/www/us/en/develop/tools/openvino-toolkit/system-requirements.html). These instructions apply to supported versions of Linux and macOS only.

## Install OpenVINO™

This guide explains how to:

1. Download the ESH installer from the Intel® Edge Software Hub™ website. 
2. Run the installer.
3. Run a demo application to verify that the OpenVINO™ toolkit is operational.

## Step 1 - Download the ESH Installer

Download the ESH installer [here](https://software.intel.com/iot/edgesoftwarehub/download/home/OpenVINO). 
You will be asked to login or create an Intel Developer Zone account.

1. Select the appropriate **Download Version** and **Target System OS**. 
2. For **Environment** select **Development and Runtime** which installs the complete toolkit.
3. Review and **Accept** the EULA.
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



