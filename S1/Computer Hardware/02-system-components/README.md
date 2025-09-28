# Module 2: System Components and Motherboards

## Learning Objectives
By the end of this module, you will be able to:
- Identify major motherboard components and their functions
- Understand chipset architecture and its role in system design
- Explain different motherboard form factors and their applications
- Describe BIOS/UEFI firmware and its configuration options
- Analyze expansion slots and their compatibility requirements
- Troubleshoot common motherboard-related issues

## Reading Assignments

### Primary Reading: Mueller - Upgrading and Repairing PCs
- **Chapter 4**: Motherboards and Buses (Pages 151-250)
  - Motherboard form factors
  - Chipset types and functions
  - System buses and slots
  - BIOS/UEFI firmware
- **Chapter 5**: System Components (Pages 251-320)
  - Power connectors
  - System clocks and timing
  - Motherboard selection criteria
- **Chapter 6**: System Setup and Configuration (Pages 321-380)
  - BIOS/UEFI setup
  - Hardware configuration
  - Boot process

### Supplementary Reading: Reagan - Troubleshooting the PC
- **Chapter 2**: System Components (Pages 45-80)
  - Component identification
  - Compatibility issues
- **Chapter 4**: Motherboard Troubleshooting (Pages 125-160)
  - Common motherboard failures
  - Diagnostic procedures

## Key Concepts

### 1. Motherboard Overview
The motherboard (also called mainboard or system board) is the primary circuit board that connects all computer components together.

**Primary Functions:**
- Houses the CPU socket
- Provides memory slots (DIMM/SO-DIMM)
- Contains expansion slots for add-in cards
- Integrates basic I/O controllers
- Distributes power to components
- Provides system timing and clocking

### 2. Motherboard Form Factors

#### ATX (Advanced Technology eXtended)
- **Dimensions**: 305mm × 244mm (12" × 9.6")
- **Features**: Full-size with maximum expansion capability
- **Power**: 24-pin main power connector + 4/8-pin CPU power
- **Expansion**: Up to 7 expansion slots
- **Applications**: Desktop PCs, workstations, gaming systems

#### Micro-ATX (µATX)
- **Dimensions**: 244mm × 244mm (9.6" × 9.6")
- **Features**: Compact design with reduced expansion
- **Power**: Same as ATX
- **Expansion**: Up to 4 expansion slots
- **Applications**: Budget systems, small form factor PCs

#### Mini-ITX
- **Dimensions**: 170mm × 170mm (6.7" × 6.7")
- **Features**: Ultra-compact with minimal expansion
- **Power**: 24-pin main + CPU power (sometimes external adapter)
- **Expansion**: 1 expansion slot typically
- **Applications**: HTPCs, embedded systems, ultra-compact builds

#### E-ATX (Extended ATX)
- **Dimensions**: 305mm × 330mm (12" × 13")
- **Features**: Extended length for high-end systems
- **Power**: Multiple power connectors
- **Expansion**: 8+ expansion slots
- **Applications**: High-end workstations, servers, enthusiast systems

### 3. Chipset Architecture

The chipset is a group of integrated circuits that manage data flow between the CPU, memory, and peripheral devices.

#### Traditional Two-Chip Design
**Northbridge (Memory Controller Hub)**
- Connects CPU to high-speed components
- Controls memory access (RAM)
- Manages AGP/PCIe graphics slots
- Handles high-speed I/O

**Southbridge (I/O Controller Hub)**
- Manages slower peripheral devices
- Controls USB, SATA, Ethernet
- Handles legacy ports (PS/2, parallel, serial)
- Manages system BIOS/UEFI

#### Modern Single-Chip Design
**System on Chip (SoC) Integration**
- Memory controller integrated into CPU
- Single chipset handles all I/O
- Platform Controller Hub (PCH) design
- Reduced power consumption and latency

#### Major Chipset Manufacturers
**Intel Chipsets:**
- Z-series: Enthusiast/overclocking features
- H-series: Mainstream desktop
- B-series: Business/value
- Q-series: Corporate with vPro

**AMD Chipsets:**
- X-series: High-end enthusiast
- B-series: Mainstream
- A-series: Entry-level

### 4. CPU Sockets

#### Intel Sockets
**LGA (Land Grid Array) - Current**
- **LGA 1700**: 12th/13th gen Core processors
- **LGA 1200**: 10th/11th gen Core processors
- **LGA 2066**: High-end Desktop (HEDT) X-series

