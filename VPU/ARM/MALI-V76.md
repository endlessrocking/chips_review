![img](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_22b_678x452.png)





Alongside today’s 76-series [CPU](https://www.anandtech.com/show/12785/arm-announces-cortex-a76-nextgen-cpu) and [GPU](https://www.anandtech.com/show/12834/arm-announces-the-mali-g76-scaling-up-bifrost) announcements from Arm, the company also has one last product announcement for the day. Joining Arm’s video processor family is a new encode/decode IP block, the aptly-named Mali-V76.

Arm’s Mali video decoders aren’t as flashy as their GPUs and don’t get the same degree of attention accordingly. But for an IP vendor like Arm, they’re an important part of their graphics portfolio and a very necessary counterpart to their Mali GPU designs. So along with the new Mali-G76 GPU, Arm has put together a new video block to go with it.

The new V76 is essentially the successor to Arm’s previous high-end video block, the [Mali-V61](https://www.anandtech.com/show/10805/arm-announces-mali-g51-mali-v61), which was announced back in 2016. Understandably the world of video encoding and decoding doesn’t evolve at quite as brisk a pace as GPUs, so Arm generally only revises their video blocks at about half the frequency.

[![img](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_04_575px.png)](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_04.png)

Overall the V76 brings a slew of changes to Arm’s video processor ecosystem. On the performance front the new video block offers twice the decode performance of the V61, and on the encode side Arm says that encoding quality has been improved by about 25%. Meanwhile on the features front, the latest block adds support for 10-bit H.264 encoding and decoding, the one major codec/format that wasn’t already present on the V61.

From a hardware perspective, Arm has retained their scalable core design, and the V76 is intended for designs ranging from 2 to 8 cores. Arm’s ambitions are very forward-looking given the longer timeframe between generation, and as a result at a nominal frequency of 600MHz, an 8 core design is slated to be able to decode up to decode videos up to 8Kp60, and encode up to 8Kp30. Or for a smaller 4 core design, that becomes 4Kp120 decoding and 4Kp60 encoding. As previously stated, this is twice the throughput per-core of the V61, meaning that at least at nominal frequencies, this is the first Arm video processor block suitable for 8K video (as well as high frame rate 4K).

[![img](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_08_575px.png)](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_08.png)

Under the hood things haven’t changed too much, as Arm has stuck with their now traditional mix of fixed function and programmable hardware to split up the various steps of video encoding/decoding and issue it to purpose-built hardware as much as possible. And while this wasn’t said by Arm, looking at the performance and feature specifications of the new processor, it looks like the V76 is derived from the same general architecture as the also recently announced low-end [Mali-V52 video processor](https://www.anandtech.com/show/10805/arm-announces-mali-g51-mali-v61), which offers the same per-core performance and features, but not the total scalability.

[![img](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_10_575px.png)](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_10.png)

Along with the greater resolution support, the other most notable addition to the new processor is support for 10-bit H.264 video. This format was oddly absent in the V61 – the processor supported 10-bit HEVC, but not H.264 – and at the time the company didn’t think it would be needed. The slow adoption of HEVC relative to the faster adoption of HDR has changed that however, so for the V76 both encode and decode support for the format is being included.

On that note, however, this processor will **not** include any support for the upcoming AV1 codec. While the bitstream specification for the eagerly anticipated codec was released a couple of months back, the timing was unfortunately after Arm had already completed the V76 RTL (never mind the fact that the specification isn’t closed yet). So it’s going to have to be the next video block after the V76 before Arm can include AV1 decode support.

| Arm Mali-V Supported Video Codecs (Encode & Decode) |      |      |      |
| --------------------------------------------------- | ---- | ---- | ---- |
| Codec                                               | V61  | V52  | V76  |
| **H.264 8-Bit**                                     | Yes  | Yes  | Yes  |
| **H.264 10-Bit**                                    | No   | Yes  | Yes  |
| **HEVC 8-Bit**                                      | Yes  | Yes  | Yes  |
| **HEVC 10-Bit**                                     | Yes  | Yes  | Yes  |
| **VP9 8-Bit**                                       | Yes  | Yes  | Yes  |
| **VP9 10-Bit**                                      | Yes  | Yes  | Yes  |
| **AV1**                                             | No   | No   | No   |

Meanwhile on the encode front, Arm’s latest processor includes a couple different improvements to improve their encode quality. Overall the encode quality is up roughly 25% over the V61 based on PSNR metrics, however this improvement isn’t entirely attributable to software. Arm is basing their comparison against the initial release firmware of the V61, which continued to receive updated firmware over its lifetime that also improved its encoding quality (though that firmware was often not distributed to existing phones). In practice the quality improvements are a 40/60 split between software and hardware, so just over half of the improvement is on the hardware side, or around 15% of the cumulative quality improvement.

[![img](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_14_575px.png)](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_14.png)

Still, with phone manufacturers finally embracing HEVC encoding for video and images, the improvement comes as an important time. The very high encoding requirements of AV1 also mean that even after a decoder ships in a phone, we’re unlikely to see a full-featured encoder in a phone any time soon. So it will be necessary to maximize HEVC encoding quality going forward.

It all goes without saying, of course, that Arm is looking to scoop (and keep) competition from other vendors of video processors. Which means that they need to not only improve over their past designs, but keep ahead of their competition as well. Arm customers already get other benefits from remaining in-ecosystem, as it were, by being able to use Arm’s frame buffer compression technology throughout their display pipeline, but at the end of the day Mali GPUs can be used with other video blocks, and for that matter V76 could be used with other GPUs.

[![img](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_21_575px.png)](https://images.anandtech.com/doci/12835/05_Mali-V76%20Deep%20Dive_NoWM_21.png)

Finally, while not a focus of their presentation, Arm also briefly commented on HDR support in our briefing. In concert with their display processor, the new video processor is currently able to handle HDR10 and HLG formatted HDR video. Meanwhile support for HDR10+ – which is HDR10 with support for dynamic metadata – is set to arrive in the future. This is an important distinction, as Arm’s display controller can’t support Dolby Vision, meaning that HDR10+ would be the only dynamic HDR format that Arm can support.