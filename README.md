# MAX72xx LED Matrix Display Library

<i>IMPORTANT NOTE: Please make sure that you find and read the html documentation that comes with the library (open "docs/index.html") or use the link below. <b>You will need to edit the MAX72xx.h file to configure the type of matrix you are using</b>. This is the most asked support question so avoid frustration and READ THE MANUAL in the docs subfolder.</i>

The library implements functions that allow the MAX72xx to be used for LED matrices (64 individual LEDs), allowing the programmer to use the LED matrix as a pixel device, displaying graphics elements much like any other pixel addressable display.

In this scenario, it is convenient to abstract out the concept of the hardware device and create a uniform and consistent pixel address space, with the libraries determining device and device-element address. Similarly, control of the devices should be uniform and abstracted to a system level.

The library still retains flexibility for device level control, should the developer require, through the use of overloaded class methods.

[Library Documentation](https://majicdesigns.github.io/MD_MAX72XX/)

## Information regarding ESP32 support

Minimal ESP32 support added for use with esp-idf. The user needs to create an spi device handle and pass it to the constructor. Please add the following to the main makefile to specify the architecture:
```
CPPFLAGS += -DARCH_ESP32
```

Create a subfolder named components in your project folder and copy the files as in the tree below:

<pre>
├── components
│   └── md_max7219
│       ├── component.mk
│       ├── include
│       │   └── MD_MAX72xx.h
│       ├── MD_MAX72xx_buf.cpp
│       ├── MD_MAX72xx.cpp
│       ├── MD_MAX72xx_font.cpp
│       ├── MD_MAX72xx_lib.h
│       └── MD_MAX72xx_pix.cpp
</pre>
