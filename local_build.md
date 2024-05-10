This is short guide on how to develop the demo on your local machine outside of the yocto environment.


You will need the CMake extension and CMake Tools extension on VScode to use this

Provided is a folder called `debug-files`, this is designed to replicate all of the file dependencies of the app, including certs and scripts

`.vscode/launch.json` allows you to configure the the commandline argument (in this case passing the config.json)
`.vscode/settings.json` overrides `IOTC_C_SDK_DIR` in CMakeLists.txt in order to use the Generic C SDK from the submodule


```bash
# clone this repo
git submodule update --init --recursive
code main.c
# Control + F5 to compile and execute the application
```

You can set breakpoints and debug the sample as needed.

