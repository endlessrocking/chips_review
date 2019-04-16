







The launch of the Kepler family of GPUs in March of 2012 was something of a departure from the normal for NVIDIA. Over the years NVIDIA has come to be known among other things for their big and powerful GPUs. NVIDIA had always produced a large 500mm2+ GPU to serve both as a flagship GPU for their consumer lines and the fundamental GPU for their Quadro and Tesla lines, and have always launched with that big GPU first.

So when the Kepler family launched first with the GK104 and GK107 GPUs – powering the GeForce GTX 680 and GeForce GT 640M respectively – it was unusual to say the least. In place of “Big Kepler”, we got a lean GPU that was built around graphics first and foremost, focusing on efficiency and in the process forgoing a lot of the compute performance NVIDIA had come to be known for in the past generation. The end result of this efficiency paid off nicely for NVIDIA, with GTX 680 handily surpassing AMD’s Radeon HD 7970 at the time of its launch in both raw performance and in power efficiency.

Big Kepler was not forgotten however. First introduced at GTC 2012, GK110 as it would come to be known would be NVIDIA’s traditional big, powerful GPU for the Kepler family. Building upon NVIDIA’s work with GK104 while at the same time following in the footsteps of NVIDIA’s compute-heavy GF100 GPU, GK110 would be NVIDIA’s *magnum opus* for the Kepler family.

Taped out later than the rest of the Kepler family, GK110 has taken a slightly different route to get to market. Rather than launching in a consumer product first, GK110 was first launched as the heart of NVIDIA’s Tesla K20 family of GPUs, the new cornerstone of NVIDIA’s rapidly growing GPU compute business.

