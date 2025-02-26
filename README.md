## Introduction

<details>
  <summary>Images of the laptop</summary>

  ![Image of the laptop on Catalina](https://github.com/user-attachments/assets/c1e877b6-6dae-4bce-84de-356a0cb4b046)
  ![Image of the laptop connected to a secondary monitor](https://github.com/user-attachments/assets/2c5365bd-4398-4260-9e51-719fd727b678)

  
</details>



Technically this isn't my first hackintosh, but it's the first one I've configured & setup. It runs macOS Catalina 10.15.7, and a MacBookPro8,1 SMBios
I've forgotten most of the things I've to get this work, but I used Catalina Patcher (Post Install) to get Graphic Acceleration working, as OCLP's Post-Install patches were grayed out.

## What's working and what's not
| Item | Status  |
| ---- | ------- |
| Built in keyboard | Yes(1) |
| Trackpad | Yes |
| Graphic Acceleration | Yes(2) |
| USB Ports & eSATA's USB functions | Yes |
| WiFi | Yes |
| Bluetooth | Yes |
| Media keys | Yes |
| Battery percentage | Yes |
| Sleep | Yes |
| Built in speakers | Yes |
| Power management | Yes (2) |
| HDMI | Yes |
| Lid detection (sleep on lid close) | Yes |
| Brightness keys | No |
| VGA | No |
| Ethernet | Not tested |
| SD-Card slot | Not tested |
| ExpressCard | Not tested |
| Headphone jack | Not tested |
| Bottom dock slot | Not tested |
| eSATA-Port's SATA functions | Not tested |

1: The keyboard has a strange issue where it stops registering clicks for a few seconds.
2. The Graphic Acceleration is slow, until the device goes to sleep and wakes up.

## My specs
CPU: i7-2640m
GPU: Intel HD 3000
RAM: 8GB DDR3 @ 1333mhz
WiFi: Intel Centrino Advanced-N 6205
Speakers: codec `IDT92HD90BXX` layout id `12`
Touchpad: ALPS Trackpad
BIOS revision: A19

## Quirks
The Dell Latitude E6220 supports UEFI, but after trying to set it up for a few days, I have come to the conclusion that the implementation is broken. Trying to add OpenCore's EFI file simply causes the BIOS to freeze.

## Setup
Change the device information using https://github.com/corpnewt/GenSMBIOS
