# NuttX-PiPico-WAVtoI2S-64fs
## What is this?
Pre-built NuttX modified to support 64fs YDA142 and other 64fs I2Sdacs. WAV files saved on SD card can be played from the Terminal.
## Wiring
Terminal can be accessed through UART0.
| UART0 | GPIO  |
| ----- | ----- |
| TX    | GP0   |
| RX    | GP1   |

| I2S       | GPIO  |
| --------- | ----- |
| I2S_DATA  | GP9   |
| I2S_BCK   | GP10  |
| I2S_LRCK  | GP11  |

| SD SPI    | GPIO  |
| --------- | ----- |
| TX        | GP19  |
| SCK       | GP18  |
| CSn       | GP17  |
| RX        | GP16  |

## How to use
The schematic design for YDA142 can be viewed here.

https://github.com/takuhoTech/YDA142-Kicad-Symbol-and-Footprint/blob/main/AudioAmplifier.pdf

```
NuttShell (NSH) NuttX-10.0.1
nsh> nxplayer
NxPlayer version 1.05
h for commands, q to exit

nxplayer> play 01.wav
nxplayer> stop
nxplayer> play 02.wav
nxplayer> pause
nxplayer> resume
nxplayer> stop
nxplayer>
```
