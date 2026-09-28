# RDC Controller

As explained in tutorial 1 ([check the slides!](https://canva.link/oon1xmuchxtwbk8)), you need to open the `.ioc` file in CubeMX, click `GENERATE CODE`, before opening the project in VS Code and then clicking "Yes" when prompted to set up the STM32 Project in the pop. Generate `launch.json` following the guide in the canva presentation.

## Controller Usage

> [!WARNING]
>
> Please do not put the PCB on metal surfaces. The pins that are exposed may short and may permanently damage the board.

Please handle the controller with care. Each RDC group is provided with only one controller, and a one backup controller. If you break them, there will be consequences.

### Battery and charging

The controller uses a single cell battery as power. Plug in a USB-C charger to the USB port at the bottom left to charge the battery. You can use the controller simultaneously to charging it.

> [!Important]
>
> Do NOT use the USB port on the STM32 bluepill at the back for charging.

There are two battery holders on the back of the board. Only the Right battery (indicated by the cat saying "Use this battery!") will be connected to the board. The other battery holder is simply for backup storage of more batteries.

### Components

The TFT should be plugged in such that the screen fits within the frame of the controller. Do not plug it the opposite way.

The HC-05 module should be plugged in following the labelled pins on the silkscreen.

The two joysticks contain buttons of their own, when set `Joystick1` and `Joystick2` pins to be `PULL-UP`, the button indicators will work automatically without needing to write any code for it.

All buttons require the `PULL-UP` setting in the GPIO configuration. The hardware schematic is provided for you for reference, if you are curious.