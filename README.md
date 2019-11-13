# zircon-notes
对zircon内核的一些分析，欢迎补充！


### Base Library
```
//FBL is the Fuchsia Base Library, which is shared between kernel and userspace.
zircon/system/ulib/fbl
kernel/lib/fbl
```



```
.
├── arch
│   ├── arm64
│   │   ├── hypervisor
│   │   │   └── gic
│   │   └── include
│   │       └── arch
│   │           └── arm64
│   │               └── hypervisor
│   │                   └── gic
│   └── x86
│       ├── cpuid
│       │   └── include
│       │       └── arch
│       │           └── x86
│       ├── hypervisor
│       ├── include
│       │   └── arch
│       │       └── x86
│       └── page_tables
│           └── include
│               └── arch
│                   └── x86
│                       └── page_tables
├── debugcommands
├── dev
│   ├── hdcp
│   │   └── amlogic_s912
│   ├── hw_rng
│   │   └── include
│   │       └── dev
│   ├── intel_rng
│   ├── interrupt
│   │   ├── arm_gic
│   │   │   ├── common
│   │   │   │   └── include
│   │   │   │       └── dev
│   │   │   │           └── interrupt
│   │   │   ├── v2
│   │   │   │   └── include
│   │   │   │       └── dev
│   │   │   │           └── interrupt
│   │   │   └── v3
│   │   │       └── include
│   │   │           └── dev
│   │   │               └── interrupt
│   │   └── include
│   │       └── dev
│   ├── iommu
│   │   ├── dummy
│   │   │   └── include
│   │   │       └── dev
│   │   │           └── iommu
│   │   └── intel
│   │       └── include
│   │           └── dev
│   │               └── iommu
│   ├── pcie
│   │   ├── address_provider
│   │   └── include
│   │       └── dev
│   │           └── address_provider
│   ├── pdev
│   │   ├── include
│   │   │   └── pdev
│   │   ├── interrupt
│   │   ├── power
│   │   └── uart
│   ├── power
│   │   ├── hisi
│   │   └── msm
│   ├── psci
│   │   └── include
│   │       └── dev
│   ├── timer
│   │   └── arm_generic
│   │       └── include
│   │           └── dev
│   │               └── timer
│   ├── uart
│   │   ├── amlogic_s905
│   │   ├── dw8250
│   │   ├── msm
│   │   ├── mt8167
│   │   ├── nxp-imx
│   │   └── pl011
│   └── udisplay
│       └── include
│           └── dev
├── hypervisor
│   └── include
│       └── hypervisor
├── include
│   ├── arch
│   ├── dev
│   ├── kernel
│   ├── ktl
│   ├── lib
│   ├── lk
│   ├── platform
│   ├── sys
│   └── syscalls
├── kernel
├── lib
│   ├── acpica
│   ├── acpi_tables
│   │   └── include
│   │       └── lib
│   ├── cbuf
│   │   └── include
│   │       └── lib
│   ├── code_patching
│   │   └── include
│   │       └── lib
│   ├── console
│   │   └── include
│   │       └── lib
│   ├── counters
│   │   └── include
│   │       └── lib
│   ├── crashlog
│   │   └── include
│   │       └── lib
│   ├── crypto
│   │   ├── entropy
│   │   └── include
│   │       └── lib
│   │           └── crypto
│   │               └── entropy
│   ├── debug
│   ├── debugcommands
│   ├── debuglog
│   │   └── include
│   │       └── lib
│   ├── efi
│   │   └── include
│   │       └── efi
│   │           └── protocol
│   ├── fbl
│   │   └── include
│   │       └── fbl
│   ├── fixed_point
│   │   └── include
│   │       └── lib
│   ├── gfx
│   │   └── include
│   │       └── lib
│   ├── gfxconsole
│   │   └── include
│   │       └── lib
│   ├── header_tests
│   ├── heap
│   │   ├── cmpctmalloc
│   │   │   └── include
│   │   │       └── lib
│   │   └── include
│   │       └── lib
│   ├── hypervisor
│   ├── instrumentation
│   │   └── include
│   │       └── lib
│   │           └── instrumentation
│   ├── io
│   │   └── include
│   │       └── lib
│   ├── ktrace
│   │   └── include
│   │       └── lib
│   │           └── ktrace
│   ├── libc
│   │   ├── include
│   │   ├── limits-dummy
│   │   └── string
│   │       └── arch
│   │           ├── arm64
│   │           └── x86
│   ├── lockdep
│   ├── memory_limit
│   │   └── include
│   │       └── lib
│   ├── mtrace
│   │   └── include
│   │       └── lib
│   ├── oom
│   │   └── include
│   │       └── lib
│   ├── pci
│   │   └── include
│   │       └── lib
│   │           └── pci
│   ├── perfmon
│   │   └── include
│   │       └── lib
│   ├── pow2_range_allocator
│   │   └── include
│   │       └── lib
│   ├── topology
│   │   └── include
│   │       └── lib
│   ├── unittest
│   │   └── include
│   │       └── lib
│   │           └── unittest
│   ├── userabi
│   │   ├── include
│   │   │   └── lib
│   │   │       └── userabi
│   │   └── userboot
│   ├── userboot
│   ├── user_copy
│   │   └── include
│   │       └── lib
│   │           └── user_copy
│   ├── vdso
│   ├── version
│   │   └── include
│   │       └── lib
│   └── watchdog
│       └── include
│           └── lib
├── object
│   └── include
│       └── object
├── platform
│   ├── generic-arm
│   └── pc
│       └── include
│           └── platform
│               └── pc
├── project
│   └── virtual
├── scripts
├── syscalls
├── target
│   ├── arm64
│   │   ├── board
│   │   │   ├── as370
│   │   │   ├── cleo
│   │   │   ├── hikey960
│   │   │   ├── kirin970
│   │   │   ├── msm8x53-som
│   │   │   ├── mt8167s_ref
│   │   │   ├── qemu
│   │   │   ├── vim2
│   │   │   │   └── firmware
│   │   │   └── visalia
│   │   ├── boot-shim
│   │   └── dtb
│   └── pc
│       └── multiboot
├── tests
├── top
└── vm
    └── include
        └── vm

```
