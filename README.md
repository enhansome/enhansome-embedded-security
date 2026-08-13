# Awesome Embedded Security with stars

[![Validate Markdown](https://github.com/hexsecs/awesome-embedded-security/workflows/Validate%20Markdown/badge.svg)](https://github.com/hexsecs/awesome-embedded-security/actions/workflows/markdown-lint.yml) ⭐ 53 | 🐛 6 | 🌐 JavaScript | 📅 2026-07-29

A curated list of embedded security tools, resources, and training for firmware analysis, reverse engineering, hardware hacking, and IoT security.

Topics covered include firmware extraction and fuzzing, secure boot and root of trust, side-channel analysis, fault injection, JTAG/SWD debugging, RTOS and TEE security, Bluetooth/BLE, Zigbee, and other wireless protocol security, and software-defined radio (SDR).

## Table of Contents

* Software Tools
  * Binary Parsing and Analysis Tools
  * Disassemblers/Decompilers
  * Fuzzing Tools
  * MCU Firmware Fuzzing
  * Emulation Tools
  * Debugging Tools
  * Secure Boot and Firmware Trust
  * Firmware Supply Chain and SBOM
  * Language Specific Decompilers
  * Security Auditing Frameworks
  * Firmware Taint Analysis
  * RTOS Security
  * TEE/Trusted Execution Environments
  * Root of Trust and TPM
  * OTA Update Security
  * IoT Protocol Security
  * Bluetooth and BLE Security
  * Zigbee / Z-Wave Security
  * Baseband Security
  * Firmware Malware Analysis
* Hardware Tools
  * Hardware Reverse Engineering Multitools
  * Hardware Debug Interfaces
  * Chip-Off and Memory Forensics
  * Side-Channel Analysis
  * Fault Injection
  * Logic Analyzer
  * RF Tools (Non-SDR)
  * Software Defined Radios
  * Software Defined Radio Software
  * Wifi Tools
* Further Learning and Training
* Open Source Intelligence (OSINT)
* Other Awesome Lists
* Contribute

## Software Tools

### Binary Parsing and Analysis Tools

* [Binwalk](https://github.com/ReFirmLabs/binwalk) ⭐ 14,224 | 🐛 91 | 🌐 Rust | 📅 2026-08-11 - Fast, easy to use tool for analyzing, reverse engineering, and extracting firmware images.
* [LIEF](https://github.com/lief-project/LIEF) ⭐ 5,524 | 🐛 32 | 🌐 C++ | 📅 2026-08-07 - Library to Instrument Executable Formats: parse, modify, and abstract ELF, PE, Mach-O, DEX, and OAT binaries found in firmware images.
* [FLARE-FLOSS](https://github.com/mandiant/flare-floss) ⭐ 4,119 | 🐛 121 | 🌐 Python | 📅 2026-08-11 - FLARE Obfuscated String Solver that automatically extracts obfuscated, encoded, and stack strings from binaries for rapid firmware triage.
* [unblob](https://github.com/onekey-sec/unblob) ⭐ 2,539 | 🐛 42 | 🌐 Python | 📅 2026-08-10 - Fast, accurate firmware extraction engine from ONEKEY supporting 100+ archive, compression, and filesystem formats with fewer false positives than Binwalk. Presented at DEF CON 30.
* [checksec](https://github.com/slimm609/checksec.sh) ⭐ 2,363 | 🐛 3 | 🌐 Go | 📅 2026-08-04 - Shell script to check binary security hardening flags (NX, PIE, RELRO, stack canary, ASLR) on ELF executables extracted from firmware.
* [OFRAK](https://github.com/redballoonsecurity/ofrak) ⭐ 2,062 | 🐛 154 | 🌐 Python | 📅 2026-08-05 - Binary analysis and modification platform that combines the ability to unpack, analyze, modify, and repack binaries.
* [cwe\_checker](https://github.com/fkie-cad/cwe_checker) ⭐ 1,348 | 🐛 30 | 🌐 Rust | 📅 2026-07-24 - Binary analysis tool that checks ELF binaries for violations of Common Weakness Enumerations (CWEs) using abstract interpretation, with cross-architecture support.
* [firmwalker](https://github.com/craigz28/firmwalker) ⭐ 1,221 | 🐛 5 | 🌐 Shell | 📅 2023-08-29 - Searches extracted firmware filesystems for interesting files, credentials, configuration, and known-vulnerable components.
* [VulHunt](https://github.com/vulhunt-re/vulhunt) ⭐ 877 | 🐛 2 | 🌐 C++ | 📅 2026-08-12 - Lua-rule-based vulnerability detection framework from Binarly's research team that operates across disassembly, IR, and decompiled code simultaneously, with dedicated UEFI module scanning support.
* [argXtract](https://github.com/projectbtle/argXtract) ⭐ 31 | 🐛 1 | 🌐 Python | 📅 2026-06-02 - Statically extracts arguments to SVC calls and HAL functions from stripped ARM Cortex-M BLE firmware without symbol tables, enabling security audits of Nordic and similar binaries. ACSAC 2021.
* [SCOUT](https://github.com/R00T-Kim/SCOUT) ⭐ 10 | 🐛 1 | 🌐 Python | 📅 2026-06-08 - Deterministic firmware analysis pipeline emitting SARIF 2.1, CycloneDX 1.6 + VEX SBOM, and hash-anchored evidence chains; auto-detects Ghidra and runs P-code SSA dataflow taint with 4-tier confidence caps. Pure stdlib (no pip dependencies).
* [Kaitai Struct](https://kaitai.io/) - Declarative language used to describe various binary data structures, laid out in files or in memory: i.e. binary file formats, network stream packet formats, etc.

### Disassemblers/Decompilers

* [Angr](https://github.com/angr/angr) ⭐ 9,009 | 🐛 696 | 🌐 Python | 📅 2026-08-13 - Platform-agnostic binary analysis framework. Brought to you by the Computer Security Lab at UC Santa Barbara, SEFCOM at Arizona State University, their associated CTF team, Shellphish, the open source community, and @rhelmot.
* [Capstone](https://github.com/capstone-engine/capstone) ⭐ 8,945 | 🐛 360 | 🌐 C | 📅 2026-08-13 - Lightweight multi-platform, multi-architecture disassembly framework. Their target is to make Capstone the ultimate disassembly engine for binary analysis and reversing in the security community.
* [RetDec](https://github.com/avast/retdec) ⭐ 8,604 | 🐛 458 | 🌐 C++ | 📅 2026-05-26 - Retargetable machine-code decompiler from Avast supporting ARM, MIPS, x86, and other architectures common in embedded firmware.
* [Keystone](https://github.com/keystone-engine/keystone) ⭐ 2,623 | 🐛 243 | 🌐 C++ | 📅 2026-07-18 - A lightweight multi-architecture assembler framework that complements Capstone.
* [BARF](https://github.com/programa-stic/barf-project) ⭐ 1,451 | 🐛 17 | 🌐 Python | 📅 2019-11-24 - A binary analysis and reverse engineering framework with support for ROP gadget search and CFG recovery.
* [Angr Management](https://github.com/angr/angr-management) ⭐ 1,167 | 🐛 245 | 🌐 Python | 📅 2026-08-13 - Multi-architecture binary analysis toolkit, with the capability to perform dynamic symbolic execution (like Mayhem, KLEE, etc.) and various static analyses on binaries. If you'd like to learn how to use it, you're in the right place!
* [Vivisect](https://github.com/vivisect/vivisect) ⭐ 996 | 🐛 113 | 🌐 Python | 📅 2026-08-04 - A combined disassembler/static analysis/symbolic execution/debugger framework.
* [IDA Pro](https://hex-rays.com/ida-pro/) 💰 - Disassembler capable of creating maps of their execution to show the binary instructions that are actually executed by the processor in a symbolic representation (assembly language). Advanced techniques have been implemented into IDA Pro so that it can generate assembly language source code from machine-executable code and make this complex code more human-readable.
* [Binary Ninja](https://binary.ninja/) 💰 - Interactive disassembler, decompiler, and binary analysis platform for reverse engineers, malware analysts, vulnerability researchers, and software developers that runs on Windows, macOS, and Linux.
* [Cutter](https://cutter.re/) - Free and Open Source RE Platform powered by Rizini.
* [Rizin](https://rizin.re/) - A free and open-source Reverse Engineering framework, providing a complete binary analysis experience with features like Disassembler, Hexadecimal editor, Emulation, Binary inspection, Debugger, and more.
* [radare2](https://www.radare.org/n/) - A free/libre toolchain for easing several low level tasks like forensics, software reverse engineering, exploiting, debugging. It is composed by a bunch of libraries (which are extended with plugins) and programs that can be automated with almost any programming language.
* [Ghidra](https://ghidra-sre.org/) - A software reverse engineering (SRE) suite of tools developed by NSA's Research Directorate in support of the Cybersecurity mission.

### Debugging Tools

* [Open OCD](https://github.com/openocd-org/openocd/) ⭐ 2,290 | 🐛 3 | 🌐 C | 📅 2026-07-28 - Provides on-chip programming and debugging support with a layered architecture of JTAG interface and TAP support.
* [assembly-repl](https://github.com/pirate/assembly-repl) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2026-05-13 - Native assembly, LLVM IR, C, C++, and Objective-C REPLs for macOS and Linux.
* [GDB](https://www.sourceware.org/gdb/) - The GNU Project debugger, allows you to see what is going on \`inside' another program while it executes -- or what another program was doing at the moment it crashed.
* [GEF](https://hugsy.github.io/gef/) - Kick-ass set of commands for X86, ARM, MIPS, PowerPC and SPARC to make GDB cool again for exploit dev. It is aimed to be used mostly by exploit developers and reverse-engineers, to provide additional features to GDB using the Python API to assist during the process of dynamic analysis and exploit development.
* [Black Magic Probe](https://codeberg.org/blackmagic-debug/blackmagic) - An open-source JTAG/SWD debugger with embedded GDB server and automatic target detection.
* [pyOCD](https://pyocd.io) - An open-source Python library for programming and debugging Arm Cortex-M microcontrollers with cross-platform debug probe support.
* [probe-rs](https://probe.rs/) - Modern Rust-based embedded debug toolkit supporting SWD/JTAG with built-in flashing, RTT logging, and GDB server for ARM and RISC-V targets.
* [Frida](https://frida.re/) - Dynamic instrumentation toolkit for injecting JavaScript or native code into running processes on embedded Linux, Android, iOS, and bare-metal targets.

### Secure Boot and Firmware Trust

* [MCUboot](https://github.com/mcu-tools/mcuboot) ⭐ 2,028 | 🐛 98 | 🌐 C | 📅 2026-08-11 - Secure bootloader for 32-bit microcontrollers supporting signed images, rollback protection, and measured boot flows.
* [wolfBoot](https://github.com/wolfSSL/wolfBoot) ⭐ 519 | 🐛 11 | 🌐 C | 📅 2026-08-13 - Portable secure bootloader for 32-bit MCUs using wolfCrypt for image signature verification (Ed25519, ECC, RSA, post-quantum LMS/XMSS), with delta updates, encrypted images, and explicit voltage-glitch countermeasures.
* [AVB (Android Verified Boot)](https://android.googlesource.com/platform/external/avb/+/master/README.md) - Reference implementation and design guidance for chained trust and verified partitions in embedded Android systems.
* [U-Boot Verified Boot](https://docs.u-boot.org/en/latest/usage/fit/verified-boot.html) - FIT-signature based verified boot support for embedded Linux boot chains.

### Firmware Supply Chain and SBOM

* [Grype](https://github.com/anchore/grype) ⭐ 12,722 | 🐛 399 | 🌐 Go | 📅 2026-08-10 - Vulnerability scanner that consumes SBOMs to identify known CVEs in firmware dependencies.
* [Syft](https://github.com/anchore/syft) ⭐ 9,396 | 🐛 627 | 🌐 Go | 📅 2026-08-12 - SBOM generator for filesystems and artifacts, useful for firmware package/component inventories.
* [Sigstore Cosign](https://github.com/sigstore/cosign) ⭐ 6,205 | 🐛 160 | 🌐 Go | 📅 2026-08-11 - Tooling for keyless signing and verification of firmware/container artifacts in CI/CD pipelines.
* [CVE Binary Tool](https://github.com/ossf/cve-bin-tool) ⭐ 1,747 | 🐛 227 | 🌐 Python | 📅 2026-08-12 - OpenSSF tool that scans binaries directly for 350+ known-vulnerable open source components (OpenSSL, libpng, BusyBox, and more), without requiring a pre-built SBOM; can also generate one from the scan.
* [in-toto](https://in-toto.io/) - Framework for supply chain integrity that records signed provenance steps and enforces layout verification.

### Fuzzing Tools

* [AFL++](https://github.com/AFLplusplus/AFLplusplus) ⭐ 6,705 | 🐛 24 | 🌐 C | 📅 2026-08-13 - A coverage-guided fuzzer with enhanced mutations, QEMU and Unicorn emulation modes, and custom power schedules.
* [honggfuzz](https://github.com/google/honggfuzz) ⭐ 3,372 | 🐛 30 | 🌐 C | 📅 2026-06-19 - A feedback-driven evolutionary fuzzer supporting hardware-based coverage (Intel BTS/PT) and persistent mode for extreme speed.
* [boofuzz](https://github.com/jtpereyda/boofuzz) ⭐ 2,354 | 🐛 101 | 🌐 Python | 📅 2026-08-06 - Actively maintained network protocol fuzzer and the spiritual successor to Sulley, with session management, target monitoring, and protocol graph support.
* [Fuzzowski](https://github.com/nccgroup/fuzzowski) ⭐ 794 | 🐛 13 | 🌐 Python | 📅 2024-01-29 - A network protocol fuzzer based on the Sulley/BooFuzz framework with support for TCP/UDP/SSL protocols.
* [GDBFuzz](https://github.com/boschresearch/gdbfuzz) ⚠️ Archived - Uses GDB hardware breakpoints as a coverage source for uninstrumented embedded targets — works on any GDB-debuggable MCU with no firmware modification required. Bosch Research / ISSTA 2023.
* [Peach](https://gitlab.com/peachtech/peach-fuzzer-community) 💰 - A smart fuzzer supporting both generation-based and mutation-based fuzzing via Peach Pit definitions. Community edition is source-available; full product is commercial.
* [libFuzzer](https://llvm.org/docs/LibFuzzer.html) - In-process, coverage-guided, evolutionary fuzzing engine integrated with LLVM.

### Language Specific Decompilers

* .NET
  * [ILSpy](https://github.com/icsharpcode/ILSpy) ⭐ 25,852 | 🐛 189 | 🌐 C# | 📅 2026-08-13 - .NET Decompiler with support for PDB generation, ReadyToRun, Metadata (\&more) - cross-platform!
  * [dnSpy](https://github.com/dnSpyEx/dnSpy) ⭐ 10,889 | 🐛 149 | 🌐 C# | 📅 2026-07-20 - .NET debugger and assembly editor.
  * [de4dot](https://github.com/de4dot/de4dot) ⚠️ Archived - .NET deobfuscator.
* Java
  * [JADX](https://github.com/skylot/jadx) ⭐ 50,050 | 🐛 442 | 🌐 Java | 📅 2026-08-05 - Dex to Java decompiler.
  * [JD-GUI](https://github.com/java-decompiler/jd-gui) ⭐ 15,172 | 🐛 248 | 🌐 Java | 📅 2024-07-08 - Java decompiler.

### Security Auditing Frameworks

* [Metasploit](https://github.com/rapid7/metasploit-framework) ⭐ 38,796 | 🐛 612 | 🌐 Ruby | 📅 2026-08-12 - Open source penetration testing framework (BSD licensed) maintained by Rapid7, with modules for exploiting vulnerabilities, scanning, and post-exploitation across embedded Linux and IoT targets.
* [kernel-hardening-checker](https://github.com/a13xp0p0v/kernel-hardening-checker) ⭐ 2,117 | 🐛 13 | 🌐 Python | 📅 2026-08-06 - Audits Linux kernel Kconfig options and boot parameters against KSPP, CLIP OS, and STIG hardening recommendations; supports ARM, ARM64, x86, and RISC-V. Works in Yocto/OpenEmbedded pipelines.
* [IoTGoat](https://github.com/OWASP/IoTGoat) ⭐ 917 | 🐛 2 | 🌐 C | 📅 2025-10-05 - OWASP intentionally insecure firmware for Raspberry Pi and x86 platforms, providing hands-on practice for the OWASP IoT Top 10 vulnerabilities.
* [FwAnalyzer (Firmware Analyzer)](https://github.com/cruise-automation/fwanalyzer) ⭐ 516 | 🐛 3 | 🌐 Go | 📅 2023-10-08 - Tool to analyze (ext2/3/4), FAT/VFat, SquashFS, UBIFS filesystem images, cpio archives, and directory content using a set of configurable rules.
* [EXPLIoT](https://pypi.org/project/expliot/) - Framework for security testing and exploiting IoT products and IoT infrastructure. It provides a set of plugins (test cases) which are used to perform the assessment and can be extended easily with new ones.
* [Firmware Analysis and Comparison Tool (FACT)](https://fkie-cad.github.io/FACT_core/) - Automated Firmware Security analysis (Router, IoT, UEFI, Webcams, Drones, …). It is easy to use (web UI), extend (plug-in system) and integrate (REST API).

### Firmware Taint Analysis

* [KARONTE](https://github.com/ucsb-seclab/karonte) ⭐ 429 | 🐛 10 | 🌐 Python | 📅 2021-09-18 - Static analysis tool that tracks untrusted input flows across binary boundaries (shared files, sockets, env vars) in embedded Linux firmware using angr-based inter-binary taint propagation. IEEE S\&P 2020.
* [SaTC](https://github.com/NSSL-SJTU/SaTC) ⭐ 351 | 🐛 27 | 🌐 Python | 📅 2024-12-12 - Anchors taint analysis to string literals shared between web front-end and back-end binaries to pinpoint user-controlled input entry points; found 33 unknown bugs in commercial firmware. USENIX Security 2021.
* [EmTaint](https://github.com/kuc001/EmTaint) ⭐ 47 | 🐛 3 | 🌐 Python | 📅 2023-05-27 - Structured symbolic expression-based taint analysis with on-demand alias resolution for embedded Linux firmware; found 151 0-day vulnerabilities across 35 real-world images. ISSTA 2023.

### RTOS Security

* [FreeRTOS Security](https://www.freertos.org/Security/01-Security-overview) - Security features and documentation for FreeRTOS including MQTT over TLS, PKCS#11, and PSA Certified implementation.
* [Zephyr Project Security](https://docs.zephyrproject.org/latest/security/index.html) - Security documentation for the Zephyr RTOS including TF-M integration, verified boot, and security testing.
* [RT-Thread Security](https://github.com/RT-Thread/rt-thread/security) ⭐ 12,148 | 🐛 485 | 🌐 C | 📅 2026-08-13 - Security resources and vulnerability reporting for RT-Thread IoT OS.
* [seL4](https://sel4.systems/) - Formally verified microkernel with machine-checked proofs of functional correctness, integrity, and confidentiality, providing the strongest security guarantees of any production OS kernel.
* [Tock OS](https://www.tockos.org/) - Rust-based embedded OS for microcontrollers designed for security through hardware-enforced memory isolation and a capability-based driver model, targeting Cortex-M and RISC-V platforms.

### TEE/Trusted Execution Environments

* [Intel SGX SDK](https://github.com/intel/linux-sgx) ⭐ 1,448 | 🐛 140 | 🌐 C++ | 📅 2026-08-13 - Open-source Linux SDK and Platform Software for Intel Software Guard Extensions, providing the build/install toolchain for developing and deploying hardware-based memory enclave applications.
* [Samsung TrustZone Research Toolkit](https://github.com/quarkslab/samsung-trustzone-research) ⭐ 160 | 🐛 0 | 🌐 Python | 📅 2019-12-16 - Quarkslab's RE toolkit for Samsung Kinibi TrustZone: Ghidra loader for MCLF trustlet binaries, Unicorn-based trustlet emulator for exploit development, and Python bindings for communicating with Trusted Applications.
* [OP-TEE](https://optee.readthedocs.io/) - Open Source Trusted Execution Environment providing isolation for secure world execution on ARM TrustZone processors.
* [Trusty TEE](https://source.android.com/docs/security/features/trusty) - Trusted Execution Environment used in Android for secure services and keystore.
* [AMD SEV](https://developer.amd.com/sev/) - Secure Encrypted Virtualization for encrypting VM memory with AMD-V hardware assistance.

### Root of Trust and TPM

* [TPM 2.0 TS](https://github.com/tpm2-software/tpm2-tss) ⭐ 892 | 🐛 145 | 🌐 C | 📅 2026-08-13 - TCG Software Stack for TPM 2.0 providing API for key management and attestation.
* [tpm2-algtest](https://github.com/crocs-muni/tpm2-algtest) ⭐ 7 | 🐛 2 | 🌐 C | 📅 2024-12-19 - Tests real TPM 2.0 chips for RNG output quality, key generation timing, algorithm support, and implementation fingerprints across 80+ firmware revisions from 6 vendors. From CRoCS (discoverers of ROCA). CHES 2024.
* [TPM 2.0 Reference Implementation](https://trustedcomputinggroup.org/resource-library/) - TPM 2.0 specification and reference software from the TCG.
* [IBM Software TPM](https://sourceforge.net/projects/ibmswtpm2/) - Software TPM 2.0 emulator for testing and development.
* [Keylime](https://keylime.dev/) - Open source TPM-based remote attestation for cloud and edge.
* [AMD fTPM Security Guidance](https://www.amd.com/en/resources/product-security/bulletin/amd-sb-4011.html) - AMD guidance and security bulletin coverage related to firmware TPM behavior on supported platforms.

### OTA Update Security

* [SUIT](https://datatracker.ietf.org/wg/suit/about/) - Software Update for the Internet of Things (SUIT) working group developing manifest-based firmware update architecture.
* [RAUC](https://rauc.io/) - Safe and secure firmware update framework for embedded Linux with bundle signing and A/B partitioning.
* [Mender](https://mender.io/) - Over-the-air software updater for Linux IoT devices with atomic updates and rollback.
* [SWUpdate](https://sbabic.github.io/swupdate/) - Linux firmware update agent with image verification and incremental updates.

### IoT Protocol Security

* [KillerBee](https://github.com/riverloopsec/killerbee) ⭐ 845 | 🐛 31 | 🌐 C | 📅 2023-09-12 - IEEE 802.15.4/ZigBee security research framework for capturing, injecting, and analyzing ZigBee network traffic using compatible radio hardware.
* [Cotopaxi](https://github.com/Samsung/cotopaxi) ⭐ 362 | 🐛 1 | 🌐 Python | 📅 2024-05-31 - Multi-protocol IoT security testing toolkit from Samsung R\&D covering MQTT, CoAP, AMQP, DTLS, KNX, QUIC, RTSP, SSDP, HTTP/2, gRPC, and more; supports fingerprinting, fuzzing, and known-vulnerability identification across 14 protocols.
* [U-Fuzz](https://github.com/asset-group/U-Fuzz) ⭐ 108 | 🐛 0 | 🌐 C | 📅 2025-07-04 - Universal stateful fuzzer that infers a protocol's state machine from a handful of benign packet captures, then generates crashing test cases; demonstrated against CoAP, Zigbee, and 5G NR.
* [TLS for MQTT](https://mqtt.org/faq/) - Overview of TLS implementation for MQTT brokers and clients.
* [wolfMQTT](https://www.wolfssl.com/products/wolfmqtt/) - MQTT client library with TLS support optimized for embedded systems.
* [CoAP Security](https://datatracker.ietf.org/doc/html/rfc7252) - Constrained Application Protocol (CoAP) security with DTLS.
* [libcoap](https://libcoap.net/) - C implementation of CoAP with DTLS support for secure IoT communication.
* [Wireshark MQTT](https://www.wireshark.org/docs/dfref/m/mqtt.html) - Protocol analyzer support for MQTT traffic inspection and security analysis.

### Bluetooth and BLE Security

* [BtleJuice](https://github.com/DigitalSecurity/btlejuice) ⚠️ Archived - Bluetooth Low Energy MITM proxy framework for real-time interception and manipulation of BLE communications.
* [GATTacker](https://github.com/securing/gattacker) ⭐ 843 | 🐛 18 | 🌐 JavaScript | 📅 2022-01-31 - BLE MITM tool for intercepting and relaying GATT profiles to test BLE device authentication and data integrity.
* [InternalBlue](https://github.com/seemoo-lab/internalblue) ⭐ 784 | 🐛 21 | 🌐 Python | 📅 2024-08-21 - Bluetooth experimentation framework enabling binary patching, LMP injection, and live monitoring of Broadcom/Cypress firmware on commodity devices (iPhone, Samsung Galaxy, Raspberry Pi) without custom hardware.
* [BlueToolkit](https://github.com/sgxgsx/BlueToolkit) ⭐ 721 | 🐛 4 | 🌐 Jupyter Notebook | 📅 2026-03-05 - Modular black-box vulnerability testing framework for Bluetooth Classic and BLE with Recon/Exploit/Report modules covering 40+ public exploits (MITM, RCE, DoS); used to uncover 128 vulnerabilities across 22 vehicles from major automakers. USENIX WOOT 2025.
* [BrakTooth](https://github.com/Matheus-Garbelini/braktooth_esp32_bluetooth_classic_attacks) ⭐ 577 | 🐛 32 | 📅 2024-08-31 - Directed exploit suite for Bluetooth Classic LMP layer vulnerabilities, targeting protocol layers inaccessible from standard host stacks; affected 1,400+ products from Intel, Qualcomm, and Broadcom. USENIX Security 2022.
* [SweynTooth](https://github.com/Matheus-Garbelini/sweyntooth_bluetooth_low_energy_attacks) ⭐ 333 | 🐛 15 | 🌐 Python | 📅 2021-11-23 - Runnable PoC exploits for 18 BLE link-layer and L2CAP vulnerabilities across TI, NXP, Cypress, Dialog, Microchip, and STMicro SDKs, including full pairing bypass and link-layer overflows. USENIX ATC 2020.
* [WHAD Framework](https://github.com/whad-team/whad-client) ⭐ 325 | 🐛 73 | 🌐 Python | 📅 2026-06-18 - Hardware-agnostic multi-protocol wireless security framework (BLE, Zigbee, Enhanced ShockBurst, ANT) using a cheap nRF52840 dongle as a universal attack radio; foundation for Quarkslab's BLE GATT fuzzer. DEF CON 32 (2024).
* [nRF Sniffer for Bluetooth LE](https://www.nordicsemi.com/Products/Development-tools/nRF-Sniffer-for-Bluetooth-LE) 💰 - Nordic Semiconductor's BLE packet sniffer for capturing and analyzing Bluetooth Low Energy traffic with Wireshark integration. Wireshark plugin is open source; dongle firmware is a closed binary requiring Nordic hardware.
* [Bettercap BLE](https://www.bettercap.org/modules/ble/) - BLE scanning, enumeration, and characteristic read/write module integrated into the bettercap Swiss-army knife framework.

### Zigbee / Z-Wave Security

* [VFuzz](https://github.com/CNK2100/VFuzz-public) ⭐ 15 | 🐛 0 | 🌐 Python | 📅 2025-04-13 - The only dedicated open-source Z-Wave security fuzzer; uses a Field Prioritization Algorithm to mutate protocol-valid frames and assess target encryption capabilities. IEEE Access 2022.
* [Z-Fuzzer](https://github.com/zigbeeprotocol/Z-Fuzzer) ⭐ 9 | 🐛 1 | 🌐 Python | 📅 2023-10-16 - Coverage-guided Zigbee protocol fuzzer using a software simulator with pre-defined peripheral and interrupt configurations; found 6 CVEs in TI Z-Stack. ACM Digital Threats 2022.

### Baseband Security

* [Rayhunter](https://github.com/EFForg/rayhunter) ⭐ 5,483 | 🐛 93 | 🌐 Rust | 📅 2026-08-10 - EFF's open source Rust tool that runs on a cheap mobile hotspot to detect cell-site simulators (IMSI catchers/Stingrays) by monitoring signaling traffic for suspicious behavior like forced 2G downgrades.
* [FirmWire](https://github.com/FirmWire/FirmWire) ⭐ 874 | 🐛 17 | 🌐 Python | 📅 2026-07-11 - Full-system emulation platform for Samsung (Shannon) and MediaTek cellular baseband firmware with AFL++ fuzzing integration, a task-injection ModKit, and dynamic debugging support. Found 7 pre-authentication memory corruptions. NDSS 2022.
* [OsmocomBB](https://github.com/osmocom/osmocom-bb) ⭐ 328 | 🐛 1 | 🌐 C | 📅 2026-06-17 - Free Software GSM baseband (Layer 1-3) implementation for TI Calypso-based phones, replacing proprietary baseband firmware entirely and enabling open research into the GSM air interface.

### Firmware Malware Analysis

* [emba](https://github.com/e-m-b-a/emba) ⭐ 3,593 | 🐛 26 | 🌐 Shell | 📅 2026-08-11 - Efficient malware analysis framework for embedded firmware with scanning and reporting.
* [Firmware Analysis Toolkit](https://github.com/attify/firmware-analysis-toolkit) ⭐ 1,582 | 🐛 51 | 🌐 Python | 📅 2024-09-16 - Automated tool for firmware emulation and vulnerability discovery.
* [Firmware Security Testing](https://github.com/scriptingxss/owasp-fstm) ⭐ 484 | 🐛 5 | 📅 2026-06-08 - OWASP firmware security testing methodology and practical guidance for assessing embedded devices.
* [EMBArk](https://github.com/e-m-b-a/embark) ⭐ 394 | 🐛 14 | 🌐 Python | 📅 2026-07-31 - Enterprise web interface for EMBA providing multi-user scan management, aggregated vulnerability dashboards, and CI/CD integration for continuous firmware security monitoring.

### Emulation Tools

* [Unicorn Engine](https://github.com/unicorn-engine/unicorn) ⭐ 9,229 | 🐛 209 | 🌐 C | 📅 2026-07-30 - A lightweight multi-architecture CPU emulator framework providing pure CPU emulation for ARM, MIPS, x86, RISC-V, and more.
* [Qiling](https://github.com/qilingframework/qiling) ⭐ 6,051 | 🐛 123 | 🌐 Python | 📅 2026-07-22 - An advanced binary emulation framework supporting cross-platform OS-level emulation for Windows, Linux, Android, BSD, UEFI, and multiple architectures.
* [PANDA](https://github.com/panda-re/panda) ⭐ 2,773 | 🐛 96 | 🌐 C | 📅 2026-07-29 - Platform for Architecture-Neutral Dynamic Analysis with record/replay functionality and LLVM IR translation for whole-system analysis.
* [Firmadyne](https://github.com/firmadyne/firmadyne) ⭐ 2,097 | 🐛 107 | 🌐 Shell | 📅 2024-07-21 - Automated system for emulating and analyzing Linux-based embedded firmware; extracts and boots firmware images in QEMU to enable dynamic vulnerability discovery.
* [FirmAE](https://github.com/pr0v3rbs/FirmAE) ⭐ 907 | 🐛 49 | 🌐 Python | 📅 2026-06-24 - An automated framework for emulation and vulnerability analysis of IoT firmware with an 79% success rate using arbitration techniques.
* [Avatar2](https://github.com/avatartwo/avatar2) ⭐ 574 | 🐛 27 | 🌐 Python | 📅 2025-03-31 - Dynamic analysis orchestration framework for binary firmware that coordinates execution across emulators (QEMU, Unicorn) and real hardware targets.
* [HALucinator](https://github.com/embedded-sec/halucinator) ⭐ 166 | 🐛 3 | 🌐 Python | 📅 2021-10-06 - MCU firmware emulation framework that replaces Hardware Abstraction Layer (HAL) functions with high-level models, enabling full firmware execution without physical hardware.
* [FirmSolo](https://github.com/BUseclab/FirmSolo) ⭐ 22 | 🐛 2 | 🌐 Python | 📅 2024-07-16 - Reverse-engineers vendor Linux kernel module version magic to load proprietary `.ko` drivers into a compatible kernel for dynamic analysis and fuzzing, unlocking code previously inaccessible to emulators. USENIX Security 2023.
* [Renode](https://renode.io/) - Open-source hardware simulation framework from Antmicro for functional testing and security analysis of embedded firmware without physical hardware.

### MCU Firmware Fuzzing

* [Fuzzware](https://github.com/fuzzware-fuzzer/fuzzware) ⭐ 376 | 🐛 15 | 🌐 Python | 📅 2026-06-27 - Automatically models MMIO peripheral inputs via symbolic execution to enable coverage-guided fuzzing of ARM Cortex-M firmware with no hardware required. Achieves up to 3.25× coverage over prior approaches. USENIX Security 2022.
* [Icicle](https://github.com/icicle-emu/icicle-emu) ⭐ 307 | 🐛 13 | 🌐 Rust | 📅 2026-08-08 - Rust-based grey-box fuzzer with architecture-agnostic coverage instrumentation, notable for supporting **MSP430 and RISC-V** where AFL++ QEMU mode has no coverage. ISSTA 2023.
* [μEmu](https://github.com/MCUSec/uEmu) ⭐ 150 | 🐛 1 | 🌐 Python | 📅 2023-11-20 - Infers peripheral behavior from invalid-access patterns under symbolic execution, then drives AFL-based fuzzing of bare-metal MCU firmware without physical hardware. USENIX Security 2021.
* [SAFIREFUZZ](https://github.com/pr0me/SAFIREFUZZ) ⭐ 130 | 🐛 1 | 🌐 Rust | 📅 2024-12-19 - Rewrites ARM Cortex-M firmware via dynamic binary rewriting to run as a Linux userspace process on ARM servers, achieving \~600× the fuzzing throughput of HALucinator. USENIX Security 2023.
* [DICE](https://github.com/RiS3-Lab/DICE-DMA-Emulation) ⭐ 66 | 🐛 4 | 🌐 C | 📅 2023-10-14 - Automatically identifies and emulates DMA input channels in MCU firmware, enabling fuzzers to exercise DMA-driven code paths that were previously opaque. IEEE S\&P 2021.
* [μAFL](https://github.com/MCUSec/microAFL) ⭐ 48 | 🐛 0 | 🌐 C | 📅 2022-07-15 - Hardware-in-the-loop fuzzer using ARM ETM trace hardware to collect coverage from a real MCU without any firmware instrumentation. Found 8 CVEs in STM32/NXP SDKs. ICSE 2022.

## Hardware Tools

### Hardware Reverse Engineering Multitools

* [Tiguard](https://github.com/tigard-tools/tigard) ⭐ 853 | 🐛 2 | 📅 2026-05-29 - An FTDI FT2232H-based multi-protocol tool for hardware hacking.
* [Bus Pirate](https://github.com/ElderlyPirate/Bus_Pirate) ⭐ 691 | 🐛 77 | 🌐 C | 📅 2025-12-28 - Open source hacker multi-tool that talks to electronic stuff. It's got a bunch of features an intrepid hacker might need to prototype their next project.
* [Glasgow Interface Explorer](https://glasgow-embedded.org/) - Versatile open-source FPGA-based hardware debugging and reverse engineering tool supporting SPI, I2C, UART, JTAG, and custom protocols with a high-level Python API.
* [GreatFET](https://greatscottgadgets.com/greatfet/) - Open-source USB host-side hardware security research platform from Great Scott Gadgets with an expandable neighbor board ecosystem for interfacing with embedded targets.
* [Hydrabus](https://hydrabus.com/) - Open-source multi-protocol hardware hacking tool with support for SPI, I2C, UART, CAN, 1-Wire, and JTAG interfaces, purpose-built for embedded device analysis.

### Hardware Debug Interfaces

* [LUNA](https://github.com/greatscottgadgets/luna) ⭐ 1,132 | 🐛 33 | 🌐 Python | 📅 2026-06-04 - FPGA-based USB analysis and development platform from Great Scott Gadgets, enabling USB sniffing, protocol fuzzing, and custom USB peripheral development via Amaranth HDL.
* [JTAGenum](https://github.com/cyphunk/JTAGenum) ⭐ 799 | 🐛 13 | 🌐 C++ | 📅 2023-10-30 - Enumerates JTAG pinouts on unknown boards by brute-force testing candidate pin mappings.
* [JTAGulator](https://github.com/grandideastudio/jtagulator) ⭐ 798 | 🐛 3 | 🌐 Propeller Spin | 📅 2025-07-29 - Automates discovery of JTAG, SWD, and UART debug interfaces on unknown PCBs by brute-forcing pin combinations, with sigrok-compatible logic analyzer mode and direct OpenOCD integration for post-discovery exploitation.
* [UrJTAG](https://urjtag.sourceforge.io/) - Open-source JTAG toolkit for boundary scan, flash programming, and low-level target interaction.

### Chip-Off and Memory Forensics

* [CHIPSEC](https://github.com/chipsec/chipsec) ⭐ 3,294 | 🐛 54 | 🌐 Python | 📅 2026-08-07 - Platform security assessment framework with firmware and chipset checks relevant to offline dump triage.
* [NANDO](https://github.com/bbogush/nand_programmer) ⭐ 385 | 🐛 29 | 🌐 C | 📅 2025-04-13 - Open hardware STM32-based parallel NAND flash programmer with chip autodetection, bad block handling, and an extensible chip database; targets the parallel NAND found in older routers, set-top boxes, and automotive ECUs.
* [SNANDer](https://github.com/McMCCRU/SNANDer) ⭐ 376 | 🐛 19 | 🌐 C | 📅 2026-05-20 - CLI programmer for SPI NOR/NAND flash and I2C EEPROMs using the ubiquitous $3 CH341A USB chip, extending it with NAND support beyond what proprietary software provides — the go-to for quick firmware dumps from IoT hardware.
* [Flashrom](https://flashrom.org/) - Utility for identifying, reading, writing, and verifying SPI flash chips common in embedded boards.
* [The Sleuth Kit](https://www.sleuthkit.org/sleuthkit/) - File system forensic toolkit for carving and examining recovered NAND/eMMC/UFS image dumps.

### Side-Channel Analysis

* [ChipWhisperer](https://github.com/newaetech/chipwhisperer) ⭐ 1,546 | 🐛 50 | 🌐 C | 📅 2026-08-12 - An open-source toolchain for side-channel power analysis and fault injection attacks with complete hardware and software stack.
* [lascar](https://github.com/Ledger-Donjon/lascar) ⭐ 409 | 🐛 3 | 🌐 Python | 📅 2023-09-05 - Fast Python SCA library from Ledger's hardware wallet security team supporting CPA, DPA, MIA, template attacks, and ML-based attacks with lazy loading for large trace datasets.
* [scared](https://github.com/eshard/scared) ⭐ 114 | 🐛 1 | 🌐 Python | 📅 2026-07-16 - Industrial-grade side-channel analysis framework from eShard with best-in-class trace processing performance; supports CPA, DPA, TVLA/NICV leakage assessment, and very large trace datasets.
* [SCALE](https://github.com/danpage/scale) ⭐ 48 | 🐛 0 | 📅 2023-09-20 - Side-Channel Attack Lab Exercises providing educational material for learning power analysis attacks with low-cost hardware.

### Fault Injection

* [PicoEMP](https://github.com/newaetech/chipshouter-picoemp) ⭐ 753 | 🐛 23 | 🌐 C | 📅 2024-08-28 - NewAE's open hardware EMFI tool built on a Raspberry Pi Pico and photographic-flash transformer circuit; the community standard entry-level electromagnetic fault injection platform.
* [PicoGlitcher](https://github.com/MKesenheimer/fault-injection-library) ⭐ 203 | 🐛 7 | 🌐 Python | 📅 2026-07-29 - RP2040/RP2350-based voltage glitching platform with 66A crowbar, sub-10ns pulse resolution via PIO sampling, and a high-level Python (`findus`) API for scripting attack campaigns. Validated by SySS Research.
* [Faulty Cat](https://github.com/ElectronicCats/faultycat) ⭐ 150 | 🐛 3 | 📅 2026-07-06 - Low-cost open hardware EMFI tool from Electronic Cats built on an RP2040, offering both electromagnetic and crowbar voltage-glitching fault injection with single-shot and parameter-sweep campaign modes.
* [EM-Fault-It-Yourself](https://github.com/fgsect/EM-Fault-It-Yourself) ⭐ 15 | 🐛 0 | 🌐 C | 📅 2022-12-13 - Motorized XYZ-stage EMFI platform targeting desktop and server SoCs (successfully attacked the AMD Secure Processor), with 2.5µm accuracy, 100mm travel, and a web UI for automated scanning campaigns. IEEE HOST 2022.

### Logic Analyzer

* [Saleae](https://www.saleae.com/) 💰 - Commercial logic analyzer hardware ($149–$499+) with proprietary software; widely used for decoding SPI, I2C, UART, and other embedded protocols.
* [Sigrok](https://sigrok.org/) - Portable, cross-platform, Free/Libre/Open-Source signal analysis software suite that supports various device types (e.g. logic analyzers, oscilloscopes, and many more).

### RF Tools (Non-SDR)

* [Proxmark3](https://github.com/RfidResearchGroup/proxmark3) ⭐ 5,936 | 🐛 79 | 🌐 C | 📅 2026-08-01 - Open-source RFID research platform for low-level interaction, analysis, and testing across a wide range of LF and HF tags and systems.
* [ChameleonUltra](https://github.com/RfidResearchGroup/ChameleonUltra) ⭐ 2,913 | 🐛 115 | 🌐 C | 📅 2026-08-10 - Pocket friendly powerful LF and HF emulation & manipulation tool which is based on the open-source project ChameleonMini.
* [Awesome Flipper Zero](https://github.com/RogueMaster/awesome-flipperzero-withModules) ⭐ 2,002 | 🐛 0 | 🌐 C | 📅 2026-08-06 - A collection of Awesome resources for the Flipper Zero device.
* [Flipper Zero](https://docs.flipper.net/) - Portable multi-tool for pentesters and geeks in a toy-like body. It loves hacking digital stuff, such as radio protocols, access control systems, hardware and more.
* [Yard Stick One](https://greatscottgadgets.com/yardstickone/) - Transmit or receive digital wireless signals at frequencies below 1 GHz. It uses the same radio circuit as the popular IM-Me.
* [Bruce](https://bruce.computer/) - Powerful open-source ESP32 firmware designed for offensive security and Red Team operations.

### Software Defined Radios

* [HackRF One](https://greatscottgadgets.com/hackrf/) - Software Defined Radio peripheral capable of transmission or reception of radio signals from 1 MHz to 6 GHz.
* [ADALM-PLUTO (PlutoSDR)](https://wiki.analog.com/university/tools/pluto) - Active learning module (PlutoSDR) used to explore software-defined radio, RF experimentation, and wireless communications.
* [RTL-SDR](https://www.rtl-sdr.com/) - Very cheap \~$30 USB dongle that can be used as a computer based radio scanner for receiving live radio signals in your area (no internet required).

### Software Defined Radio Software

* [Future SDR](https://www.futuresdr.org/) - Supports Blocks with synchronous or asynchronous implementations for stream-based or message-based data processing.
* [Maia SDR](https://maia-sdr.org/) - Open-source FPGA-based SDR project focusing on the ADALM Pluto.

### Wifi Tools

* [Pwnagotchi](https://pwnagotchi.ai/) - A2C-based “AI” powered by bettercap and running on a Raspberry Pi Zero W that learns from its surrounding WiFi environment in order to maximize the crackable WPA key material it captures.
* [ESP32Maurauder](https://github.com/justcallmekoko/ESP32Marauder) ⭐ 11,947 | 🐛 320 | 🌐 C++ | 📅 2026-08-12 - A suite of WiFi/Bluetooth offensive and defensive tools for the ESP32.

## Further Learning and Training

* [HardwareAllTheThings](https://github.com/swisskyrepo/HardwareAllTheThings) ⭐ 926 | 🐛 0 | 🌐 HTML | 📅 2026-08-09 - Actively maintained hardware and IoT pentesting wiki by swisskyrepo covering fault injection, JTAG/SWD/UART exploitation, firmware dumping, side-channel attacks, and RF attacks with practical tooling references.
* [DVRF](https://github.com/praetorian-inc/DVRF) ⚠️ Archived - Damn Vulnerable Router Firmware: modified Linksys firmware containing intentional MIPS/ARM binary exploitation challenges (buffer overflows, format strings, heap bugs) runnable under QEMU without physical hardware.
* [DVID](https://github.com/Vulcainreo/DVID) ⭐ 225 | 🐛 3 | 🌐 C | 📅 2024-02-12 - Damn Vulnerable IoT Device: open hardware ATmega328p board (Gerbers published) purpose-built for practicing UART extraction, firmware dumping, and Bluetooth sniffing attacks on physical hardware.
* [Embeddedsecurity.io](https://embeddedsecurity.io/) - Beginners resource on embedded systems security.
* [SecuringHardware.com](https://learn.securinghardware.com/) 💰 - Paid hardware security training courses by Joe Fitz [@securelyfitz](https://x.com/securelyfitz).
* [GrandIdeaStudio.com](https://grandideastudio.com/training/) 💰 - Paid hardware hacking training with Joe Grand (aka Kingpin).
* Fault Injection and Side Channel Attacks
  * [synacktiv - Blog](https://www.synacktiv.com/en/publications/how-to-voltage-fault-injection) - A how-to on voltage fault injection.
  * [raelize.com - Blog](https://raelize.com/blog) - Great insight into hardware hacking such as fault injection and side-channel attacks.
* [Microcorruption](https://microcorruption.com/) - Browser-based embedded security CTF presenting a series of challenges on a fictional MSP430-based lock system, covering stack overflows through advanced memory corruption exploitation.
* [MITRE eCTF](https://ectf.mitre.org/) - Annual collegiate "build-then-break" competition where teams harden and then attack each other's firmware on real ARM Cortex-M microcontrollers; open source tooling and insecure reference designs published each year.

## Open Source Intelligence (OSINT)

* [Awesome OSINT](https://github.com/jivoi/awesome-osint) ⭐ 28,052 | 🐛 9 | 📅 2026-08-03

## Other Awesome Lists

List of security lists.

* General Security
  * [Hacking](https://github.com/carpedm20/awesome-hacking) ⭐ 16,855 | 🐛 69 | 📅 2024-06-02
  * [Security](https://github.com/sbilly/awesome-security) ⭐ 14,744 | 🐛 302 | 📅 2026-01-11
  * [Malware Analysis](https://github.com/rshipp/awesome-malware-analysis) ⭐ 14,113 | 🐛 25 | 📅 2024-06-07
  * [Capture the Flag](https://github.com/apsdehal/awesome-ctf) ⭐ 11,750 | 🐛 64 | 🌐 JavaScript | 📅 2024-07-22
  * [Honeypots](https://github.com/paralax/awesome-honeypots) ⭐ 10,517 | 🐛 20 | 🌐 Python | 📅 2026-06-01
  * [Android Security](https://github.com/ashishb/android-security-awesome) ⭐ 9,604 | 🐛 2 | 🌐 Makefile | 📅 2026-08-10
  * [Incident Response](https://github.com/meirwah/awesome-incident-response) ⭐ 9,319 | 🐛 73 | 📅 2026-07-15
  * [Application Security](https://github.com/paragonie/awesome-appsec) ⭐ 7,023 | 🐛 40 | 🌐 PHP | 📅 2025-02-22
  * [Fuzzing](https://github.com/cpuu/awesome-fuzzing) ⭐ 985 | 🐛 1 | 📅 2026-07-09
* Embedded
  * [General Embedded](https://github.com/nhivp/Awesome-Embedded) ⭐ 8,972 | 🐛 2 | 📅 2026-08-12
  * [Embedded and IoT Security](https://github.com/fkie-cad/awesome-embedded-and-iot-security) ⭐ 2,414 | 🐛 2 | 📅 2023-10-17
* Domain Specific
  * Automotive
    * [CANbus](https://github.com/iDoka/awesome-canbus) ⭐ 3,385 | 🐛 4 | 📅 2026-08-07
    * [CANb IDs](https://github.com/iDoka/awesome-automotive-can-id) ⭐ 975 | 🐛 0 | 📅 2026-08-12
    * [Awesome Automotive Security](https://github.com/hexsecs/awesome-automotive-security) ⭐ 9 | 🐛 0 | 📅 2026-05-16
* Meta
  * [awesome](https://github.com/sindresorhus/awesome) ⭐ 495,188 | 🐛 100 | 📅 2026-06-30
  * [lists](https://github.com/jnv/lists) ⭐ 11,413 | 🐛 20 | 📅 2026-03-23

## Contribute

Contributions welcome! Read the [contribution guidelines](contributing.md) first.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-13._
