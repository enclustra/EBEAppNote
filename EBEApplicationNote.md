# EBE Application Note

# Purpose
The purpose of this document is to explain the workflow and to provide practical examples of how to use the [Enclustra Build Environment (EBE)](https://www.enclustra.com/en/products/tools/linux-build-environment/) and customize the corresponding software according to the design requirements.

# Summary
This application note describes the three main parts of the Enclustra Build Environment: U-Boot, Linux kernel and root file system. It provides details on the build flow for each part, including examples on how to customize certain components according to the system requirements. In addition, references to other useful documents are included.

# License
Copyright 2021 by Enclustra GmbH, Switzerland. All rights are reserved. Unauthorized duplication of this document, in whole or in part, by any means is prohibited without the prior written permission of Enclustra GmbH, Switzerland. Although Enclustra GmbH believes that the information included in this publication is correct as of the date of publication, Enclustra GmbH reserves the right to make changes at any time without notice. All information in this document is strictly confidential and may only be published by Enclustra GmbH, Switzerland. All referenced trademarks are the property of their respective owners.

# Introduction
The following chapters explain how to create a custom design and how to run an EBE generated Linux on a newly created design.

The recommended way to create a custom design is to use the [Enclustra Reference Designs](https://www.github.com/enclustra) as a starting point. The Enclustra build environment uses the pre-generated files from the reference design as
default binaries.

The downloaded reference design can be modified according to the users specification. But as a first step it might be helpful to build the bitstream and all required boot files using the unmodified reference design. This ensures that the build process works as expected. Once Linux is booting using the output of the own manually generated reference design, it is up to the user to modify the design.

# Table of contents
* [1 - Workflow](./Chapter-1-Workflow.md)
    - [1.1 Modules equipped with Xilinx SoC](Chapter-1-Workflow.md#11---modules-equipped-with-xilinx-soc)
   - [1.2 Modules equipped with Intel SoC](Chapter-1-Workflow.md#12---modules-equipped-with-intel-soc)
   - [1.3 Additional information](Chapter-1-Workflow.md#13-additional-information)
* [2 - U-Boot](./Chapter-2-U-Boot.md)
    - [2.1 Bootloader](Chapter-2-U-Boot.md#21-bootloader)
    - [2.2 Folder structure](Chapter-2-U-Boot.md#22-folder-structure)
    - [2.3 Configuration](Chapter-2-U-Boot.md#23-configuration)
    - [2.4 Device tree](Chapter-2-U-Boot.md#24-device-tree)
    - [2.5 Command line interface](Chapter-2-U-Boot.md#25-command-line-interface)
    - [2.6 Environment](Chapter-2-U-Boot.md#26-environment)
    - [2.7 Boot scripts](Chapter-2-U-Boot.md#27-boot-scripts)
    - [2.8 Additional information](Chapter-2-U-Boot.md#28-additional-information)
* [3 - Linux kernel](./Chapter-3-Linux-Kernel.md)
    - [3.1 Folder structure](Chapter-3-Linux-Kernel.md#31-folder-structure)
    - [3.2 Configuration](Chapter-3-Linux-Kernel.md#32-configuration)
    - [3.3 Add an existing driver example](Chapter-3-Linux-Kernel.md#33-add-an-existing-driver-example)
    - [3.4 Create and add a custom driver](Chapter-3-Linux-Kernel.md#34-create-and-add-a-custom-driver)
    - [3.5 Device tree](Chapter-3-Linux-Kernel.md#35-deviec-tree)
    - [3.6 Additional information](Chapter-3-Linux-Kernel.md#36-additional-information)
* [4 - Buildroot](./Chapter-4-Buildroot.md)
    - [4.1 Root file system](Chapter-4-Buildroot.md#41-root-file-system)
    - [4.2 Folder structure](Chapter-4-Buildroot.md#42-folder-structure)
    - [4.3 Configuration](Chapter-4-Buildroot.md#43-configuration)
    - [4.4 Toolchain](Chapter-4-Buildroot.md#44-toolchain)
    - [4.5 File system modification](Chapter-4-Buildroot.md#45-file-system-modification)
    - [4.6 Init system](Chapter-4-Buildroot.md#46-init-system)
    - [4.7 Create a custom application](Chapter-4-Buildroot.md#47-create-a-custom-application)
    - [4.8 Debug a custom application](Chapter-4-Buildroot.md#48-debug-a-custom-application)
    - [4.9 Copy files to root file system](Chapter-4-Buildroot.md#49-copy-files-to-root-file-system)
    - [4.10 Useful commands](Chapter-4-Buildroot.md#410-useful-commands)
    - [4.11 Additional information](Chapter-4-Buildroot.md#411-additional-information)
# References
* [Enclustra Reference Designs](https://www.github.com/enclustra)

**Please continue reading [Chapter 1 - Workflow](./Chapter-1-Workflow.md).**