**Legacy Intel Sockets**
- **LGA 1151**: 6th-9th gen Core processors
- **LGA 1155**: 2nd/3rd gen Core processors
- **Socket 478**: Pentium 4

#### AMD Sockets
**PGA (Pin Grid Array) and AM Series**
- **AM5**: Ryzen 7000 series (LGA design)
- **AM4**: Ryzen 1000-5000 series
- **TR4/sTRX4**: Threadripper HEDT processors

**Socket Characteristics:**
- Pin count and arrangement
- Voltage requirements
- Thermal design power (TDP) support
- Upgrade path compatibility

### 5. Memory Slots and Configuration

#### DIMM (Dual Inline Memory Module)
- **Desktop Standard**: 288-pin DDR4/DDR5
- **Capacity**: Up to 128GB per slot (current)
- **Channels**: Dual/Quad channel support
- **Speed**: DDR4: 2133-3200+ MHz, DDR5: 4800-6400+ MHz

#### SO-DIMM (Small Outline DIMM)
- **Laptop Standard**: 260-pin DDR4, 262-pin DDR5
- **Capacity**: Up to 64GB per slot
- **Applications**: Laptops, mini-ITX systems

#### Memory Configuration Rules
- **Single Channel**: One DIMM installed
- **Dual Channel**: Two DIMMs in matching colored slots
- **Quad Channel**: Four DIMMs in specific slot arrangement
- **Interleaving**: Alternating memory access for performance

### 6. Expansion Slots

#### PCIe (Peripheral Component Interconnect Express)
**PCIe Generations:**
- **PCIe 3.0**: 8 GT/s per lane (1 GB/s)
- **PCIe 4.0**: 16 GT/s per lane (2 GB/s)
- **PCIe 5.0**: 32 GT/s per lane (4 GB/s)

**PCIe Slot Types:**
- **x16**: Graphics cards, high-bandwidth devices
- **x8**: High-performance network cards, RAID controllers
- **x4**: NVMe SSDs, moderate bandwidth cards
- **x1**: Sound cards, low-bandwidth peripherals

#### Legacy Expansion Slots
**PCI (Peripheral Component Interconnect)**
- **Speed**: 133 MB/s (32-bit, 33 MHz)
- **Applications**: Legacy cards, some embedded systems
- **Status**: Largely obsoleted by PCIe

**AGP (Accelerated Graphics Port)**
- **Speed**: 266-2133 MB/s (1x-8x)
- **Applications**: Graphics cards (pre-PCIe era)
- **Status**: Completely obsoleted

### 7. Power Connectors

#### Main Power Connectors
**24-Pin ATX Power**
- Provides +12V, +5V, +3.3V, -12V, +5V standby
- Evolution from 20-pin legacy connector
- Required for motherboard operation

**CPU Power Connectors**
- **4-Pin**: Basic CPU power (older systems)
- **8-Pin**: Modern CPU power (EPS12V)
- **4+4 Pin**: Compatible with both 4-pin and 8-pin

#### Auxiliary Power Connectors
**SATA Power**
- 15-pin connector for SATA drives
- Provides +12V, +5V, +3.3V

**Molex (4-Pin Peripheral)**
- Legacy power connector
- Provides +12V and +5V
- Still used for fans and some accessories

**PCIe Power**
- **6-Pin**: Up to 75W for graphics cards
- **8-Pin**: Up to 150W for graphics cards
- **6+2 Pin**: Compatible with both 6-pin and 8-pin

### 8. BIOS/UEFI Firmware

#### BIOS (Basic Input/Output System)
**Functions:**
- Power-On Self Test (POST)
- Hardware initialization
- Boot device selection
- Basic hardware configuration

**Limitations:**
- 16-bit code execution
- 1MB memory addressing
- MBR boot support only
- Text-based interface
- Limited storage (2-8MB)

#### UEFI (Unified Extensible Firmware Interface)
**Advantages over BIOS:**
- 32-bit or 64-bit code execution
- GPT partition support (>2TB drives)
- Secure Boot capability
- Graphical user interface
- Mouse support
- Larger storage capacity
- Faster boot times
- Network capabilities

**UEFI Components:**
- Boot Manager
- Runtime Services
- Boot Services
- Device Drivers
- Security features

#### Common BIOS/UEFI Settings
**Boot Configuration:**
- Boot device priority
- UEFI vs Legacy boot mode
- Secure Boot enable/disable
- Fast Boot options

