# Arduino Atmega168 device into makeblock IDE

Edit `/Applications/Makeblock/mBlock.app/Contents/Resources/app/mlink-v1/platforms/arduino/boards.js`
Add the following section
```
    nano168: {
        args: "-mmcu=atmega168 -DF_CPU=16000000L -DARDUINO=10809 -DARDUINO_AVR_NANO -DARDUINO_ARCH_AVR",
        linkArgs: "-mmcu=atmega168",
        variants: "eightanaloginputs",
        staticLib: "libnano.a",
        rootDir: "nano"
    }
```

The full file will look like

```
module.exports={uno:{args:"-mmcu=atmega328p -DF_CPU=16000000L -DARDUINO=10605 -DARDUINO_AVR_UNO -DARDUINO_ARCH_AVR",linkArgs:"-mmcu=atmega328p",variants:"standard",staticLib:"libmbot.a",rootDir:"mbot"},mega:{args:"-mmcu=atmega2560 -DF_CPU=16000000L -DARDUINO=10605 -DARDUINO_AVR_MEGA2560 -DARDUINO_ARCH_AVR",linkArgs:"-mmcu=atmega2560",variants:"mega",staticLib:"libranger.a",rootDir:"ranger"},leonardo:{args:"-mmcu=atmega32u4 -DF_CPU=16000000L -DARDUINO=10605 -DARDUINO_AVR_LEONARDO -DARDUINO_ARCH_AVR",linkArgs:"-mmcu=atmega32u4",variants:"leonardo",staticLib:"libleonardo.a",rootDir:"leonardo"},micro:{args:"-mmcu=atmega32u4 -DF_CPU=16000000L -DARDUINO=10605 -DARDUINO_AVR_MICRO -DARDUINO_ARCH_AVR -DUSB_VID=0x2341 -DUSB_PID=0x8037",linkArgs:"-mmcu=atmega32u4",variants:"micro",staticLib:"libmicro.a",rootDir:"micro"},yun:{args:"-mmcu=atmega32u4 -DF_CPU=16000000L -DARDUINO=10605 -DARDUINO_AVR_YUN -DARDUINO_ARCH_AVR -DUSB_VID=0x2341 -DUSB_PID=0x8041",linkArgs:"-mmcu=atmega32u4",variants:"yun",staticLib:"libyun.a",rootDir:"yun"},nano:{args:"-mmcu=atmega328p -DF_CPU=16000000L -DARDUINO=10809 -DARDUINO_AVR_NANO -DARDUINO_ARCH_AVR",linkArgs:"-mmcu=atmega328p",variants:"eightanaloginputs",staticLib:"libnano.a",rootDir:"nano"},nano168:{args:"-mmcu=atmega168 -DF_CPU=16000000L -DARDUINO=10809 -DARDUINO_AVR_NANO -DARDUINO_ARCH_AVR",linkArgs:"-mmcu=atmega168",variants:"eightanaloginputs",staticLib:"libnano.a",rootDir:"nano"}};
```

