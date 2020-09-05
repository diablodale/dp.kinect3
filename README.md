# dp.kinect3

<img align="right" src="https://user-images.githubusercontent.com/679350/92308029-f2755800-ef9a-11ea-9e80-d133662376d1.jpg" alt="Kinect 3"/>

dp.kinect3 is a plugin for the [Cycling '74 Max](https://cycling74.com/) development environment to use your [Microsoft Azure Kinect](https://azure.microsoft.com/en-us/services/kinect-dk/) sensor (the 3rd generation Kinect) on your Windows PC.

### Setup Overview

The Azure Kinect sensor does not have a shared driver/runtime
that all applications use. Instead, all files are separate and
installed with applications like dp.kinect3.

This will increase the size of the dp.kinect3 download.  
I split the download into two groups:

* dp.kinect3 files that I create and test. All features
  of dp.kinect3 _except body tracking_ will work with
  only these files. Usually, new features and bugfixes need
  only these files. This download is ~4 MB
* Microsoft body tracking neural net files that Microsoft
  creates and tests. These will change less often.
  This download is ~430 MB. I defer to Microsoft to
  (re)distribute its own files.

### dp.kinect3

1. Verify [Microsoft's system requirements](https://docs.microsoft.com/en-us/azure/kinect-dk/system-requirements)
2. Install [Cycling'74 Max](https://cycling74.com/downloads/) version 6 or newer (64-bit)
3. Download dp.kinect3 from <https://hidale.com/shop/dp-kinect3/>
4. [Decompress](https://support.microsoft.com/en-us/help/14200/windows-compress-uncompress-zip-files)
   all the files in this download into an empty directory for dp.kinect3
5. Next, you must register dp.kinect3

### Register

1. Your *dp.kinect2* license enables you access to this private release.
   Please visit <https://hidale.com/shop/dp-kinect2/>
   if you do not yet have a license.
2. Open `example.maxpat` patch included in the dp.kinect3 download
3. Double-click on the top-left `(p register)` subpatch
4. Type your registration name in the field beside the register button.
   Your registration name is usually not your email address.
5. Click the register button and use the dialog box that appears to select
   your *dp.kinect2* registration key (.dpreg file)
6. You will see a successful registration in the Max console window

### Body Tracking

Follow these three steps if you want body tracking.

1. Download and install Microsoft's
   [Body Tracking SDK 1.0.1](https://www.microsoft.com/en-us/download/details.aspx?id=100942). Note the install directory; often `"C:\Program Files\Azure Kinect Body Tracking SDK"`
2. Navigate into the SDK install directory, then the `tools` subdirectory,
   e.g. `"C:\Program Files\Azure Kinect Body Tracking SDK\tools"`
3. Copy these seven files from `tools` to
   the dp.kinect3 directory
   ```
   k4abt.dll
   onnxruntime.dll
   dnn_model_2_0.onnx
   cudart64_100.dll
   cublas64_100.dll
   cudnn64_7.dll
   vcomp140.dll
   ```

### Documentation

The dp.kinect2 documentation and tutorials should be used during this
private release. Many patches and examples will work by changing the object
in the patch from (dp.kinect2) to (dp.kinect3).

<https://github.com/diablodale/dp.kinect2/wiki> has this reference
documentation and tutorials. You can also experiment with the helpfile
that is included with the dp.kinect2 download. Many examples
on the tabs work by changing the object to (dp.kinect3)
