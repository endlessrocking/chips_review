### GCN 1st generation

- support for 64-bit addressing (x86-64address space) with unified address space for CPU and GPU[[12\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-anandUVM-12)
  - support for [PCI-E 3.0](https://en.wikipedia.org/wiki/PCI_Express#PCI_Express_3.0)[[21\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-21)
  - GPU sends [interrupt requests](https://en.wikipedia.org/wiki/Interrupt_request) to CPU on various events (such as [page faults](https://en.wikipedia.org/wiki/Page_fault))
- support for Partially Resident Textures[[22\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-22), which enable virtual memory support through [DirectX](https://en.wikipedia.org/wiki/DirectX) and [OpenGL](https://en.wikipedia.org/wiki/OpenGL) extensions
- [AMD PowerTune](https://en.wikipedia.org/wiki/AMD_PowerTune) support, which dynamically adjusts performance to stay within a specific TDP[[23\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-23)
- support for [Mantle (API)](https://en.wikipedia.org/wiki/Mantle_(API))

There are Asynchronous Compute Engines controlling computation and dispatching.[[11\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-amd_final.pdf-11) [[24\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-24)

#### ZeroCore Power

ZeroCore Power is a long idle power saving technology, shutting off functional units of the GPU when not in use.[[25\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-25) AMD ZeroCore Power technology supplements [AMD PowerTune](https://en.wikipedia.org/wiki/AMD_PowerTune).

#### Chips

discrete GPUs (Southern Islands family):

- Oland
- Cape Verde
- Pitcairn
- Tahiti

### GCN 2nd generation

![img](https://upload.wikimedia.org/wikipedia/commons/thumb/3/34/AMD_PowerTune_Bonaire.svg/220px-AMD_PowerTune_Bonaire.svg.png)

GCN 2nd generation was introduced with Radeon HD 7790 and is also found in Radeon HD 8770, R7 260/260X, R9 290/290X, R9 295X2, R7 360, R9 390/390X, as well as [Steamroller](https://en.wikipedia.org/wiki/Steamroller_(microarchitecture))-based [Desktop Kaveri APUs](https://en.wikipedia.org/wiki/List_of_AMD_Accelerated_Processing_Unit_microprocessors#"Kaveri"_(2014,_28_nm)) and [Mobile Kaveri APUs](https://en.wikipedia.org/wiki/List_of_AMD_Accelerated_Processing_Unit_microprocessors#"Kaveri"_2014,_28_nm) and in the [Puma](https://en.wikipedia.org/wiki/Puma_(microarchitecture))-based ["Beema" and "Mullins" APUs](https://en.wikipedia.org/wiki/List_of_AMD_Accelerated_Processing_Unit_microprocessors#.22Beema.22.2C_.22Mullins.22_.282014.2C_28_nm.29). It has multiple advantages over the original GCN, including [FreeSync](https://en.wikipedia.org/wiki/FreeSync) support, [AMD TrueAudio](https://en.wikipedia.org/wiki/AMD_TrueAudio) and a revised version of [AMD PowerTune](https://en.wikipedia.org/wiki/AMD_PowerTune) technology.

GCN 2nd generation introduced an entity called "Shader Engine" (SE). A Shader Engine comprises one geometry processor, up to 44 CUs (Hawaii chip), rasterizers, ROPs, and L1 cache. Not part of a Shader Engine is the Graphics Command Processor, the 8 ACEs, the L2 cache and memory controllers as well as the audio and video accelerators, the display controllers, the 2 DMA controllers and the PCIe interface.

The A10-7850K "Kaveri" contains 8 CUs (compute units) and 8 Asynchronous Compute Engines for independent scheduling and work item dispatching.[[26\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-26)

At AMD Developer Summit (APU) in November 2013 Michael Mantor presented the [Radeon R9 290X](https://en.wikipedia.org/wiki/AMD_Radeon_Rx_200_Series#Radeon_R9_290).[[27\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-gs4152-27)

#### Chips

discrete GPUs (Sea Islands family):

- Bonaire
- Hawaii

integrated into APUs:

- Temash
- Kabini
- Liverpool (i.e. the APU found in the Playstation 4)
- Durango (i.e. the APU found in the Xbox One and Xbox One S)
- Kaveri
- Godavari
- Mullins
- Beema
- Carrizo-L

### GCN 3rd generation

GCN 3rd generation[[28\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-28) was introduced in 2014 with the [Radeon R9 285](https://en.wikipedia.org/wiki/List_of_AMD_graphics_processing_units#Radeon-R9-285) and R9 M295X, which have the "Tonga" GPU. It features improved tessellation performance, lossless delta color compression in order to reduce memory bandwidth usage, an updated and more efficient instruction set, a new high quality scaler for video, and a new multimedia engine (video encoder/decoder). Delta color compression is supported in Mesa.[[29\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-29) However, its double precision performance is worse compared to previous generation.[[30\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-30)

#### Chips

discrete GPUs:

- Tonga (Volcanic Islands family), comes with [UVD](https://en.wikipedia.org/wiki/UVD) 5.0 (Unified Video Decoder)
- Fiji (Pirate Islands family), comes with UVD 6.0 and [High Bandwidth Memory](https://en.wikipedia.org/wiki/High_Bandwidth_Memory) (HBM 1)

integrated into APUs:

- Carrizo, comes with UVD 6.0
- Bristol Ridge[[31\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-AMDGen7-31)
- Stoney Ridge[[31\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-AMDGen7-31)

### Polaris (GCN 4th generation)

GPUs of the Arctic Islands-family were introduced in Q2 of 2016 with the [AMD Radeon 400 series](https://en.wikipedia.org/wiki/AMD_Radeon_400_series). The 3D-engine (i.e. GCA (Graphics and Compute array) or GFX) is identical to that found in the Tonga-chips.[[32\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-RadeonFeatureMatrix-32) But Polaris feature a newer Display Controller engine, UVD version 6.3, etc.

All Polaris-based chips other than the Polaris 30 are produced on the 14 nm FinFET process.[[33\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-33) The slightly newer refreshed Polaris 30 is built on the 12 nm LP process node. The fourth generation GCN instruction set architecture is compatible with the third generation. It is an optimization for 14 nm FinFET process enabling higher GPU clock speeds than with the 3rd GCN generation.[[34\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-anand_vega-34) Architectural improvements include new hardware schedulers, a new primitive discard accelerator, a new display controller, and an updated UVD that can decode HEVC at 4K resolutions at 60 frames per second with 10 bits per color channel.

#### Chips

discrete GPUs:[[35\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-35)

- Polaris 10 (also codenamed [Ellesmere](https://en.wikipedia.org/wiki/Ellesmere_Island)) found on "Radeon RX 470"- and "Radeon RX 480"-branded graphics cards
- Polaris 11 (also codenamed [Baffin](https://en.wikipedia.org/wiki/Baffin_Island)) found on "Radeon RX 460"-branded graphics cards (also Radeon RX 560**D**)
- Polaris 12 (also codenamed Lexa) found on "Radeon RX 550" and "Radeon RX 540"-branded graphics cards
- Polaris 20, which is a refreshed (14 nm LPP process) Polaris 10 with higher clocks, used for "Radeon RX 570" and "Radeon RX 580"-branded graphics cards[[36\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-36)
- Polaris 21, which is a refreshed (14 nm LPP process) Polaris 11, used for "Radeon RX 560"-branded graphics cards
- Polaris 22, found on "Radeon RX Vega M GH" and "Radeon RX Vega M GL"-branded graphics cards
- Polaris 30, which is a refreshed (12 nm LP GloFo/Samsung process) Polaris 20 with higher clocks, used for "Radeon RX 590"-branded graphics cards[[37\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-37)

#### Performance

FP64 performance of all GCN 4th generation GPUs is 1/16 of FP32 performance.

### Vega (GCN 5th generation)

See also: [AMD RX Vega series](https://en.wikipedia.org/wiki/AMD_RX_Vega_series)

AMD began releasing details of their next generation of GCN Architecture, termed the 'Next-Generation Compute Unit', in January 2017.[[34\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-anand_vega-34)[[38\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-38)[[39\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-39) The new design is expected to increase [instructions per clock](https://en.wikipedia.org/wiki/Instructions_per_clock), higher [clock speeds](https://en.wikipedia.org/wiki/Clock_rate), support for [HBM2](https://en.wikipedia.org/wiki/High_Bandwidth_Memory#HBM2), a larger memory [address space](https://en.wikipedia.org/wiki/Address_space). The discrete graphics chipsets also include "HBCC (High Bandwidth Cache Controller)", but not when integrated into APUs.[[40\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-40) Additionally, the new chips are expected to include improvements in the [Rasterisation](https://en.wikipedia.org/wiki/Rasterisation) and [Render output units](https://en.wikipedia.org/wiki/Render_output_unit). The [stream processors](https://en.wikipedia.org/wiki/Unified_shader_model) are heavily modified from the previous generations to support packed math Rapid Pack Math technology for 8-bit, 16-bit, and 32-bit numbers. With this there is a significant performance advantage when lower precision is acceptable (for example: processing two [half-precision](https://en.wikipedia.org/wiki/FP16) numbers at the same rate as a single [single precision](https://en.wikipedia.org/wiki/Single-precision_floating-point_format)number).

Nvidia introduced tile-based rasterization and binning with [Maxwell](https://en.wikipedia.org/wiki/Maxwell_(microarchitecture)),[[41\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-41) and this was a big reason for Maxwell's efficiency increase. In January, [AnandTech](https://en.wikipedia.org/wiki/AnandTech) assumed that Vega would finally catch up with Nvidia regarding energy efficiency optimizations due to the new "DSBR (Draw Stream Binning Rasterizer)" to be introduced with Vega.[[42\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-42)

It also added support for a new [shader](https://en.wikipedia.org/wiki/Shader) stage – Primitive Shaders.[[43\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-43)[[44\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-auto-44) Primitive shaders provide more flexible geometry processing and replace the [vertex](https://en.wikipedia.org/wiki/Shader#Vertex_shaders) and [geometry shaders](https://en.wikipedia.org/wiki/Shader#geometry_shaders) in a rendering pipeline. As of December 2018, the Primitive shaders can't be used because required API changes are yet to be done[[45\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-45).

#### Chips

discrete GPUs:

- Vega 10 (also codenamed [Greenland](https://en.wikipedia.org/wiki/Greenland)[[46\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-46)) found on "Radeon RX Vega 64", "Radeon RX Vega 56", "Radeon Vega Frontier Edition" and "Radeon Pro V340" graphics cards[[47\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-47)

- Vega 12 found on "Radeon Vega Pro 20" and "Radeon Vega Pro 16"-branded mobile graphics cards[[48\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-48)

- Vega 20 found on "Radeon Instinct MI50" and "Radeon Instinct MI60"-branded accelerator cards[[49\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-49) and "Radeon VII"-branded graphics cards[[50\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-50).

integrated into APUs:

- Raven Ridge[[51\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-51) came with VCN 1 which supersedes VCE and UVD and allows full fixed-function VP9 decode.

#### Performance

FP64 performance of all GCN 5th generation GPUs, except for Vega 20, is 1/16 of FP32 performance. For Vega 20 this is 1/2 of FP32 performance.[[52\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-52)

All GCN 5th generation GPUs support FP16 calculations which is 2/1 of FP32 performance.

### Navi

Navi is expected in 2019 or later and will offer "Next Generation Memory" as well as improved scalability.[[53\]](https://en.wikipedia.org/wiki/Graphics_Core_Next#cite_note-53)