Earlier this month [NVIDIA announced their latest generation flagship GeForce card, the GeForce GTX 1080](http://anandtech.com/show/10304/nvidia-announces-the-geforce-gtx-1080-1070). Based on their new Pascal architecture and built on TSMC’s 16nm FinFET process, the GTX 1080 is being launched as the first 16nm/14nm-based video card, and in time-honored fashion NVIDIA is starting at the high-end. The end result is that the GTX 1080 will be setting the new high mark for single-GPU performance.

Unlike past launches, NVIDIA is stretching out the launch of the GTX 1080 a bit more. After previously announcing it back on May 6th, the company is lifting their performance and architecture embargo today. Gamers however won’t be able to get their hands on the card until the 27th – next Friday – with pre-order sales starting this Friday. It is virtually guaranteed that the first batch of cards will sell out, but potential buyers will have a few days to mull over the data and decide if they want to throw down $699 for one of the first Founders Edition cards.

As for the AnandTech review, as I’ve only had a few days to work on the article, I’m going to hold it back rather than rush it out as a less thorough article. In the meantime however, as I know everyone is eager to see our take on performance, I wanted to take a quick look at the card and the numbers as a preview of what’s to come. Furthermore the entire performance dataset has been made available in the new [GPU 2016 section of AnandTech Bench](http://www.anandtech.com/bench/GPU16/), for anyone who wants to see results at additional resolutions and settings.

## Architecture  

| NVIDIA GPU Specification Comparison |                          |             |             |             |
| ----------------------------------- | ------------------------ | ----------- | ----------- | ----------- |
|                                     | GTX 1080                 | GTX 980 Ti  | GTX 980     | GTX 780     |
| **CUDA Cores**                      | 2560                     | 2816        | 2048        | 2304        |
| **Texture Units**                   | 160                      | 176         | 128         | 192         |
| **ROPs**                            | 64                       | 96          | 64          | 48          |
| **Core Clock**                      | 1607MHz                  | 1000MHz     | 1126MHz     | 863MHz      |
| **Boost Clock**                     | 1733MHz                  | 1075MHz     | 1216MHz     | 900Mhz      |
| **TFLOPs (FMA)**                    | 9 TFLOPs                 | 6 TFLOPs    | 5 TFLOPs    | 4.1 TFLOPs  |
| **Memory Clock**                    | 10Gbps GDDR5X            | 7Gbps GDDR5 | 7Gbps GDDR5 | 6Gbps GDDR5 |
| **Memory Bus Width**                | 256-bit                  | 384-bit     | 256-bit     | 384-bit     |
| **VRAM**                            | 8GB                      | 6GB         | 4GB         | 3GB         |
| **FP64**                            | 1/32                     | 1/32        | 1/32 FP32   | 1/24 FP32   |
| **TDP**                             | 180W                     | 250W        | 165W        | 250W        |
| **GPU**                             | GP104                    | GM200       | GM204       | GK110       |
| **Transistor Count**                | 7.2B                     | 8B          | 5.2B        | 7.1B        |
| **Manufacturing Process**           | TSMC 16nm                | TSMC 28nm   | TSMC 28nm   | TSMC 28nm   |
| **Launch Date**                     | 05/27/2016               | 06/01/2015  | 09/18/2014  | 05/23/2013  |
| **Launch Price**                    | MSRP: $599 Founders $699 | $649        | $549        | $649        |

While I’ll get into architecture in much greater detail in the full article, at a high level the Pascal architecture (as implemented in GP104) is a mix of old and new; it’s not a revolution, but it’s an important refinement. Maxwell as an architecture was very successful for NVIDIA both at the consumer level and the professional level, and for the consumer iterations of Pascal, NVIDIA has not made any radical changes. The basic throughput of the architecture has not changed – the ALUs, texture units, ROPs, and caches all perform similar to how they did in GM2xx.

Consequently the performance aspects of consumer Pascal – we’ll ignore GP100 for the moment – are pretty easy to understand. NVIDIA’s focus on this generation has been on pouring on the clockspeed to push total compute throughput to 9 TFLOPs, and updating their memory subsystem to feed the beast that is GP104.

[![img](https://images.anandtech.com/doci/10326/GeForce_GTX_1080_Block_Diagram_FINAL_575px.png)](https://images.anandtech.com/doci/10326/GeForce_GTX_1080_Block_Diagram_FINAL.png)

On the clockspeed front, a great deal of the gains come from the move to 16nm FinFET. The smaller process allows NVIDIA to design a 7.2B transistor chip at just 314mm2, while the use of FinFET transistors, though ultimately outright necessary for a process this small to avoid debilitating leakage, has a significant benefit to power consumption and the clockspeeds NVIDIA can get away with at practical levels of power consumption. To that end NVIDIA has sort of run with the idea of boosting clockspeeds, and relative to Maxwell they have done additional work at the chip design level to allow for higher clockspeeds at the necessary critical paths. All of this is coupled with energy efficiency optimizations at both the process and architectural level, in order to allow NVIDIA to hit these clockspeeds without blowing GTX 1080’s power budget.

[![img](https://images.anandtech.com/doci/10326/PascalCraft_575px.png)](https://images.anandtech.com/doci/10326/PascalCraft.png)

Meanwhile to feed GTX 1080, NVIDIA has made a pair of important changes to improve their effective memory bandwidth. The first of these is the inclusion of faster GDDR5X memory, which as implemented on GTX 1080 is capable of reaching 10Gb/sec/pin, a significant 43% jump in theoretical bandwidth over the 7Gb/sec/pin speeds offered by traditional GDDR5 on last-generation Maxwell products. Coupled with this is the latest iteration of NVIDIA’s delta color compression technology – now on its fourth generation – which sees NVIDIA once again expanding their pattern library to better compress frame buffers and render targets. NVIDIA’s figures put the effective memory bandwidth gain at 20%, or a roughly 17% reduction in memory bandwidth used thanks to the newer compression methods.

[![img](https://images.anandtech.com/doci/10326/PascalCompress_575px.png)](https://images.anandtech.com/doci/10326/PascalCompress.png)

As for features included, we’ll touch upon that in a lot more detail in the full review. But while Pascal is not a massive overhaul of NVIDIA’s architecture, it’s not without its own feature additions. Pascal gains the ability to pre-empt graphics operations at the pixel (thread) level and compute operations at the instruction level, allowing for much faster context switching. And on the graphics side of matters, the architecture introduces a new geometry projection ability – Simultaneous Multi-Projection – and as a more minor update, gets bumped up to Conservative Rasterization Tier 2.

[![img](https://images.anandtech.com/doci/10326/PascalPreempt_575px.png)](https://images.anandtech.com/doci/10326/PascalPreempt.png)

Looking at the raw specifications then, GTX 1080 does not disappoint. Though we’re looking at fewer CUDA cores than the GM200 based GTX 980 Ti or Titan, NVIDIA’s significant focus on clockspeed means that GP104’s 2560 CUDA cores are far more performant than a simple core count would suggest. The base clockspeed of 1607MHz is some 42% higher than GTX 980 (and 60% higher than GTX 980 Ti), and the 1733MHz boost clockspeed is a similar gain. On paper, GTX 1080 is set to offer 78% better performance than GTX 980, and 47% better performance than GTX 980 Ti. The real world gains are, of course, not quite this great, but they’re also relatively close to these numbers at times.

[![img](https://images.anandtech.com/doci/10326/GTX1080Bare_575px.jpg)](https://images.anandtech.com/doci/10326/GTX1080Bare.jpg)

## Gaming Performance, Power, Temperature, & Noise

So with the basics of the architecture and core configuration behind us, let’s dive into some numbers.

![Rise of the Tomb Raider - 3840x2160 - Very High (DX11)](https://images.anandtech.com/graphs/graph10326/81656.png)

![Dirt Rally - 3840x2160 - Ultra](https://images.anandtech.com/graphs/graph10326/81657.png)



![Ashes of the Singularity - 3840x2160 - Extreme](https://images.anandtech.com/graphs/graph10326/81658.png)

![Battlefield 4 - 3840x2160 - Ultra Quality (0x MSAA)](https://images.anandtech.com/graphs/graph10326/81659.png)

![Crysis 3 - 3840x2160 - Very High Quality + FXAA](https://images.anandtech.com/graphs/graph10326/81660.png)

![The Witcher 3 - 3840x2160 - Ultra Quality (No Hairworks)](https://images.anandtech.com/graphs/graph10326/81661.png)

![The Division - 3840x2160 - Ultra Quality](https://images.anandtech.com/graphs/graph10326/81662.png)

![Grand Theft Auto V - 3840x2160 - Very High Quality](https://images.anandtech.com/graphs/graph10326/81663.png)

![Hitman - 3840x2160 - Ultra Quality](https://images.anandtech.com/graphs/graph10326/81664.png)

As the first high-end card of this generation to launch, NVIDIA gets to set the pace for the market. At the risk of being redundant the GTX 1080 is now the fastest single-GPU card on the market, and even at 4K it wins at every single gaming benchmark, typically by a good margin. In practice we’re looking at a 31% performance lead over GTX 980 Ti – the card the GTX 1080 essentially replaces – with a similar 32% lead over AMD’s Radeon R9 Fury X. Meanwhile against the slightly older GTX 980, that gap is 70%.

On a generational basis this ends up being very close to the 74% jump in 4K performance going from the GTX 680 to GTX 980. And although the pricing comparison is not especially flattering for NVIDIA here, it should be evident that NVIDIA isn’t just looking to sell GTX 1080 as an upgrade for high-end Kepler cards, but as an upgrade for GTX 980 as well, just 20 months after it launched.

![The Witcher 3 - 1920x1080 - Ultra Quality (No Hairworks)](https://images.anandtech.com/graphs/graph10326/81668.png)

I also wanted to quickly throw in a 1080p chart, both for the interest of comparing the GTX 1080 to the first-generation 28nm cards, and for gamers who are playing on high refresh rate 1080p monitors. Though this will of course vary from game to game, roughly speaking the GTX 1080 should be 3x faster than the GTX 680 or Radeon HD 7970. This is a good reminder of how architectural efficiency has played a greater role in past years, as this is a much larger gain than we saw jumping from 55nm to 40nm or 40nm to 28nm, both of which were much closer to the historical norm of 2x.

![Load Power Consumption - Crysis 3](https://images.anandtech.com/graphs/graph10326/81665.png)

Meanwhile when it comes to power, temperature, and noise, NVIDIA continues to execute very well here. Power consumption under Crysis 3 is some 20W higher than GTX 980 or 52W lower than GTX 980 Ti, generally in line with NVIDIA’s own TDP ratings after accounting for the slightly higher CPU power consumption incurred by the card’s higher performance. The end result is that GTX 1080 is a bit more power hungry than GTX 980, but still in the sweet spot NVIDIA has carved out in the gaming market. Broadly speaking, this amounts to a 54% increase in energy efficiency in the case of Crysis 3.

[![img](https://images.anandtech.com/doci/10326/GeForce_GTX_1080_3qtr_Front_Left_Thermal_575px.jpg)](https://images.anandtech.com/doci/10326/GeForce_GTX_1080_3qtr_Front_Left_Thermal.jpg)

![Load GPU Temperature - Crysis 3](https://images.anandtech.com/graphs/graph10326/81666.png)

![Load Noise Levels - Crysis 3](https://images.anandtech.com/graphs/graph10326/81667.png)

Otherwise from a design perspective the GTX 1080 Founders Edition carries on from NVIDIA’s high-end GTX 700/900 reference design, allowing NVIDIA to once again offer a superior blower-based solution. NVIDIA’s temperature management technology has not changed relative to Maxwell, so like their other cards, the GTX 1080 tops out in the low 80s for load temperature. More significantly, at 47.5 db(A) load noise, the card is on par with the GTX 780 and half a dB off of the GTX 980.

Ultimately NVIDIA has designed the GTX 1080 to be a drop-in replacement for the GTX 980, and this data confirms just that, indicating that GTX 1080’s much higher performance comes with only a slight increase in power consumption and no meaningful change in temperatures or acoustics.

## First Thoughts

Wrapping up our preview of the GeForce GTX 1080, I think it’s safe to say that NVIDIA intends to start off the 16nm/14nm generation with a bang. As the first high-end card of this generation the GTX 1080 sets new marks for overall performance and for power efficiency, thanks to the combination of TSMC’s 16nm FinFET process and NVIDIA’s Pascal architecture. Translating this into numbers, at 4K we’re looking at 30% performance gain versus the GTX 980 Ti and a 70% performance gain over the GTX 980, amounting to a very significant jump in efficiency and performance over the Maxwell generation.

[![img](https://images.anandtech.com/doci/10326/GeForce_GTX_1080_Front_575px.jpg)](https://images.anandtech.com/doci/10326/GeForce_GTX_1080_Front.jpg)

Looking at the bigger picture, as the first vendor to launch their 16nm/14nm flagship card, NVIDIA will get to enjoy the first mover’s advantage both with respect to setting performance expectations and with pricing. The GeForce GTX 1080 will keep the performance crown solidly in NVIDIA’s hands, and with it control of the high-end video card market for some time to come.  NVIDIA’s loyal opposition, AMD’s Radeon Technologies Group, has strongly hinted that they’re not going to be releasing comparable high-performance video cards in the near future. Rather the company is looking to make a run at the much larger mainstream market for desktops and laptops with their Polaris architecture, something that GP104 isn’t meant to address.

The lack of competition at the high-end means that for the time being NVIDIA can price the GTX 1080 at what the market will bear, and this is more or less what we’re looking at for NVIDIA’s new card. While the formal MSRP on the GTX 1080 is $599 – $50 over what the GTX 980 launched at – that price is the starting price for custom cards from NVIDIA’s partners. The reference card as we’ve previewed it today – what NVIDIA is calling the Founders Edition card – carries a $100 premium over that, pushing it to $699.

| GeForce GTX 1080 Configurations |                                                    |                                           |
| ------------------------------- | -------------------------------------------------- | ----------------------------------------- |
|                                 | Base                                               | Founders Edition                          |
| **Core Clock**                  | 1607MHz                                            | 1607MHz                                   |
| **Boost Clock**                 | 1733MHz                                            | 1733MHz                                   |
| **Memory Clock**                | 10Gbps GDDR5X                                      | 10Gbps GDDR5X                             |
| **Cooler**                      | Manufacturer Custom (Typical: 2 or 3 Fan Open Air) | NVIDIA Reference (Blower w/Vapor Chamber) |
| **Availability Date**           | June 2016?                                         | 05/27/2016                                |
| **Price**                       | Starting at $599                                   | $699                                      |

While the differences between the reference and custom cards will be a longer subject for our full review, the more immediate ramification is going to be that only the Founders Edition cards are guaranteed to be available at launch. NVIDIA can’t speak definitively for their board partners, but at this point I am not seriously expecting custom cards until June. And this means that if you want one of the first GTX 1080s, then you’re going to have to pay $699 for the Founders Edition card. Which is not to say that it’s a bad card – far from it, it’s probably NVIDIA’s finest reference card to date – however it pushes the card’s price north of 980 Ti territory, some $150 higher than where the GTX 980 launched in 2014. For those who can afford such a card they will not be disappointed, but it’s definitely less affordable than past NVIDIA x80 cards.

Anyhow, we’ll be back later this week with our full review of the GeForce GTX 1080, so be sure to stay tuned.