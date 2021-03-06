# pyk4a
This library is a simple and pythonic wrapper in Python 3 for the Azure-Kinect-Sensor-SDK.

Images are returned as numpy arrays and behave like python objects.

This approach incurs almost no overhead in terms of CPU, memory or other resources.
It also simplifies usage. Kinect C api image buffers are directly reused and image releases are performed automatically by the python garbage collector.


## Prerequisites
The [Azure-Kinect-Sensor-SDK](https://github.com/microsoft/Azure-Kinect-Sensor-SDK) is required to build this library.
To use the SDK, refer to the installation instructions [here](https://github.com/microsoft/Azure-Kinect-Sensor-SDK).


## Install

### Linux

Make sure your `LD_LIBRARY_PATH` contains the directory of k4a.lib

```
pip install pyk4a
```

### Windows

Make sure you replace the paths in the following instructions with your own k4a sdk path.

```
pip install git+https://github.com/kevinkit/pyk4a.git --global-option=build_ext --global-option="-IC:\Program Files\Azure Kinect SDK v1.2.0\sdk\include" --global-option="-LC:\Program Files\Azure Kinect SDK v1.2.0\sdk\windows-desktop\amd64\release\lib"```
```

Don't forget to add the folder containing the release `k4a.dll` to your Path env variable `C:\Program Files\Azure Kinect SDK v1.3.0\sdk\windows-desktop\amd64\release\bin`

## Example

A advanced example is available in the [example](https://github.com/etiennedub/pyk4a/tree/master/example) folder.
To execute it [opencv-python](https://github.com/skvark/opencv-python) is required.

## Documentation

No documentation is available but most methods are used in the example. You can follow it as reference.
You can also check directly the code of the main class [PyK4A](https://github.com/etiennedub/pyk4a/blob/master/pyk4a/pyk4a.py).

## Contribution

Feel free to send pull requests.

Bug reports are also appreciated. Please include as much details as possible.

### TODO:

- Allow mapping of ir sensor to color
- get_capture in MJPG