**CPU Settings:**
- CPU ratio/multiplier
- Base clock (BCLK)
- Voltage settings
- Power management

**Memory Settings:**
- Memory frequency
- Memory timings
- Memory voltage
- XMP/DOCP profiles

**Storage Settings:**
- SATA mode (AHCI/IDE/RAID)
- NVMe configuration
- Hot swap enable/disable

### 9. System Buses

#### Front Side Bus (FSB) - Legacy
- Connected CPU to Northbridge
- Shared between CPU and memory
- Bottleneck in older systems

#### Quick Path Interconnect (QPI) - Intel
- Point-to-point connections
- Higher bandwidth than FSB
- Used in multi-processor systems

#### HyperTransport - AMD
- High-speed point-to-point connection
- Scalable bandwidth
- Used in AMD systems

#### DMI (Direct Media Interface)
- Connects CPU to chipset in modern systems
- Replaced traditional FSB architecture
- Various generations with increasing bandwidth

### 10. Integrated Components

#### Audio
- **Standards**: HD Audio, AC'97 (legacy)
- **Channels**: 2.1 to 7.1 surround sound
- **Quality**: 16-24 bit, 44.1-192 kHz sampling
- **Connectors**: 3.5mm jacks, optical S/PDIF

#### Network
- **Ethernet**: 10/100/1000 Mbps (Gigabit)
- **Wireless**: Wi-Fi 6/6E (802.11ax)
- **Bluetooth**: 5.0+ support
- **Controllers**: Intel, Realtek, Broadcom

#### USB Controllers
- **USB 2.0**: 480 Mbps (High Speed)
- **USB 3.0/3.1 Gen 1**: 5 Gbps (SuperSpeed)
- **USB 3.1 Gen 2**: 10 Gbps (SuperSpeed+)
- **USB 3.2**: Up to 20 Gbps
- **USB4/Thunderbolt 4**: 40 Gbps

## Motherboard Selection Criteria

### 1. CPU Compatibility
- Socket type match
- Chipset support for CPU features
- BIOS/UEFI version compatibility
- Power delivery adequacy

### 2. Memory Support
- Maximum capacity support
- Memory type (DDR4/DDR5)
- Speed support (JEDEC vs XMP)
- Number of memory slots

### 3. Expansion Requirements
- PCIe slot configuration
- Number and type of slots needed
- Multi-GPU support (SLI/CrossFire)
- M.2 slot availability

### 4. I/O Requirements
- USB port quantity and types
- Audio output requirements
- Network connectivity needs
- Legacy port requirements

### 5. Form Factor Considerations
- Case compatibility
- Available space for components
- Cooling requirements
- Cable management

### 6. Budget Constraints
- Feature requirements vs cost
- Upgrade path considerations
- Brand preferences and warranty

## Troubleshooting Common Issues

### 1. No Power/No POST
**Symptoms:**
- No lights, fans, or activity
- Fans spin but no display
- POST codes or beep patterns

**Troubleshooting Steps:**
1. Check power supply connections
2. Verify RAM installation
3. Remove unnecessary components
4. Check CPU installation
5. Test with minimal configuration
6. Inspect for physical damage

### 2. Boot Failures
**Symptoms:**
- System starts but won't boot OS
- Boot device not found errors
- Continuous restart loops

**Troubleshooting Steps:**
1. Check boot device connections
2. Verify BIOS/UEFI boot settings
3. Test with known good storage device
4. Check for corrupted boot files
5. Reset BIOS/UEFI to defaults

### 3. Stability Issues
**Symptoms:**
- Random crashes or freezes
- Blue screens of death (BSOD)
- Intermittent hardware failures

**Troubleshooting Steps:**
1. Test memory with MemTest86
2. Check CPU and system temperatures
3. Verify power supply adequacy
4. Update BIOS/UEFI firmware
5. Test individual components

### 4. Performance Problems
**Symptoms:**
- Slower than expected performance
- High CPU or memory usage
- Thermal throttling

**Troubleshooting Steps:**
1. Check clock speeds and voltages
2. Verify thermal paste application
3. Ensure proper ventilation
4. Update drivers and firmware
5. Check for background processes

## Laboratory Exercises

### Lab 1: Motherboard Identification
**Objective**: Identify and document motherboard components

**Required Tools:**
- Various motherboards (different form factors)
- Magnifying glass
- Digital camera
- Component identification charts

