ofxMVG
======

[OpenFX](http://openeffects.org) plugins for Multiple View Geometry

**This project is not ready for end users and is not maintained for now. It has been developed for testing and analyzing camera tracking algorithms. It may become active again in the future, but not for now.**

## CameraLocalizer

CameraLocalizer estimates the camera pose of an image regarding an existing 3D reconstruction generated by openMVG.
The plugin supports multiple clips in input to localize a RIG of cameras (multiple cameras rigidly fixed).

![Camera localization screenshot](./doc/cameraLocalizationNuke.png)

CameraLocalizer on [ShuttleOFX](https://github.com/shuttleofx/ShuttleOFX)

## LensCalibration

LensCalibration estimates the best distortion parameters according to the couple camera/optics of a dataset.
The plugin supports video file & folder containing images or image sequence.

LensCalibration on [ShuttleOFX](https://github.com/shuttleofx/ShuttleOFX)

## Compilation

```
git submodule update -i
mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=../install
make install
```

## Usage
```
export OFX_PLUGIN_PATH=/path/to/ofxMVG/install
```
Then launch your preferred [OpenFX](http://openeffects.org) Host.
Currently, the plugins have only been tested in Nuke.

## License

The plugins are released under the [MPL License](LICENSE.md).
