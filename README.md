# Embedded Programming Projects

These projects are designed to explore and learn embedded programming using various languages and platforms.

## Platforms Used

Currently, only the **Seeeduino Xiao** (based on the **Atmel SAMD21 Cortex-M0**) is supported.

- **Seeeduino Xiao**: A compact development board featuring the **Atmel SAMD21 microcontroller**. It is suitable for low-power embedded projects and prototyping.  
  - [Seeeduino Xiao Datasheet](https://files.seeedstudio.com/wiki/XIAO-Expansion-Board/res/ATSAMD21G18A-MU-Datasheet.pdf)
  - [Atmel SAMD21 Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-42181-SAM-D21_Datasheet.pdf)

## Pinout for Seeeduino Xiao

Here is the pinout diagram for the **Seeeduino Xiao** to guide your hardware setup:

![Seeeduino Xiao Pinout](https://wiki.seeedstudio.com/Seeeduino-XIAO/img/Seeeduino-XIAO-pinout.png)

## Roadmap

The current roadmap includes pure implementations, implementations using hardware abstraction layers (HAL), and implementations with language-specific frameworks.

### Pure Implementations (Without HAL)

This approach involves working directly with registers and the ARM Cortex-M0 without relying on any HAL, providing a deeper understanding of the underlying hardware.

- [ ] **C**  
  You can start with direct register access using ARM GCC. Example: [ARM GCC Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm)
  
- [ ] **C++**  
  The same approach as C, but using object-oriented practices. No HAL involved.

- [ ] **Rust**  
  Use Rust with `no_std` and without the HAL by writing to registers directly. [Learn more](https://docs.rust-embedded.org/book/start/registers.html).
  
- [ ] **Zig**  
  Zig provides low-level access to memory and peripherals, perfect for working without a HAL. Check out [MicroZig](https://github.com/microzig/microzig).
  
- [ ] **Haskell**  
  Haskell with LLVM can be cross-compiled to run on SAMD21, but it requires manual setup. [Haskell LLVM guide](https://neilmitchell.blogspot.com/2013/07/haskell-on-arm.html).

### Implementations with HAL

This approach abstracts hardware details and uses vendor-provided or third-party HALs to simplify peripheral interactions.

- [ ] **C (with HAL)**  
  Use **ASF4** (Advanced Software Framework) with SAMD21 to abstract hardware layers. [ASF4 HAL Documentation](https://onlinedocs.microchip.com/pr/GUID-2A8AADED-413E-4021-AF0C-D99E61B8160D-en-US-4/GUID-AF9CCA00-AD16-41F5-8EDB-A194AA6D51B9.html)

- [ ] **C++ (with HAL)**  
  Similar to C, using ASF4. [Microchip ASF4 API](https://onlinedocs.microchip.com).

- [ ] **Rust (with HAL)**  
  The `atsamd-hal` crate provides a high-level abstraction for SAMD21 peripherals.  
  [atsamd-hal crate](https://github.com/atsamd-rs/atsamd)  
  [RTIC for Rust](https://rtic.rs/0.5/book/en/).

- [ ] **Zig (with HAL)**  
  Use **MicroZig** for HAL-based Zig development. [MicroZig GitHub](https://github.com/microzig/microzig).

- [ ] **Haskell (with HAL)**  
  Haskell isn’t widely used with HALs, but you can explore using LLVM to cross-compile and work towards integrating HAL-like frameworks if needed.

### Implementations with Frameworks

Language-specific frameworks make embedded development easier by managing concurrency, peripherals, and other system-level operations.

- [ ] **C (with Framework)**  
  Use **FreeRTOS** with C for task management. Example: [FreeRTOS on ARM Cortex-M0](https://www.freertos.org/RTOS-Cortex-M0-M3.html)

- [ ] **C++ (with Framework)**  
  FreeRTOS with C++ classes can provide an RTOS on SAMD21.

- [ ] **Rust (with RTIC)**  
  Use **RTIC** (Real-Time Interrupt-driven Concurrency) for Rust-based embedded systems. [RTIC documentation](https://rtic.rs).

- [ ] **Zig (with Framework)**  
  Use **MicroZig** for task scheduling and concurrency management. [MicroZig GitHub](https://github.com/microzig/microzig).

- [ ] **Haskell (with LLVM)**  
  Haskell doesn’t have a direct embedded framework, but explore LLVM-based frameworks for parallel task execution.

## References and Useful Links

- **Atmel SAMD21 Datasheet**: [SAMD21 Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-42181-SAM-D21_Datasheet.pdf)
- **Seeeduino Xiao Datasheet**: [Seeeduino Xiao](https://files.seeedstudio.com/wiki/XIAO-Expansion-Board/res/ATSAMD21G18A-MU-Datasheet.pdf)
- **ARM GCC Toolchain**: [ARM GCC](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm)
- **ASF4 Documentation**: [ASF4 HAL](https://onlinedocs.microchip.com/pr/GUID-4E095027-601A-4343-844F-2034603B4C9C-en-US-4)
- **Rust Embedded Book**: [Rust Embedded](https://docs.rust-embedded.org/book/)
- **RTIC for Rust**: [RTIC Framework](https://rtic.rs)
- **MicroZig for Zig**: [MicroZig](https://github.com/microzig/microzig)
