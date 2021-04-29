# OpenVINO™ Installation with the Enterprise Software Hub™

The Enterprise Software Hub™, or ESH, is a fast and convenient option for OpenVINO™ installation.  The following document describes how to use it.

## Installation Overview

1. Download the ESH installer from the Intel OpenVINO™ website.
2. Run the installer
3. Verify that the OpenVINO™ toolkit is operational.

## Step 1 - Download the ESH Installer

If you have not already downloaded the installer, use [this link](https://software.intel.com/content/www/us/en/develop/tools/openvino-toolkit/download.html).
You will be asked to login or create an Intel Developer Zone account.

1. Select the appropriate "version" and "target OS" options.  
2. For Environment, select "Development and Runtime", which will install the complete toolkit.
3. Read the EULA and press "Accept" when ready.
4. You will download a file named OpenVINO.zip.

## Step 2 - Run the Installer

Installation will take 10 minutes with a fast network connection, longer otherwise.

1. Unzip the installer.  This will create a path similar to:
  OpenVINO
  | - Intel_Distribution_of_OpenVINO_Toolkit_***
  
  (The exact name of the "Intel_Distribution_of_OpenVINO_Toolkit" directory will vary depending on the version.)
  
 2. Enter the directory with the installer
  Replace the "\*" *** below with either the full name or use tab-completion.

 ```sh
 cd OpenVINO/Intel_Distribution_of_OpenVINO_Toolkit_***
 ```
3. Change the mode of the installer binary to allow execution.

```sh
chmod +x edgesoftware
```

4. Run the installer.
```sh
./edgesoftware install
```

## Step 3 - Verify the Install

After installation has completed, verify that the essential tools are operating on your system using a demo script.

NOTE: You may get an error about GStreamer during installation.  This may be ignored.

There are two suitable scripts for testing OpenVINO™, demo_security_barrier and demo_squeezenet.



