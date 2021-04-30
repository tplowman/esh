# Install the Intel® distribution of the OpenVINO™ toolkit with Edge Software Hub™

The Intel® Edge Software Hub™ (ESH) is a fast, convenient method for OpenVINO™ installation. For complete information on the OpenVINO™ toolkit including an overview, system requirements, OS compatibility, use cases and other resources, see [System Requirements](https://software.intel.com/content/www/us/en/develop/tools/openvino-toolkit/system-requirements.html). These instructions apply to supported versions of Linux and macOS only.

## Install OpenVINO™

This guide explains how to:

1. Download the ESH installer from the Intel® Edge Software Hub™ website. 
2. Run the installer.
3. Run a demo script to verify that the OpenVINO™ toolkit is operational.

## Step 1 - Download the ESH Installer

Download the ESH installer from the [Edge Software Hub](https://software.intel.com/iot/edgesoftwarehub/download/home/OpenVINO). 
You will be asked to login or create an Intel Developer Zone account.

1. Select the appropriate **Download Version** and **Target System OS**. 
2. For **Environment** select **Development and Runtime** which installs the complete toolkit.
You'll have the option to download the default package or create a customized installation from pre-validated components. We recommend starting with the default configuration which includes all components.
4. Review and **Accept** the EULA.
5. The **OpenVINO.zip** file downloads to your system.

## Step 2 - Run the Installer

Installation will take 10 minutes or longer depending on your network speed.

1. Unzip the installer.  This will create a path similar to:
  ```sh
  OpenVINO/Intel_Distribution_of_OpenVINO_Toolkit_***
  ```
  
  where *** represents the version of OpenVINO™. 
  
 2. Enter the directory with the installer:
  Replace the *** below with either the full name or use tab-completion.

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
**NOTE:** You may see an error about GStreamer during installation which can safely be ignored. It's for logging purposes only.

When installation is complete, you'll see a table of component **SUCCESS** messages displayed.

## Step 3 - Run a Demo to Verify the Install

Verify that the essential OpenVINO™ tools are operating on your system by running a demo script.

There are two suitable scripts for testing OpenVINO™; **demo_security_barrier** and **demo_squeezenet**.  We'll use the security barrier script because it has graphical output.

**NOTE:** You will need to modify the version suffix ***openvino_2021.3.394*** shown in the commands below to match the version of OpenVINO™ you have installed.

1. Source the required environment variables:
```sh
source /opt/intel/openvino_2021.3.394/bin/setupvars.sh
```

1. Move to the directory where the script is located:
```sh
cd /opt/intel/openvino_2021.3.394/deployment_tools/demo
```

2. Run the demo script.  This will take several minutes:
```sh
sudo -EH ./demo_security_barrier_camera.sh
```
3. When successful, an image of a car with two bounding boxes and labels for **make** and **model** will be displayed on screen.

* The sudo command is used because the script downloads files to the /opt directory, which requires root write permissions.

* The script downloads a model, converts it to the OpenVINO™ IR format using the **Model Optimizer** and executes the ***security_barrier_camera_demo*** demo script.  Examining the script is also a good introduction to the OpenVINO™ developer workflow.

* You can look at the original image with an image viewer.  The image ***car_1.bmp*** is located in the same directory. 

On Linux, you can open the image with the following command while in the same directory:
```sh
eog car_1.bmp
```

**Congratulations!** By running the demo, you have confirmed that you have a working OpenVINO™ installation.

For more information on developing your edge AI solution, see the [OpenVINO™ toolkit library](https://docs.openvinotoolkit.org/2020.3/index.html).