*![img](https://images.anandtech.com/reviews/video/NVIDIA/Titan/DSC_8655sm.jpg)Oak Ridge National Laboratory's Titan Supercomputer*

Or perhaps as it’s better known, the GPU at the heart of the world’s fastest supercomputer, [Oak Ridge National Laboratory’s *Titan* supercomputer](http://www.anandtech.com/show/6421/inside-the-titan-supercomputer-299k-amd-x86-cores-and-186k-nvidia-gpu-cores/).

The Titan supercomputer was a major win for NVIDIA, and likely the breakthrough they’ve been looking for. A fledging business merely two generations prior, NVIDIA and their Tesla family have quickly shot up in prestige and size, much to the delight of NVIDIA. Their GPU computing business is still relatively small – consumer GPUs dwarf it and will continue to do so for the foreseeable future – but it’s now a proven business for NVIDIA. More to the point however, winning contracts like Titan are a major source of press and goodwill for the company, and goodwill the company intends to capitalize on.

With the launch of the Titan supercomputer and the Tesla K20 family now behind them, NVIDIA is now ready to focus their attention back on the consumer market. Ready to bring their big and powerful GK110 GPU to the consumer market, in typical NVIDIA fashion they intend to make a spectacle of it. In NVIDIA’s mind there’s only one name suitable for the first consumer card born of the same GPU as their greatest computing project: GeForce GTX Titan.

[![img](https://images.anandtech.com/doci/6760/TiltedTitan_575px.jpg)](https://images.anandtech.com/doci/6760/TiltedTitan.jpg)

**GeForce GTX Titan: By The Numbers**

At the time of the GK110 launch at GTC, we didn’t know if and when GK110 would ever make it down to consumer hands. From a practical perspective GTX 680 was still clearly in the lead over AMD’s Radeon HD 7970. Meanwhile the Titan supercomputer was a major contract for NVIDIA, and something they needed to prioritize. 18,688 551mm2 GPUs for a single customer is a very large order, and at the same time orders for Tesla K20 cards were continuing to pour in each and every day after GTC. In the end, yes, GK110 would come to the consumer market. But not until months later, after NVIDIA had the chance to start filling Tesla orders. And today is that day.

Much like the launch of the GTX 690 before it, NVIDIA intends to stretch this launch out a bit to maximize the amount of press they get. Today we can tell you all about Titan – its specs, its construction, and its features – but not about its measured performance. For that you will have to come back on Thursday, when we can give you our benchmarks and performance analysis.

|                           | **GTX Titan**  | **GTX 690**    | **GTX 680**    | **GTX 580**    |
| ------------------------- | -------------- | -------------- | -------------- | -------------- |
| **Stream Processors**     | 2688           | 2 x 1536       | 1536           | 512            |
| **Texture Units**         | 224            | 2 x 128        | 128            | 64             |
| **ROPs**                  | 48             | 2 x 32         | 32             | 48             |
| **Core Clock**            | 837MHz         | 915MHz         | 1006MHz        | 772MHz         |
| **Shader Clock**          | N/A            | N/A            | N/A            | 1544MHz        |
| **Boost Clock**           | 876Mhz         | 1019MHz        | 1058MHz        | N/A            |
| **Memory Clock**          | 6.008GHz GDDR5 | 6.008GHz GDDR5 | 6.008GHz GDDR5 | 4.008GHz GDDR5 |
| **Memory Bus Width**      | 384-bit        | 2 x 256-bit    | 256-bit        | 384-bit        |
| **VRAM**                  | 6              | 2 x 2GB        | 2GB            | 1.5GB          |
| **FP64**                  | 1/3 FP32       | 1/24 FP32      | 1/24 FP32      | 1/8 FP32       |
| **TDP**                   | 250W           | 300W           | 195W           | 244W           |
| **Transistor Count**      | 7.1B           | 2 x 3.5B       | 3.5B           | 3B             |
| **Manufacturing Process** | TSMC 28nm      | TSMC 28nm      | TSMC 28nm      | TSMC 40nm      |
| **Launch Price**          | $999           | $999           | $499           | $499           |

Diving right into things then, at the heart of the GeForce GTX Titan we have the GK110 GPU. By virtue of this being the 2nd product to be launched based off the GK110 GPU, there are no great mysteries here about GK110’s capabilities. [We’ve covered GK110 in depth from a compute perspective,](http://www.anandtech.com/show/6446/nvidia-launches-tesla-k20-k20x-gk110-arrives-at-last/3) so many of these numbers should be familiar with our long-time readers.

GK110 is composed of 15 of NVIDIA’s SMXes, each of which in turn is composed of a number of functional units. Every GK110 packs 192 FP32 CUDA cores, 64 FP64 CUDA cores, 64KB of L1 cache, 65K 32bit registers, and 16 texture units. These SMXes are in turn paired with GK110’s 6 ROP partitions, each one composed of 8 ROPs, 256KB of L2 cache, and connected to a 64bit memory controller. Altogether GK110 is a massive chip, coming in at 7.1 billion transistors, occupying 551mm2 on TSMC’s 28nm process.

For Titan NVIDIA will be using a partially disabled GK110 GPU. Titan will have all 6 ROP partitions and the full 384bit memory bus enabled, but only 14 of the 15 SMXes will be enabled. In terms of functional units this gives Titan a final count of 2688 FP 32 CUDA cores, 896 FP64 CUDA cores, 224 texture units, and 48 ROPs. This makes Titan virtually identical to NVIDIA’s most powerful Tesla, K20X, which ships with the same configuration. NVIDIA does not currently ship any products with all 15 SMXes enabled, and though NVIDIA will never really explain why this is – yield, power, or otherwise – if nothing else it leaves them an obvious outlet for growth if they need to further improve Titan’s performance, by enabling that 15th SMX.

[![img](https://images.anandtech.com/doci/6760/GK110_Block_Diagram_FINAL2_575px.png)](https://images.anandtech.com/doci/6760/GK110_Block_Diagram_FINAL2.png)

Of course functional units are only half the story, so let’s talk about clockspeeds. As a rule of thumb bigger GPUs don’t clock as high as smaller GPUs, and Titan will be adhering to this rule. Whereas GTX 680 shipped with a base clock of 1006MHz, Titan ships at a more modest 837MHz, making up for any clockspeed disadvantage with the brute force behind having so many functional units. Like GTX 680 (and unlike Tesla), boost clocks are once more present, with Titan’s official boost clock coming in at 876MHz, while the maximum boost clock can potentially be much higher.

On the memory side of things, Titan ships with a full 6GB of GDDR5. As a luxury card NVIDIA went for broke here and simply equipped the card with as much RAM as is technically possible, rather than stopping at 3GB. You wouldn’t know that from looking at their memory clocks though; even with 24 GDDR5 memory chips, NVIDIA is shipping Titan at the same 6GHz effective memory clock as the rest of the high-end GeForce 600 series cards, giving the card 288GB/sec of memory bandwidth.

To put all of this in perspective, on paper (and at base clocks), GTX 680 can offer just shy of 3.1 TFLOPS of FP32 performance, 128GTexels/second texturing throughput, and 32GPixels/second rendering throughput, driven by 192GB/sec of memory bandwidth. Titan on the other hand can offer 4.5 TFLOPS of FP32 performance, 187GTexels/second texturing throughput, 40GPixels/second rendering throughput, and is driven by a 288GB/sec memory bus. This gives Titan 46% more shading/compute and texturing performance, 25% more pixel throughput, and a full 50% more memory bandwidth than GTX 680. Simply put, thanks to GK110 Titan is a far more powerful GPU than what GK104 could accomplish.

Of course with great power comes great power bills, to which Titan is no exception. In GTX 680’s drive for efficiency NVIDIA got GTX 680 down to a TDP of 195W with a power target of 170W, a remarkable position given both the competition and NVIDIA’s prior generation products. Titan on the other hand will have a flat 250W power target – in line with prior generation big NVIDIA GPUs – staking out its own spot on the price/power hierarchy, some 28%-47% higher in power consumption than GTX 680. These values are almost identical to the upper and lower theoretical performance gaps between Titan and GTX 680, so performance is growing in-line with power consumption, but only just. From a practical perspective Titan achieves a similar level of efficiency as GTX 680, but as a full compute chip it’s unquestionably not as lean. There’s a lot of compute baggage present that GK104 didn’t have to deal with.



**Who’s Titan For, Anyhow?**

Having established performance expectations, let’s talk about where Titan fits into NVIDIA’s product stack. First and foremost, though Titan is most certainly geared in part as a gaming video card (and that’s largely how we’ll be looking at it), that’s not the only role it serves. Titan is also going to be NVIDIA’s entry-level compute card. We’ll dive more into why that is in a bit in our feature breakdown, but the biggest factor is that for the first time on any consumer-level NVIDIA card, **double precision (FP64) performance is uncapped**. That means 1/3 FP32 performance, or roughly 1.3TFLOPS theoretical FP64 performance. NVIDIA has taken other liberties to keep from this being treated as a cheap Tesla K20, but for lighter workloads it should fit the bill.

As compared to the server and high-end workstation market that Tesla carves out, NVIDIA will be targeting the compute side of Titan towards researchers, engineers, developers, and others who need access to (relatively) cheap FP64 performance, and don’t need the scalability or reliability that Tesla brings. To that end Titan essentially stands alone in NVIDIA’s product stack; the next thing next to a FP64-constrained consumer card is the much more expensive Tesla K20.

![img](https://images.anandtech.com/doci/6760/GeForce-GTX-Titan_Press_Final-4.jpg)

Far more complex will be the gaming situation. Titan will not be pushing anything down in NVIDIA’s product stack, rather NVIDIA’s product stack will be growing up to accompany Titan. Like the GTX 690, NVIDIA is going to position Titan as a premium/luxury product, releasing it at the same $999 price point. GTX 690 itself will continue to exist at the same $999 price point, meanwhile GTX 680 will continue at its current price point of roughly $450.

Continuing the GTX 690 analogies, Titan will not only be sharing in GTX 690’s price point, but also in its design principles and distribution. This means Titan is a well-built card with its housing composed primarily of metals, with the same kind of luxury finish as the GTX 690. On the distribution side of things Asus and EVGA are once again NVIDIA’s exclusive partners for North America, and they will essentially be distributing  reference Titan cards. In time we will see some specialized variation, with water-cooling in particular being an obvious route for EVGA to go. Factory overclocks are also on the table.

With the above in mind, it goes without saying that while GTX 690 had some historical precedence in its price, the same cannot be said for Titan. The price of NVIDIA’s top-tier single-GPU video cards hovered around $500 for the GeForce 400/500 series, and while they attempted to launch at $650 for the GTX 280, the launch of the Radeon HD 4870 quickly brought that price down to earth. As such this will be the most expensive single-GPU product out of NVIDIA yet.

[![img](https://images.anandtech.com/doci/6760/GeForceTrio_575px.jpg)](https://images.anandtech.com/doci/6760/GeForceTrio.jpg)
*Top To Bottom: GTX 680, GTX Titan, GTX 690*

Ultimately NVIDIA is not even going to try to compete on a price-performance basis with Titan. There are a number of potential reasons for this – ranging from the competitive landscape to yields to needs for GK110 GPUs elsewhere within NVIDIA – and all of those reasons are probably true to some extent. Regardless, NVIDIA believes that like the GTX 690 they can sell Titan as a luxury product, and hence $999. The GTX 680 and below will compose NVIDIA’s more traditional price-performance competitive fare.

As to be expected from such a price, NVIDIA’s marketing department will be handling Titan in a similar fashion as they did GTX 690. This not only includes reiterating the fact that Titan is intended to be a luxury product, but also focusing on markets where luxury products are accepted, and where Titan in particular makes sense.

Perhaps not surprisingly, with $999 video cards the makeup of consumers shifts away from both traditional big-box OEMs and DIY builders, and towards boutique builders. Boutique builders are essentially already in the business of providing luxury computers, offering an outlet for luxury buyers who need not spend their time building their own computer, and want something of higher quality than what the typical OEM provides. As such while Titan will be sold on the open market just as like any other card, NVIDIA tells us that they expect a lot of those buyers are going to be the boutiques.

For Titan in particular, NVIDIA is going to be focusing on two boutique computer concepts, reflecting the blower design of Titan as opposed to the front/back exhausting design of the GTX 690. The first concept will be SFF PCs, where blowers are a necessity due to a lack of space (and often, a lack of heavy sound dampening), and where such cards can draw fresh air in from outside the chassis.

[![img](https://images.anandtech.com/doci/6760/GeForce-GTX-Titan_Press_Final-17_575px.jpg)](https://images.anandtech.com/doci/6760/GeForce-GTX-Titan_Press_Final-17.jpg)

On the other end of the spectrum will be the ultra-enthusiast market where one Titan isn’t enough, and even two may come up short. Again thanks to the fact that it’s a blower, Titan can easily be fit in an ATX motherboard for tri-SLI operation, which NVIDIA envisions not just as the ultimate gaming computer, but the ultimate NV/3D Surround computer in particular. Multi-monitor gaming with graphically intensive games can quickly nullify the performance of even a single Titan card, so tri-SLI is NVIDIA’s solution to driving three monitors as well as one Titan can drive one monitor. At the same time however, NVIDIA intends to showcase that a tri-SLI system doesn’t need to be loud, despite the cramped conditions and despite the 750W+ that 3 Titans will pull, thanks to the high quality construction of the cards. Tri-SLI has been possible for a number of years, but NVIDIA believes with Titan in particular they have a solid grip on the heat and noise concerns it typically comes with.

To that end, as part of the Titan launch NVIDIA has shipped out a number of boutique systems in either a SFF or tri-SLI full tower configuration to reviewers, in order to show off their usage concepts in completed and well-constructed systems. [Anand received a SFF Tiki](http://www.anandtech.com/show/6763/) from Falcon Northwest, while I have received a tri-SLI equipped Genesis from Origin PC. Like Titan itself we can’t talk about the performance of these systems, but we’ll be able to go into greater detail on Thursday when the complete NDA lifts. In the meantime we’ve been able to post a few impressions, which we’ve put up on their respective articles.

[![img](https://images.anandtech.com/doci/6760/originpc-full-titan-front-angle_575px.jpg)](https://images.anandtech.com/doci/6760/originpc-full-titan-front-angle.jpg)

Moving on, with a $999 launch price NVIDIA’s competition will be rather limited. The GTX 690 is essentially a companion product; NVIDIA’s customers can either get the most powerful single-GPU card NVIDIA offers in a blower design, or an alternative design composed of two lesser GPUs in SLI, in a front and rear exhausting design. The GTX 690 will be the faster card, but at a higher TDP and with the general drawbacks of SLI. On the other hand Titan will be the more consistent card, the lower TDP card, the easier to cool card, but also the slower card. Meanwhile though it’s not a singular product, the GTX 680 SLI will also be another option, offering higher performance, higher TDP, more noise, and a cheaper price tag of around $900.

As for AMD, with their fastest single-GPU video card being the 7970 GHz Edition, offering performance closer to the GTX 680 than Titan, Titan essentially sits in a class of its own on the single-GPU front. AMD’s competition for Titan will be the 7970GE in CrossFire, and then the officially unofficial 7990 family, composed of the air-cooled PowerColor 7990, and the closed loop water-cooled Asus Ares II. But with NVIDIA keeping GTX 690 around, these are probably closer competitors to the multi-GPU 690 than they are the single-GPU Titan.

Finally, let’s talk launch availability. By scheduling the launch of Titan during the Chinese New Year, NVIDIA has essentially guaranteed this is a delayed availability product. Widespread availability is expected on the 25th, though cards may start popping up a couple of days earlier. NVIDIA hasn’t gone into depth for launch quantities, but they did specifically shoot down the 10,000 card rumor; this won’t be a limited run product and we don’t have any reason at this time to believe this will be much different from the GTX 690’s launch (tight at first, but available and increasingly plentiful).

| February 2013 GPU Pricing Comparison                         |       |                                                              |
| ------------------------------------------------------------ | ----- | ------------------------------------------------------------ |
| AMD                                                          | Price | NVIDIA                                                       |
|                                                              | $1000 | GeForce GTX Titan/690                                        |
| [(Unofficial) Radeon HD 7990](http://detonator.dynamitedata.com/cgi-bin/redirect.pl?user=u00000626&url=http%3a%2f%2fwww.newegg.com%2fProduct%2fProduct.aspx%3fItem%3dN82E16814131483%26amp%3bTpk%3d7990) | $900  |                                                              |
| [Radeon HD 7970 GHz Edition](http://detonator.dynamitedata.com/cgi-bin/redirect.pl?user=u00000626&url=http%3a%2f%2fwww.newegg.com%2fProduct%2fProduct.aspx%3fItem%3dN82E16814161431) | $450  | [GeForce GTX 680](http://detonator.dynamitedata.com/cgi-bin/redirect.pl?user=u00000626&url=http%3a%2f%2fwww.newegg.com%2fProduct%2fProduct.aspx%3fItem%3dN82E16814500238) |
| [Radeon HD 7970](http://detonator.dynamitedata.com/cgi-bin/redirect.pl?user=u00000626&url=http%3a%2f%2fwww.newegg.com%2fProduct%2fProduct.aspx%3fItem%3dN82E16814103201) | $390  |                                                              |
|                                                              | $350  | [GeForce GTX 670](http://detonator.dynamitedata.com/cgi-bin/redirect.pl?user=u00000626&url=http%3a%2f%2fwww.newegg.com%2fProduct%2fProduct.aspx%3fItem%3dN82E16814130782) |
| [Radeon HD 7950 ](http://detonator.dynamitedata.com/cgi-bin/redirect.pl?user=u00000626&url=http%3a%2f%2fwww.newegg.com%2fProduct%2fProduct.aspx%3fItem%3dN82E16814150590) | $300  |                                                              |





**Meet The GeForce GTX Titan**

As we briefly mentioned at the beginning of this article, the GeForce GTX Titan takes a large number of cues from the GTX 690. Chief among these is that it’s a luxury card, and as such is built to similar standards as the GTX 690. Consequently, like the GTX 690, Titan is essentially in a league of its own when it comes to build quality.

Much like the GTX 690 was to the GTX 590, Titan is an evolution of the cooler found on the GTX 580. This means we’re looking at a card roughly 10.5” in length using a double-wide cooler. The basis of Titan’s cooler is a radial fan (blower) sitting towards the back of the card, with the GPU, RAM, and most of the power regulation circuitry in front of the fan. As a result the bulk of the hot air generated by Titan is blown forwards and out of the card. However it’s worth noting that unlike most other blowers technically the back side isn’t sealed, and while there is relatively little circuitry behind the fan, it would be incorrect to state that the card is fully exhausting. With that said, leaving the back side of the card open seems to be more about noise and aesthetics than it does heat management.



[![img](https://images.anandtech.com/doci/6760/GeForceGTX_Titan_3Qtr2a_575px.jpg)](https://images.anandtech.com/doci/6760/GeForceGTX_Titan_3Qtr2a.jpg)

Like the GTX 580 but unlike the GTX 680, heat transfer is provided by a nickel tipped aluminum heatsink attached to the GPU via a vapor chamber. We typically only see vapor chambers on premium cards due to their greater costs, but also when space is at a premium. Meanwhile NVIDIA seems to be pushing the limits of heatsink size here, with the fins on Titan’s heatsink actually running beyond the base of the vapor chamber. Meanwhile providing the thermal interface between the GPU itself and the vapor chamber is a silk screened application of a high-end Shin-Etsu thermal compound; NVIDIA claims this compound offers over twice the performance of GTX 680’s grease, although of all of NVIDIA’s claims this is the least possible to validate.

Moving on, catching what the vapor chamber doesn’t cover is an aluminum baseplate that runs along the card, not only providing structural rigidity but also providing cooling for the VRMs and for the RAM on the front side of the card. Baseplates aren’t anything new for NVIDIA, but again this is something that we don’t see a lot of except on their more premium cards.

[![img](https://images.anandtech.com/doci/6760/GeForceGTX_Titan_Front3a_575px.jpg)](https://images.anandtech.com/doci/6760/GeForceGTX_Titan_Front3a.jpg)

Capping off Titan we have its most visible luxury aspects. Like the GTX 690 before it, NVIDIA has replaced virtually every bit of plastic with metal for aesthetic/perceptual purposes. This time the entire shroud and fan housing is composed of casted aluminum, which NVIDIA tells us is easier to cast than the previous mix of aluminum and magnesium that the GTX 690 used. Meanwhile the polycarbonate window makes its return allowing you to see Titan’s heatsink solely for the sake of it.

As for the back side of the card, keeping with most of NVIDIA’s cards Titan runs with a bare back. The GDDR5 RAM chips don’t require any kind of additional cooling, and a metal backplate while making for a great feeling card, occupies precious space that would otherwise impede cooling in tight spaces.

[![img](https://images.anandtech.com/doci/6760/TitanBack_575px.jpg)](https://images.anandtech.com/doci/6760/TitanBack.jpg)

Moving on, let’s talk about the electrical details of Titan’s design. Whereas GTX 680 was a 4+2 power phase design – 4 power phases for the GPU and 2 for the VRAM – Titan improves on this by moving to a 6+2 power phase design. I suspect the most hardcore of overclockers will be disappointed with Titan only having 6 phases for the GPU, but for most overclocking purposes this would seem to be enough.

[![img](https://images.anandtech.com/doci/6760/GeForceGTX_Titan_Front1_575px.jpg)](https://images.anandtech.com/doci/6760/GeForceGTX_Titan_Front1.jpg)

Meanwhile for RAM it should come as no particular surprise that NVIDIA is once more using 6GHz RAM here. Specifically, NVIDIA is using 24 6GHz Samsung 2Gb modules here, totaling up to the 6GB of RAM we see on the card. 12 modules are on front with the other 12 modules on the rear. The overclocking headroom on 6GHz RAM seems to vary from chip to chip, so while Titan should have some memory overclocking headroom it’s hard to say just what the combination of luck and the wider 384bit memory bus will do.

Providing power for all of this is a pair of PCIe power sockets, a 6pin and an 8pin, for a combined total of 300W of capacity. With Titan only having a TDP of 250W in the first place, this leaves quite a bit of headroom before ever needing to run outside of the PCIe specification.

At the other end of Titan we can see that NVIDIA has once again gone back to their “standard” port configuration for the GeForce 600 series: two DL-DVI ports, one HDMI port, and one full-size DisplayPort. Like the rest of the 600 family, Titan can drive up to four displays so this configuration is a good match. Though I would still like to see two mini-DisplayPorts in the place of the full size DisplayPort, in order to tap the greater functionality DisplayPort offers though its port conversion mechanisms.



**Titan For Compute**

Titan, as we briefly mentioned before, is not just a consumer graphics card. It is also a compute card and will essentially serve as NVIDIA’s entry-level compute product for both the consumer and pro-sumer markets.

The key enabler for this is that Titan, unlike any consumer GeForce card before it, will feature full FP64 performance, allowing GK110’s FP64 potency to shine through. Previous NVIDIA cards either had very few FP64 CUDA cores (GTX 680) or artificial FP64 performance restrictions (GTX 580), in order to maintain the market segmentation between cheap GeForce cards and more expensive Quadro and Tesla cards. NVIDIA will still be maintaining this segmentation, but in new ways.

| NVIDIA GPU Comparison |             |             |              |              |
| --------------------- | ----------- | ----------- | ------------ | ------------ |
|                       | Fermi GF100 | Fermi GF104 | Kepler GK104 | Kepler GK110 |
| Compute Capability    | 2.0         | 2.1         | 3.0          | 3.5          |
| Threads/Warp          | 32          | 32          | 32           | 32           |
| Max Warps/SM(X)       | 48          | 48          | 64           | 64           |
| Max Threads/SM(X)     | 1536        | 1536        | 2048         | 2048         |
| Register File         | 32,768      | 32,768      | 65,536       | 65,536       |
| Max Registers/Thread  | 63          | 63          | 63           | 255          |
| Shared Mem Config     | 16K 48K     | 16K 48K     | 16K 32K 48K  | 16K 32K 48K  |
| Hyper-Q               | No          | No          | No           | Yes          |
| Dynamic Parallelism   | No          | No          | No           | Yes          |

We’ve covered GK110’s compute features in-depth in [our look at Tesla K20](http://www.anandtech.com/show/6446/nvidia-launches-tesla-k20-k20x-gk110-arrives-at-last) so we won’t go into great detail here, but as a reminder, along with beefing up their functional unit counts relative to GF100, GK110 has several feature improvements to further improve compute efficiency and the resulting performance. Relative to the GK104 based GTX 680, Titan brings with it a much greater number of registers per thread (255), not to mention a number of new instructions such as the shuffle instructions to allow intra-warp data sharing. But most of all, Titan brings with it NVIDIA’s Kepler marquee compute features: HyperQ and Dynamic Parallelism, which allows for a greater number of hardware work queues and for kernels to dispatch other kernels respectively.

[![img](https://images.anandtech.com/doci/6760/K20Efficiency_575px.png)](https://images.anandtech.com/doci/6760/K20Efficiency.png)

With that said, there is a catch. NVIDIA has stripped GK110 of some of its reliability and scalability features in order to maintain the Tesla/GeForce market segmentation, which means Titan for compute is left for small-scale workloads that don’t require Tesla’s greater reliability. ECC memory protection is of course gone, but also gone is HyperQ’s MPI functionality, and GPU Direct’s RDMA functionality (DMA between the GPU and 3rd party PCIe devices). Other than ECC these are much more market-specific features, and as such while Titan is effectively locked out of highly distributed scenarios, this should be fine for smaller workloads.

There is one other quirk to Titan’s FP64 implementation however, and that is that it needs to be enabled (or rather, uncapped). By default Titan is actually restricted to 1/24 performance, like the GTX 680 before it. Doing so allows NVIDIA to keep clockspeeds higher and power consumption lower, knowing the apparently power-hungry FP64 CUDA cores can’t run at full load on top of all of the other functional units that can be active at the same time. Consequently NVIDIA makes FP64 an enable/disable option in their control panel, controlling whether FP64 is operating at full speed (1/3 FP32), or reduced speed (1/24 FP32).

![img](https://images.anandtech.com/doci/6760/NVCP.jpg)

The penalty for enabling full speed FP64 mode is that NVIDIA has to reduce clockspeeds to keep everything within spec. For our sample card this manifests itself as GPU Boost being disabled, forcing our card to run at 837MHz (or lower) at all times. And while we haven't seen it first-hand, NVIDIA tells us that in particularly TDP constrained situations Titan can drop below the base clock to as low as 725MHz. This is why NVIDIA’s official compute performance figures are 4.5 TFLOPS for FP32, but only 1.3 TFLOPS for FP64. The former is calculated around the base clock speed, while the latter is calculated around the worst case clockspeed of 725MHz. The actual execution rate is still 1/3.

Unfortunately there’s not much else we can say about compute performance at this time, as to go much farther than this requires being able to reference specific performance figures. So we’ll follow this up on Thursday with those figures and a performance analysis.



**GPU Boost 2.0: Temperature Based Boosting**

With the Kepler family NVIDIA introduced their GPU Boost functionality. Present on the desktop GTX 660 and above, boost allows NVIDIA’s GPUs to turbo up to frequencies above their base clock so long as there is sufficient power headroom to operate at those higher clockspeeds and the voltages they require. Boost, like turbo and other implementations, is essentially a form of performance min-maxing, allowing GPUs to offer higher clockspeeds for lighter workloads while still staying within their absolute TDP limits.

With the first iteration of GPU Boost, GPU Boost was based almost entirely around power considerations. With the exception of an automatic 1 bin (13MHz) step down in high temperatures to compensate for increased power consumption, whether GPU Boost could boost and by how much depended on how much power headroom was available. So long as there was headroom, GPU Boost could boost up to its maximum boost bin and voltage.



[![img](https://images.anandtech.com/doci/6760/GPUBoost_575px.jpg)](https://images.anandtech.com/doci/6760/GPUBoost.jpg)

For Titan, GPU Boost has undergone a small but important change that has significant ramifications to how GPU Boost works, and how much it boosts by. And that change is that with GPU Boost 2, NVIDIA has essentially moved on from a power-based boost system to a temperature-based boost system. Or perhaps more precisely, a system that is predominantly temperature based but is also capable of taking power into account.



[![img](https://images.anandtech.com/doci/6760/Boost2_575px.jpg)](https://images.anandtech.com/doci/6760/Boost2.jpg)

When it came to GPU Boost 1, its greatest weakness as explained by NVIDIA is that it essentially made conservative assumptions about temperatures and the interplay between high temperatures and high voltages in order keep from seriously impacting silicon longevity. The end result being that NVIDIA was picking boost bin voltages based on the worst case temperatures, which meant those conservative assumptions about temperatures translated into conservative voltages.

So how does a temperature based system fix this? By better mapping the relationship between voltage, temperature, and reliability, NVIDIA can allow for higher voltages – and hence higher clockspeeds – by being able to finely control which boost bin is hit based on temperature. As temperatures start ramping up, NVIDIA can ramp down the boost bins until an equilibrium is reached.

Of course total power consumption is still a technical concern here, though much less so. Technically NVIDIA is watching both the temperature and the power consumption and clamping down when either is hit. But since GPU Boost 2 does away with the concept of separate power targets – sticking solely with the TDP instead – in the design of Titan there’s quite a bit more room for boosting thanks to the fact that it can keep on boosting right up until the point it hits the 250W TDP limit. Our Titan sample can boost its clockspeed by up to 19% (837MHz to 992MHz), whereas our GTX 680 sample could only boost by 10% (1006MHz to 1110MHz).

[![img](https://images.anandtech.com/doci/6760/B2V_575px.jpg)](https://images.anandtech.com/doci/6760/B2V.jpg)

Ultimately however whether GPU Boost 2 is power sensitive is actually a control panel setting, meaning that power sensitivity can be disabled. By default GPU Boost will monitor both temperature and power, but 3rdparty overclocking utilities such as EVGA Precision X can prioritize temperature over power, at which point GPU Boost 2 can actually ignore TDP to a certain extent to focus on power. So if nothing else there’s quite a bit more flexibility with GPU Boost 2 than there was with GPU Boost 1.

Unfortunately because GPU Boost 2 is only implemented in Titan it’s hard to evaluate just how much “better” this is in any quantities sense. We will be able to present specific Titan numbers on Thursday, but other than saying that our Titan maxed out at 992MHz at its highest boost bin of 1.162v, we can’t directly compare it to how the GTX 680 handled things.



**GPU Boost 2.0: Overclocking & Overclocking Your Monitor**

The first half of the GPU Boost 2 story is of course the fact that with 2.0 NVIDIA is switching from power based controls to temperature based controls. However there is also a second story here, and that is the impact to overclocking.

With the GTX 680, overclocking capabilities were limited, particularly in comparison to the GeForce 500 series. The GTX 680 could have its power target raised (guaranteed “overclocking”), and further overclocking could be achieved by using clock offsets. But perhaps most importantly, voltage control was forbidden, with NVIDIA going so far as to nix EVGA and MSI’s voltage adjustable products after a short time on the market.

There are a number of reasons for this, and hopefully one day soon we’ll be able to get into NVIDIA’s Project Greenlight video card approval process in significant detail so that we can better explain this, but the primary concern was that without strict voltage limits some of the more excessive users may blow out their cards with voltages set too high. And while the responsibility for this ultimately falls to the user, and in some cases the manufacturer of their card (depending on the warranty), it makes NVIDIA look bad regardless. The end result being that voltage control on the GTX 680 (and lower cards) was disabled for everyone, regardless of what a card was capable of.

With Titan this has finally changed, at least to some degree. In short, NVIDIA is bringing back overvoltage control, albeit in a more limited fashion.

[![img](https://images.anandtech.com/doci/6760/Overvolt_575px.jpg)](https://images.anandtech.com/doci/6760/Overvolt.jpg)

For Titan cards, partners will have the final say in whether they wish to allow overvolting or not. If they choose to allow it, they get to set a maximum voltage (Vmax) figure in their VBIOS. The user in turn is allowed to increase their voltage beyond NVIDIA’s default reliability voltage limit (Vrel) up to Vmax. As part of the process however users have to acknowledge that increasing their voltage beyond Vrel puts their card at risk and may reduce the lifetime of the card. Only once that’s acknowledged will users be able to increase their voltages beyond Vrel.

![img](https://images.anandtech.com/doci/6760/Voltage.png)

With that in mind, beyond overvolting overclocking has also changed in some subtler ways. Memory and core offsets are still in place, but with the switch from power based monitoring to temperature based monitoring, the power target slider has been augmented with a separate temperature target slider.

[![img](https://images.anandtech.com/doci/6760/Untitled_575px.png)](https://images.anandtech.com/doci/6760/Untitled.png)

The power target slider is still responsible for controlling the TDP as before, but with the ability to prioritize temperatures over power consumption it appears to be somewhat redundant (or at least unnecessary) for more significant overclocking. That leaves us with the temperature slider, which is really a control for two functions.

First and foremost of course is that the temperature slider controls what the target temperature is for Titan. By default for Titan this is 80C, and it may be turned all the way up to 95C. The higher the temperature setting the more frequently Titan can reach its highest boost bins, in essence making this a weaker form of overclocking just like the power target adjustment was on GTX 680.

[![img](https://images.anandtech.com/doci/6760/FanCurve1_575px.jpg)](https://images.anandtech.com/doci/6760/FanCurve1.jpg)

The second function controlled by the temperature slider is the fan curve, which for all practical purposes follows the temperature slider. With modern video cards ramping up their fan speeds rather quickly once cards get into the 80C range, merely increasing the power target alone wouldn’t be particularly desirable in most cases due to the extra noise it generates, so NVIDIA tied in the fan curve to the temperature slider. By doing so it ensures that fan speeds stay relatively low until they start exceeding the temperature target. This seems a bit counterintuitive at first, but when put in perspective of the goal – higher temperatures without an increase in fan speed – this starts to make sense.

[![img](https://images.anandtech.com/doci/6760/FanCurve2_575px.jpg)](https://images.anandtech.com/doci/6760/FanCurve2.jpg)

Finally, in what can only be described as a love letter to the boys over at [120hz.net](http://120hz.net/), NVIDIA is also introducing a simplified *monitor* overclocking option, which can be used to increase the refresh rate sent to a monitor in order to coerce it into operating at that higher refresh rate. Notably, this isn’t anything that couldn’t be done before with some careful manipulation of the GeForce control panel’s custom resolution option, but with the monitor overclocking option exposed in PrecisionX and other utilities, monitor overclocking has been reduced to a simple slider rather than a complex mix of timings and pixel counts.

Though this feature can technically work with any monitor, it’s primarily geared towards monitors such as the various Korean LG-based 2560x1440 monitors that have hit the market in the past year, a number of which have come with electronics capable of operating far in excess of the 60Hz that is standard for those monitors. On the models that have been able to handle it, modders have been able to get some of these 2560x1440 monitors up to and above 120Hz, essentially doubling their native 60Hz refresh rate to 120Hz, greatly improving smoothness to levels similar to a native 120Hz TN panel, but without the resolution and quality drawbacks inherent to those TN products.

![img](https://images.anandtech.com/doci/6760/PixelClock.png)

Of course it goes without saying that just like any other form of overclocking, monitor overclocking can be dangerous and risks breaking the monitor. On that note, out of our monitor collection we were able to get our Samsung 305T up to 75Hz, but whether that’s due to the panel or the driving electronics it didn’t seem to have any impact on performance, smoothness, or responsiveness. This is truly a “your mileage may vary” situation.

**Origin’s Genesis: Titan on Water & More to Come**

Wrapping up part 1 of our look at NVIDIA’s GeForce GTX Titan, we wanted to take a quick look at the tri-SLI system NVIDIA sampled to us for this article: Origin’s Genesis. Without the ability to publish performance data we can’t go into any detail and otherwise fully evaluate it, but what we can do is give you a sneak peek at what’s among the most unusual, and likely most powerful Titan systems on the market.

But first, as a bit of a preface, as we mentioned earlier in our article NVIDIA has been sampling reviewers with various SFF and tri-SLI systems to showcase their two boutique computer concepts. With the tri-SLI system it was not only intended to show off raw performance, but also to serve as a showcase of Titan’s build quality. You see, NVIDIA had told us that the acoustics on Titan were so good that a tri-SLI system could not only be a reasonable choice from a background noise perspective, but that it would be notably quieter than even a GTX 680 tri-SLI system, the latter being particularly hard to believe given GTX 680’s impressive acoustics and low power consumption.

![img](https://images.anandtech.com/doci/6760/GeForce-GTX-Titan_Press_Final-11.png)

Of course, things didn’t exactly go according to plan, and in a happy accident Origin went above and beyond NVIDIA’s original request. As the Genesis’ marquee feature is water-cooling, Origin went all-out in setting up our sample system for water-cooling, and not just on the CPU. Despite the fact that Titan was (and technically still is) an unreleased card, working alongside their waterblock supplier [EKWaterBlocks](http://www.ekwb.com/) they were able to get proper waterblocks for Titan in time to build our system. As a result our tri-SLI Genesis unexpectedly ended up being both completely water-cooled and factory overclocked.

The bad news of course is that because of the performance embargo we can’t tell you anything about the performance of the Genesis, other than to say that as fast as one Titan card is, three overclocked Titan cards running on water is even faster, sometimes by a massive margin. Furthermore, coupled with this is the fact that GPU Boost 2 was designed in part to better mesh with the superior cooling capabilities of water-cooling, taking advantage of the fact that water-cooled GPUs rarely hit their temperature limits. As a result what’s already a fast system can sustain performance that much higher thanks to the fact that we hit our top boost bins more often.

But we’re getting ahead of ourselves here…

[![img](https://images.anandtech.com/doci/6760/originpc-full-titan-front-angle_575px.jpg)](https://images.anandtech.com/doci/6760/originpc-full-titan-front-angle.jpg)

| **Origin Genesis Specifications** |                                                              |
| --------------------------------- | ------------------------------------------------------------ |
| **Chassis**                       | Corsair 800D                                                 |
| **Processor**                     | Intel Core i7-3970X Extreme Edition, Overclocked To 4.9GHz, ORIGIN CRYOGENIC Custom Liquid Cooling CPU (6x4.9GHz, 32nm, 15MB L3, 150W) |
| **Motherboard**                   | Intel DX79SR                                                 |
| **Memory**                        | 16GB Corsair Vengeance DDR3 1866Mhz                          |
| **Graphics**                      | **3-WAY SLI** NVIDIA GeForce GTX TITAN, ORIGIN CRYOGENIC LIQUID Cooling Solution and Professional Overclocking |
| **Hard Drive(s)**                 | 2x120 GB Corsair Neutron SSDs in RAID 0  1TB Western Digital Caviar Black SATA 6.0Gb/s, 7200RPM, 64MB Cache |
| **Optical Drive(s)**              | 12X Blu-ray (BD) Disc Combo                                  |
| **Power Supply**                  | 1.2 Kilowatt PSU Corsair                                     |
| **Networking**                    | On-Board Intel                                               |
| **Audio**                         | Realtek ALC892 Speaker, line-in, mic, and surround jacks     |
| **Front Side**                    | Power button 4x Fan Controls 40-in-1 card reader 2x USB 3.0 2x USB 2.0 Mic and headphone jacks |
| **Top Side**                      | -                                                            |
| **Operating System**              | Windows 7 Ultimate 64-bit                                    |
| **Dimensions**                    | 16.2" x 4.6" x 16" (412mm x 117mm x 407mm)                   |
| **Warranty**                      | 1 Year Part Replacement and 45 Day Free Shipping Warranty with Lifetime Labor/24-7 Support |
| **Pricing**                       | MSRP of review system: ~$7000                                |

We’ll have more on Thursday, including performance data for what so far is turning out to be a ridiculously fast tri-SLI system. So until then, stay tuned.