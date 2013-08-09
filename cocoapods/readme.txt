This directory contains a prebuilt platform file for cocoapods integration.

The file "platform.h" is built during the make process, but is checked in so that it is available to cocoapods without needing to run the configure steps. This should be fine since cocoapods is specific to Mac/iOS platforms.

To update the "platform.hpp" file:

1. Make sure you have a local installation of zmq. If you don't have one, get the source from https://github.com/zeromq/zeromq3-x and install it locally.
2. Run `./autogen.sh`
3. Run `./configure --with-libzmq=$ZMQ_PATH`
4. Run `cp src/platform.h cocoapods/platform.h`