**Procedure:**
1. Identify motherboard form factor
2. Locate and photograph major components
3. Identify chipset model and specifications
4. Document expansion slots and connectors
5. Create component location diagram

### Lab 2: BIOS/UEFI Configuration
**Objective**: Navigate and configure firmware settings

**Required Equipment:**
- Test system with accessible BIOS/UEFI
- USB drive for settings backup
- Documentation materials

**Tasks:**
1. Enter BIOS/UEFI setup
2. Navigate through all menu sections
3. Document default settings
4. Enable/disable various features
5. Save and restore configurations
6. Update firmware (if safe)

### Lab 3: Component Compatibility Testing
**Objective**: Test component compatibility and installation

**Required Components:**
- Different RAM modules
- Various expansion cards
- Multiple storage devices
- Power supply tester

**Procedure:**
1. Test RAM compatibility and speed
2. Install different expansion cards
3. Configure RAID arrays
4. Test power supply voltages
5. Document compatibility issues

## Study Activities

### Activity 1: Motherboard Comparison Chart
Create a detailed comparison of three different motherboard models:
- Form factor and dimensions
- Supported CPU sockets
- Memory specifications
- Expansion slot configuration
- Integrated features
- Price and target market

### Activity 2: Chipset Research
Research and compare chipsets from Intel and AMD:
- Feature differences between series
- Performance characteristics
- Overclocking support
- Integrated capabilities
- Power consumption

### Activity 3: BIOS/UEFI Feature Analysis
Document and explain 20 common BIOS/UEFI settings:
- Setting name and location
- Function and impact
- Recommended values
- Compatibility considerations

## Self-Assessment Questions

### Multiple Choice
1. What is the primary function of the chipset?
   a) Process instructions
   b) Store data temporarily
   c) Manage data flow between components
   d) Provide graphical output

2. Which power connector is required for modern motherboards?
   a) 20-pin ATX
   b) 24-pin ATX
   c) 4-pin Molex
   d) SATA power

3. What advantage does UEFI have over traditional BIOS?
   a) Smaller storage requirements
   b) Faster processor speeds
   c) Support for drives larger than 2TB
   d) Lower power consumption

### Short Answer
1. Explain the difference between Northbridge and Southbridge chipset designs.
2. List five factors to consider when selecting a motherboard.
3. Describe the boot process from power-on to operating system load.

### Problem Solving
1. A system powers on but displays no video output. List a systematic troubleshooting approach.
2. Design a motherboard specification for a gaming system with specific requirements.

## Key Terms and Definitions

**ATX**: Standard motherboard form factor (305mm × 244mm)

**Chipset**: Group of integrated circuits managing data flow

**DIMM**: Dual Inline Memory Module for desktop systems

**POST**: Power-On Self Test performed during boot

**PCIe**: High-speed serial expansion bus standard

**Socket**: CPU mounting and connection interface

**UEFI**: Modern firmware interface replacing BIOS

**VRM**: Voltage Regulator Module for CPU power delivery

**FSB**: Front Side Bus (legacy CPU-to-memory connection)

**DMI**: Direct Media Interface (modern CPU-to-chipset connection)

## Additional Resources

### Manufacturer Documentation
- Intel Chipset Documentation
- AMD Platform Documentation
- ASUS Motherboard Manuals
- MSI Technical Specifications
- Gigabyte Support Resources

### Online Tools
- CPU Socket Compatibility Charts
- Memory Compatibility Lists (QVL)
- PCIe Lane Configuration Tools
- Power Supply Calculators

### Professional References
- ATX Specification Documents
- UEFI Specification
- PCIe Specification
- DDR4/DDR5 JEDEC Standards

## Assessment Checklist
- [ ] Can identify major motherboard components
- [ ] Understands different form factors and applications
- [ ] Knows chipset functions and architecture
- [ ] Can configure BIOS/UEFI settings
- [ ] Understands expansion slot types and compatibility
- [ ] Can troubleshoot common motherboard issues
- [ ] Knows power requirements and connections
- [ ] Understands memory configuration rules

## Next Module Preview
**Module 3: Processors and Memory** will cover:
- CPU architecture and specifications
- Memory technologies and optimization
- Cache systems and performance
- Overclocking principles and practice

---
*Estimated Study Time: 10-12 hours*
*Prerequisites: Module 1 completion*
*Last Updated: [Current Date]*
