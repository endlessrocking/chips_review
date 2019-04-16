![img](https://images.anandtech.com/doci/12579/Quadro_GV100-front_678x452.jpg)

Along with today’s memory capacity bump for the existing Tesla V100 cards, NVIDIA is also rolling out a new Volta-based card for the Quadro family. Aptly named the Quadro GV100, this is the successor to last year’s Quadro GP100, and marks the introduction of the Volta architecture into the Quadro family.

As a consequence of NVIDIA’s GPU lines bifurcating between graphics and compute, in the last couple of years the Quadro family has been in an odd spot where it straddles the line between the two. Previously the king of all NVIDIA cards, instead the Quadro family itself has been bifurcated a bit, between the compute GPU-derrived cards like the [Quadro GP100](https://www.anandtech.com/show/11102/nvidia-announces-quadro-gp100) and now GV100, and the more pure graphics cards like the P-series. The introduction of the Quadro GV100 in turn looks to maintain status quo here, delivering an even more powerful Quadro card with chart-topping graphics performance, but also the GV100’s GPU’s strong compute heritage.

| NVIDIA Quadro Specification Comparison |               |              |              |               |
| -------------------------------------- | ------------- | ------------ | ------------ | ------------- |
|                                        | GV100         | GP100        | P6000        | M6000         |
| **CUDA Cores**                         | 5120          | 3584         | 3840         | 3072          |
| **Tensor Cores**                       | 640           | N/A          | N/A          | N/A           |
| **Texture Units**                      | 320           | 224          | 240          | 192           |
| **ROPs**                               | 128           | 128          | 96           | 96            |
| **Boost Clock**                        | ~1450MHz      | ~1430MHz     | ~1560MHz     | ~1140MHz      |
| **Memory Clock**                       | 1.7Gbps HBM2  | 1.4Gbps HBM2 | 9Gbps GDDR5X | 6.6Gbps GDDR5 |
| **Memory Bus Width**                   | 4096-bit      | 4096-bit     | 384-bit      | 384-bit       |
| **VRAM**                               | 32GB          | 16GB         | 24GB         | 24GB          |
| **ECC**                                | Full          | Full         | Partial      | Partial       |
| **Half Precision**                     | 29.6 TFLOPs?  | 21.5 TFLOPs  | N/A          | N/A           |
| **Single Precision**                   | 14.8 TFLOPs   | 10.3 TFLOPs  | 12 TFLOPs    | 7 TFLOPs      |
| **Double Precision**                   | 7.4 TFLOPs    | 5.2 TFLOPs   | 0.38 TFLOPs  | 0.22 TFLOPs   |
| **Tensor Performance**                 | 118.5 TLFOPs  | N/A          | N/A          | N/A           |
| **TDP**                                | 250W          | 235W         | 250W         | 250W          |
| **GPU**                                | GV100         | GP100        | GP102        | GM200         |
| **Architecture**                       | Volta         | Pascal       | Pascal       | Maxwell 2     |
| **Manufacturing Process**              | TSMC 12nm FFN | TSMC 16nm    | TSMC 16nm    | TSMC 28nm     |
| **Launch Date**                        | March 2018    | March 2017   | October 2016 | March 2016    |

While NVIDIA’s pre-brief announcement doesn’t mention whether the Quadro GP100 is being discontinued, the Quadro GV100 is none the less the de facto replacement for NVIDIA’s last current-generation Big Pascal card. The official specifications for the card put it at 14.8 TFLOPs of single precision performance, which works out to a fully-enabled GV100 GPU clocked at around 1.45GHz. This is only a hair below the mezzanine Tesla V100, and ahead of the PCIe variant. And like the capacity-bumped Tesla cards, the Quadro GV100 ships with 32GB of natively ECC-protected HBM2. This finally gets an NVIDIA professional visualization card to 32GB; the GP100 was limited to 16GB, and the Quadro P6000 tops out at 24GB.

On the features front, the card also ships with NVIDIA’s tensor cores fully enabled, with performance again in the ballpark of the Tesla V100. Like the Quadro GP100’s compute features, the tensor cores aren’t expected to be applicable to all situations, but there are some professional visualization scenarios where NVIDIA expects it to be of value. More importantly though, the Quadro GV100 continues the new tradition of shipping with 2 NVLink connectors, meaning a pair of the cards can be installed in a system and enjoy the full benefits of the interface, particularly low latency data transfers, remote memory access, and memory pooling.

At a high level, the Quadro GV100 should easily be the fastest Quadro card, a distinction the GP100 didn’t always hold versus its pure graphics siblings, and that alone will undoubtedly move cards. As we’ve already seen with the Titan V in the prosumer space – NVIDIA dodging expectations by releasing the prosumer Volta card first and ProViz card second – the Titan V can be a good deal faster than any of the Pascal cards assuming that software is either designed to take advantage of the architecture, or at least meshes well with NVIDIA’s architectural upgrades. Among other things, NVIDIA is once again big into virtual reality this year, so the GV100 just became their flagship VR card, a convenient timing for anyone looking for a fast card to drive the just-launched [HTC Vive Pro](https://www.anandtech.com/show/12548/htc-vive-pro-pre-orders-start-for-799).

[![img](https://images.anandtech.com/doci/12579/RTX_Diagram_1522171266_575px.jpg)](https://images.anandtech.com/doci/12579/RTX_Diagram_1522171266.jpg)

However the GV100’s bigger calling within NVIDIA’s ecosystem is that it’s now the only Quadro card using the Volta architecture, meaning it’s the only card to support hardware raytracing acceleration, vis a vie [NVIDIA’s RTX technology](https://www.anandtech.com/show/12546/nvidia-unveils-rtx-technology-real-time-ray-tracing-acceleration-for-volta-gpus-and-later). Announced last week at the 2018 Game Developers Conference, RTX is NVIDIA’s somewhat ill-defined hardware acceleration backend for real-time raytracing. And while the GDC announcement was focused on the technology’s use in games and game development, at GTC the company is focusing on the professional uses of it, including yet more game development, but also professional media creation. Not that NVIDIA expects movie producers to sudden do final production in real-time on GPUs, but as with the game asset creation scenario, the idea is to significantly improve realism during pre-production by giving artists a better idea of what a final scene would look like.

Along with Microsoft’s new DirectX Raytracing API, the RTX hardware will also be available within NVIDIA’s OptiX ray tracing engine – which is almost certainly a better fit for ProViz users – while NVIDIA is also saying that Vulkan support is on tap for the future. And like the game development scenario, NVIDIA will also be looking to leverage their tensor cores here as well in order to use them for AI denoising. Which, given the still limited raytracing performance of current hardware, is increasingly being setup as the critical component for making real-time ray tracing viable in 2018.

[![img](https://images.anandtech.com/doci/12579/Quadro_GV100-3qtr_575px.jpg)](https://images.anandtech.com/doci/12579/Quadro_GV100-3qtr.jpg)

Otherwise, the Quadro GV100 looks to be a fairly standard Quadro card. TDP has gone up ever slightly from the Quadro GP100 – from 235W to 250W – so while it should generally be drop-in replaceable, it’s not strictly identical. Nor are the display outputs identical; the Quadro GV100 has dropped the GP100’s sole DVI port, leaving it with a pure 4x DisplayPort 1.4 setup. The card also features the standard Quadro Sync and Stereo connectors for synchronized refresh and quad-buffered stereo respectively.

Wrapping things up, the Quadro GV100 is shipping immediately from NVIDIA, and OEMs will begin including it in their systems in June. Official pricing has not been announced, but like the GP100 before it, I would expect this card to run for north of $5,000. Official pricing has also been announced for the card; NVIDIA's fastest Quadro will go for a cool $9,000.