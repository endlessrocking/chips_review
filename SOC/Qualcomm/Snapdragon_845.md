
Table of Contents
=================

      * [OVERVIEW](#overview)
      * [CPU &amp; Memory Subsystem](#cpu--memory-subsystem)
      * [System Performance](#system-performance)
      * [GPU Performance &amp; Power Estimates](#gpu-performance--power-estimates)
      * [irst Thoughts](#irst-thoughts)


## OVERVIEW



In what has become an annual tradition for Qualcomm, the company has once again opened the doors of their San Diego headquarters to the press to take a preview look at the next generation of their flagship mobile platform. These events have been going on for several years now, and have become an integral part of how Qualcomm approaches the public with their wares; preview events not only let them set expectations, but to get the word out to technically-minded audiences in a vendor-neutral manner. Rather than being one part in the next flagship smartphone, preview day means that everything can be about Qualcomm and the platforms that they have created.

Late last year [Qualcomm announced the Snapdragon 845 platform](https://www.anandtech.com/show/12114/qualcomm-announces-snapdragon-845-soc), the successor to 2017’s Snapdragon 835. Implementing a number of important architectural improvements over its predecessor, the Snapdragon 845 gets to follow-up on what ended up being a rather well-received platform in the Snapdragon 835, and to see if Qualcomm can maintain their momentum. Qualcomm used their December event to release a good bit of info on the 845 in advance, so we’ve already had a chance to see what Qualcomm is planning architecturally. And now with the preview event we finally get to see how all of this comes together with a look at the platform as a whole.

Whenever discussing the state of affairs of Qualcomm’s flagship SoCs, I always struggle not to tie it to the Snapdragon 810 in some fashion. Which not to beat Qualcomm over the head for past mistakes – in that case a poorly thought out response to Apple – but rather because it serves as a such a great point of reference for discussing the company’s SoC development as a whole. 810 was arguably the company’s low point, so everything since then has been part of a rather remarkable upward trajectory for the flagship Snapdragon. Even though Qualcomm has been leading the pack in high performance SoCs for several years now, last year’s Snapdragon 835 in particular really felt like Qualcomm was in that position for all-around technical capabilities and not merely because of size, momentum, and the realities of LTE licensing.

All of this means that there’s a lot riding on the Snapdragon 845, just in a different and less obvious way than before. Qualcomm has redeemed themselves from the 810 and it’s not a question of whether they can put together a great SoC, but instead it’s a question of how they will follow up upon a great SoC like the 835.

| Qualcomm Snapdragon 845 vs 835 |                                                              |                                                              |
| ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| SoC                            | Snapdragon 845                                               | Snapdragon 835                                               |
| CPU                            | 4x Kryo 385 Gold (A75 derivative) @ 2.8GHz 4x256KB L2  4x Kryo 385 Silver (A55 derivative) @ 1.77GHz 4x128KB L2  2MB L3 in DSU | 4x Kryo 280 Gold (A73 derivative) @ 2.45GHz 2MB L2  4x Kryo 280 Silver (A53 derivative) @ 1.90GHz 1MB L2 |
| GPU                            | Adreno 630                                                   | Adreno 540 @ 670/710MHz                                      |
| Memory                         | 4x 16-bit CH @ 1866MHz LPDDR4x 29.9GB/s  3MB system cache    | 4x 16-bit CH @ 1866MHz LPDDR4x 29.9GB/s                      |
| ISP/Camera                     | Dual 14-bit Spectra 280 ISP 1x 32MP or 2x 16MP               | Dual 14-bit Spectra 180 ISP 1x 32MP or 2x 16MP               |
| Encode/ Decode                 | 2160p60 10-bit H.265 720p480                                 | 2160p30 (2160p60 decode), 1080p120 H.264 & H.265             |
| Integrated Modem               | Snapdragon X20 LTE (Category 18/13)  DL = 1200Mbps 5x20MHz CA, 256-QAM  UL = 150Mbps 2x20MHz CA, 64-QAM | Snapdragon X16 LTE (Category 16/13)  DL = 1000Mbps 3x20MHz CA, 256-QAM  UL = 150Mbps 2x20MHz CA, 64-QAM |
| Mfc. Process                   | 10nm LPP                                                     | 10nm LPE                                                     |

The answer to that comes in the form of the Snapdragon 845, an interesting SoC that is a “tock” design if there ever was one. Qualcomm doesn’t get the advantage of an entirely new manufacturing node – the 845 is being made on Samsung’s second-generation 10LPP process, a refined version of 10LPE used for the 835 – so Qualcomm’s improvements are rooted almost entirely in architecture rather than a mix of architecture and manufacturing. Which is to say that it’s a bit of an uphill challenge for the company, but the flip side of that argument is that it’s going to be a chance for Qualcomm’s architectural engineers to take attention front and center.

[![img](https://images.anandtech.com/doci/12420/sd845_blockdiagram_575px.png)](https://images.anandtech.com/doci/12420/sd845_blockdiagram.png)

What the Snapdragon 845 entails then, [as we originally learned late last year](https://www.anandtech.com/show/12114/qualcomm-announces-snapdragon-845-soc), is a series of upgrades and overhauls across all the various subsystems of the SoC. Arguably the biggest news here is that Qualcomm’s latest-generation Kyro 385-series CPU cores are derived from ARM’s Cortex-A75 and A55 designs, and that the resulting SoC is the first to employ ARM's [DynamiQ CPU cluster organization](https://www.anandtech.com/show/11441/dynamiq-and-arms-new-cpus-cortex-a75-a55). DynamIQ enables the various different CPU cores within an SoC to be hosted within the same cluster and cache hierarchy, as opposed to having separate discrete clusters with no shared cache between them, allowing for finer-grained and more efficient approaches to when and how various clusters are powered up. Meanwhile on the GPU side, the notoriously tight-lipped GPU group over at Qualcomm has confirmed that the Snapdragon 845 implements the first Adreno 600 series GPU, which in turn is the first new GPU architecture from Qualcomm in a couple of years and promises some significant performance improvements.

Outside of the core processor architecture, the changes in the rest of the SoC are perhaps not quite as dramatic, but still important to the platform as a whole. This includes, of course, Qualcomm’s latest and greatest LTE modem, the Snapdragon X20, upgrading Qualcomm’s LTE capabilities category 18. Both the camera ISP and Hexagon DSP have also been upgraded as well with the introduction of the Spectra 280 and Hexagon 685, which Qualcomm will be leveraging for camera image quality improvements and their stake in the modern mobile AI race respectively. Finally, the SoC also includes the latest version of the company’s Aqstic audio codec, which although audio has not traditionally been heavily promoted by the company, will be an increasingly important part of differentiating itself from other high-performance mobile SoCs.

[![img](https://images.anandtech.com/doci/12420/qc_qrd_575px.jpg)](https://images.anandtech.com/doci/12420/qc_qrd.jpg)

Getting down to the heart of matters then, this year’s flagship Snapdragon platform preview is a lot like last year’s. We’re once again taking a look at a Qualcomm Reference Design (QRD), which is a fully functional smartphones in a slightly oversized, utilitarian chassis used for hardware testing and software development. The Snapdragon 835 QRD was a 5.5-inch equivalent phone, and for the 845 QRD Qualcomm has stuck with much the same. The device itself is unremarkable, featuring a 1440p LCD and 6GB of LPDDR4X memory, but it’s otherwise typical of the class of Snapdragon 845 devices we expect to see starting a bit later this year.

Similarly, while this is still a preview, final device performance shouldn’t be too much different from what we see with Qualcomm’s QRD. Vendors do make customizations to both hardware and software, so how a device’s cooling system is built or how aggressive the power management is configured will have an impact on final performance. But as far as stock performance goes, the QRD is about as neural as it gets, if not a slightly idealized case for the platform as it allows Qualcomm to optimally configure the phone themselves.





## CPU & Memory Subsystem

As we mentioned earlier, the Snapdragon 845 is the first SoC employing ARM’s new cluster technology DynamiQ. The different CPU cores are no longer hosted in dedicated cluster subsystems but are now integrated in a larger DynamiQ cluster. This change means that the cluster cache which to date was referred to as the L2 cache becomes the L3 cache and the individual CPU cores now receive a new private per-core L2. In the case of the Snapdragon 845, the Kryo 385 performance cores – derivative of ARM’s new A75 – are configured with 256KB L2 caches. The Kryo 845 efficiency cores, which are derivative of the A55, use 128KB L2 cache configurations.

[![img](https://images.anandtech.com/doci/12420/cpu_575px.png)](https://images.anandtech.com/doci/12420/cpu.png)

The L3 cache of the DynamiQ Shared Unit (DSU) is configured at 2MB. At the launch of the Snapdragon 845 Qualcomm advertised three voltage and clock domains – unfortunately we haven’t had time to look deeper into the system of the QRD to find out how this is partitioned, however it is still my unconfirmed belief that the third clock/voltage domain is dedicated to the DSU and not part of the CPU cores. An important characteristic that is totally new to the Android SoC ecosystem is the introduction of a system cache – this 3MB cache seems to sit at the memory controller / interconnect level above the CPU subsystem, something we’ll get back to in just a bit.Qualcomm’s performance projections seemed relatively conservative as they claimed a performance uplift of only 25-30% which seemed lower than ARM’s projections. We have to keep in mind that beyond the microarchitectural improvements expected from the transition from A73 to A75 based CPU cores we also have a flat 14% frequency increase from 2.47GHz to 2.8GHz on the side of the performance cores. Unfortunately in the limited testing time we had with the QRD we couldn’t make use of long-running CPU benchmarks such as our SPEC suite, so for the scope of this article we had to base our synthetic analysis on GeekBench4 results.

| Geekbench 4 - Integer Performance Single Threaded |                   |                   |            |
| ------------------------------------------------- | ----------------- | ----------------- | ---------- |
|                                                   | Snapdragon 845    | Snapdragon 835    | % Increase |
| **AES**                                           | 1160 MB/s         | 942.5 MB/s        | **23.1%**  |
| **LZMA**                                          | 4.15 MB/s         | 2.98 MB/s         | **39.3%**  |
| **JPEG**                                          | 20.8 Mpixels/s    | 16.6 Mpixels/s    | **25.2%**  |
| **Canny**                                         | 32.1 Mpixels/s    | 24.9 Mpixels/s    | **28.8%**  |
| **Lua**                                           | 2.18 MB/s         | 1.75 MB/s         | **24.0%**  |
| **Dijkstra**                                      | 1.90 MTE/s        | 1.62 MTE/s        | **16.9%**  |
| **SQLite**                                        | 70.3 Krows/s      | 53.4 Krows/s      | **31.8%**  |
| **HTML5 Parse**                                   | 12.9 MB/s         | 8.97 MB/s         | **44.1%**  |
| **HTML5 DOM**                                     | 3.00 Melems/s     | 2.27 Melems/s     | **31.9%**  |
| **Histogram Equalization**                        | 67.3 Mpixels/s    | 52.5 Mpixels/s    | **28.2%**  |
| **PDF Rendering**                                 | 66.4 Mpixels/s    | 48.5 Mpixels/s    | **37.0%**  |
| **LLVM**                                          | 321.2 functions/s | 257.3 functions/s | **24.8%**  |
| **Camera**                                        | 7.96 images/s     | 5.64 images/s     | **40.9%**  |

For the integer workload results we see a healthy performance across the various tests. Qualcomm’s 25-30% increase here seems to be justified as this is the most common increase in most tests. Workloads such as LZMA, HTML5 parsing, PDF rendering and the Camera substests see larger increases into the 40% range. The overall improvement in absolute performance for the integer tests is 31%.

![Geekbench 4  (Single Threaded) Integer Score/MHz](https://images.anandtech.com/graphs/graph12420/95155.png)

If we revisit performance per clock across recent microarchitectures we see the Snapdragon’s A75 based cores increase by only a meagre 15% which is below our expectations. We move on to the floating point benchmarks to see if we see a similar story.

| Geekbench 4 - Floating Point Performance Single Threaded |                 |                 |            |
| -------------------------------------------------------- | --------------- | --------------- | ---------- |
|                                                          | Snapdragon 845  | Snapdragon 835  | % Increase |
| **SGEMM**                                                | 16.6 GFLOPS     | 11.4 GFLOPS     | **45.1%**  |
| **SFFT**                                                 | 4.23 GFLOPS     | 2.86 GFLOPS     | **47.9%**  |
| **N-Body Physics**                                       | 1400 Kpairs/s   | 872.2 Kpairs/s  | **60.5%**  |
| **Rigid Body Physics**                                   | 8524.2 FPS      | 6130.5 FPS      | **39.0%**  |
| **Ray Tracing**                                          | 354.0 Kpixels/s | 232.7 Kpixels/s | **52.1%**  |
| **HDR**                                                  | 11.9 Mpixels/s  | 8.31 Mpixels/s  | **43.2%**  |
| **Gaussian Blur**                                        | 34.5 Mpixels/s  | 23.9 Mpixels/s  | **44.3%**  |
| **Speech Recognition**                                   | 17.9 Words/s    | 13.6 Words/s    | **31.6%**  |
| **Face Detection**                                       | 752.4 Ksubs/s   | 532.8 Ksubs/s   | **41.2%**  |

The FP subtests of GB4 show a noticeably larger increase than the integer tests. Besides the switch from a 2-wide decode front-end to a 3-wide one, the largest changes of the A75 microarchitecture was found in the floating point execution pipelines and is likely the cause for the larger FP performance improvement. The boost here comes at an overall 45% in GB4.

![Geekbench 4 (Single Threaded) Floating Point Score/MHz](https://images.anandtech.com/graphs/graph12420/95156.png)

In terms of performance per clock, the 45% overall boost translates into a much larger 26% increase in IPC which is nearer to what we had expected.

[![img](https://images.anandtech.com/doci/12420/arm-a75_a55-a75_perf_575px.png)](https://images.anandtech.com/doci/12420/arm-a75_a55-a75_perf.png)

Revisiting the performance claims from ARM’s TechDay release of the A75 we notice that we had been promised larger improvements such as up to a 34% increase in GB4 performance per clock, which I interpreted with the frequency increase of the Snapdragon 845 to result in a 52% overall increase, which did not materialise. I reached out to ARM on the topic and got back several points of consideration: The projections ARM published were made on a A75 simulation with 512KB L2 caches and 2MB L3. The L3 matches the configuration of the Snapdragon 845 however Qualcomm’s choice of going with smaller L2 caches will have a certain performance hit. ARM didn’t have a number at hand for GB4 but quotes a 2% performance degradation for SPEC2000, and claims for GB4 it should be lower. Another consideration point is the memory subsystem of the SoC which ARM can’t control but heavily impacts the performance of the CPU, so let’s have a look at that.

[![img](https://images.anandtech.com/doci/12420/845lat_575px.png)](https://images.anandtech.com/doci/12420/845lat.png)

Running our internal memory benchmark on the QRD we see several expected characteristics of the Snapdragon 845: Compared to the Snapdragon 835’s A73 based cores we see the shift from shared cluster L2’s to private ones as well as the integration of sort of an L3 and L4 cache. The new L2 caches are very visible in our benchmark as memory latency up to the 256KB barrier (or rather, the 320KB barrier as the L1D and L2 are exclusive) sees a vast reduction compared to the L2 region of the A73 cores. The A75 cores promise 8-cycle hits for the L2 versus 19 cycles on the A73. In our test the difference is far larger as see a reduction from ~30ns down to ~4.5ns (not forgetting a clock frequency increase of the new cache). After the 256/320KB test size boundary we enter the DSU’s L3 cache. ARM describes the L3 as pseudo-exclusive so the outer boundary should end around or shortly after the 2048KB mark, the transition here is much harder to make out in the limited data we had time to collect so hopefully we’ll get to revisit it on a commercial device.

On the Snapdragon 835 the transition between L2 cache and DRAM is very sharp and visible in the graph. On the Snapdragon 845 however we see a far more gradient latency transition stretching out to up to the 5MB test depth. This is confirmation that Qualcomm’s system cache is indeed applied to the CPU subsystem and acts as an exclusive L4 cache to the processors. I think this new system cache is a true SoC-wide cache lying high up at the interconnect or memory controller level.

One of the worries of such a configuration for the CPU subsystem was increased latency to DRAM and it seems my fears were realised as the Snapdragon 845 shows a 30% increase in main memory latency from the CPU subsystem. Previously the Snapdragon 835 seemed to have by far one of the best memory controller implementations which directly resulted in higher performance of memory latency sensitive workloads. The latency increase in the 845 thus must be counteracting some of the microarchitectural improvements on part of the CPU cores. For GB4 in particular I made a remark that I didn’t notice any performance impact at all on the part of the Kirin 970’s memory latency, however we’re talking about different platforms and CPUs so I can’t be certain.

We reserve final conclusion on synthetic benchmarks until we get more time with a Snapdragon 845 device and able to investigate more and run SPEC. For now it looks like the Snapdragon 845 does not reach ARM’s projected performance levels, and falls well short of the claims. Among one of the other performance claims was Octane. We retired Octane some years ago and Google shortly followed up with official retirement, but as an added data-point the Snapdragon 845 reached a score of 15969 versus the Snapdragon 835’s 11879, also well short of a 20000 target that a projected 1.48x per clock performance increase would have resulted in.



## System Performance

To see how the new CPUs and memory subsystem translate into more real system performance, we move onto more representative tests such as PCMark. PCMark’s performance is affected by several factors: not only does raw performance of the hardware count but also we need to consider the individual system’s software stack. We’ve seen large differences between Android OS major versions where the improvements of the Android Runtime can be directly visible in subtests such as the Writing test. Also a SoC’s DVFS schemes and schedulers can have huge impacts on “performance-latency”, meaning how fast the CPUs can ramp up a workload. This directly translates in a lot more performance in several of PCMark’s subtests as in the default settings none of the tests actually represent the pure performance of the CPU if it were locked at maximum frequency on the performance cores. The results of the tests are also overall a good representation of “snappiness” of a device.

![PCMark Work 2.0 - Web Browsing 2.0](https://images.anandtech.com/graphs/graph12420/95162.png)

In the web browsing test the Snapdragon 845 QRD manages to outpace the Pixel 2 XL by 20%. Here we’re also looking at performance across devices with different OS versions. The Google devices are running Android 8.1 while the Samsung devices were tested with Android 7.0. The Mate 10 Pro runs Android 8.0 while the Mate 9 still had 7.0. The Qualcomm QRD we tested ran Android 8.0.

Again the performance increase over Snapdragon 835 devices isn’t all that great. DynamiQ allows for far more efficient thread transitions between the CPU cores and subsequently I expected Qualcomm to take advantage of this through more aggressive scheduling resulting in more than just a 20% increase. The difference between the Mate 9 and Mate 10 here is a good example of what a software configuration change can bring in terms of performance (both devices employ same performance CPU configurations). Samsung’s Exynos’ SoCs still use GTS scheduling and have non-optimal performance-latency resulting in bad scores, amplified by the fact that Samsung’s memory performance is also underwhelming when compared to the Snapdragon and Kirin SoCs.

![PCMark Work 2.0 - Data Manipulation](https://images.anandtech.com/graphs/graph12420/95158.png)![PCMark Work 2.0 - Writing 2.0](https://images.anandtech.com/graphs/graph12420/95163.png)

The Data Manipulation and Writing 2.0 tests make heavy use of the Android runtime and APIs and also a very memory latency sensitive. Between the best showings of the Snapdragon 835 variant of the S8 and the Pixel 2 XL in each respective benchmark, the Snapdragon QRD845 showed conservative increases of 8 to 14%. The Exynos SoCs lacklustre performance is again hampered by software and by bad memory performance.

![PCMark Work 2.0 - Video Editing](https://images.anandtech.com/graphs/graph12420/95161.png)

The video editing test is PCMark’s weak-point as it’s bottlenecked by things such as OS API overhead, and why we see tight grouping of performance results across a large range of SoCs. The Snapdragon 845 ends up high, but below the Pixel 2 XL. I would not put much weight on the results of this test as they’re not necessarily representative. Futuremark claims that the test is a lot more sensitive in mid- and low-range devices which can exhibit performance issues.

![PCMark Work 2.0 - Photo Editing 2.0](https://images.anandtech.com/graphs/graph12420/95160.png)

The photo editing test makes heavy use of Renderscript and use GPU acceleration to apply various effects on an image set. The QRD845 here shines as it’s able to showcase a 38% performance improvement over the Pixel 2 XL. Again the test not solely tests the raw performance of the system but also how optimized it is in terms of the software stack. This can be seen in the Kirin vs Exynos devices as Huawei’s phones vastly outperform Samsung’s devices in this test.

![PCMark Work 2.0 - Performance](https://images.anandtech.com/graphs/graph12420/95159.png)

Overall PCMark’s performance score for the QRD845 increases by 17% over the Pixel 2 XL. Disregarding the video test, we see a similar scenario as in the synthetic tests as the new SoC’s CPU performance increases are lower than we had expected. Still the Snapdragon 845 is able to top the charts and should adequately power 2018’s flagship devices.

For 2018 we are reviewing our mobile benchmarking suite and altering some of the benchmarks we use. One of the changes in the way we benchmark devices is that we’re moving away from standalone browser and rather are benchmarking the OS’s WebView implementations. In general this seems to be a better choice for testing device experience as there is a lot of content that is being consumed via WebView windows. We also avoid the argument about different browser performance and since Google has now made WebView an updatable Play Store component we should also have valid comparisons older devices and systems. On the iOS side we do the same as we now benchmark browser tests within a WkWebView shell.

![WebXPRT 2015 - OS WebView](https://images.anandtech.com/graphs/graph12420/95171.png)

Starting off with WebXPRT 2015 for a last time before we’ll retire it in favour of WebXPRT 3, we see the QRD845 performing fantastically. Here the 44% performance increase over the Pixel 2 XL is a lot more in line with what we had expected of the new SoC. The QRD845 is even able to catch up a lot with Apple’s newest A11 and Monsoon cores in this test.

To keep up with the ever changing landscape of the developing web, we’re also retiring past JavaScript benchmarks in favour of a brand new and more representative benchmark developed by the [WebKit team](https://webkit.org/blog/8063/speedometer-2-0-a-benchmark-for-modern-web-app-responsiveness/)and [welcomed by Google](https://v8project.blogspot.lu/2018/01/speedometer-2.html); Speedometer 2.0.

![Speedometer 2.0 - OS WebView](https://images.anandtech.com/graphs/graph12420/95169.png)

Here the Snapdragon 845 showcased another healthy performance increase of 37% over the Snapdragon 835 devices. Apple’s superior JavaScript performance can be attributed to a much faster and more optimized Nitro engine while Google’s V8 has only seen meagre improvements over the years. Notable is the Apple A11’s massive performance jump over the A10 – vastly increasing the distance to Android devices.



## GPU Performance & Power Estimates

One of the larger changes that the Snapdragon 845 brings with itself is a new GPU architecture. Qualcomm has been traditionally very secretive when talking about details of their Adreno GPUs and the Adreno 630 is no different here. Truth to be told, the only real sign that we’re looking at more major architectural changes is the transition from the Adreno 5xx series to the Adreno 6xx series.

[![img](https://images.anandtech.com/doci/12420/gpu_575px.png)](https://images.anandtech.com/doci/12420/gpu.png)

While the Adreno 630 remains largely a black box we do know what Qualcomm’s claims for the GPU are. We’re looking at overall 30% better performance and a 30% improvement in power. The latter point is something that Qualcomm liked to showcase both at the announcement of the Snapdragon 845 as well as for this benchmarking event, however it needs to be clarified that the power improvement is measured at iso-performance levels. Naturally because the 845 targets higher performance points the power would be higher than at 835-levels of performance. Regardless of this marketing nit-pick, we’re still expecting an efficiency increase at peak performance levels if the resulting absolute power remains at the same levels as the Snapdragon 835.

![3DMark Sling Shot 3.1 Extreme Unlimited - Graphics - Peak](https://images.anandtech.com/graphs/graph12420/95164.png)

We start off with Futuremark’s 3DMark Sling Shot 3.1 Extreme Unlimited test. The graphics test mainly showcases the GPU improvements of a system and here the Snapdragon 845 easily reaches its performance target, improving by up to 32% compared to the Snapdragon 835 powered Pixel 2 XL and Galaxy S8. This is an astonishingly great achievement for Qualcomm in one generation.

When we’re looking at competitor devices we see only the the iPhone X able to compete with the last generation Snapdragon 835 devices – however with a catch. The A11 is severely thermally constrained and is only able to achieve these scores when the devices are cold. Indeed as seen from the smaller score of the iPhone 8, the SoC isn’t able to sustain maximum performance for even one benchmark run before having to throttle. Unfortunately this also applies to current and last generation Exynos and Kirin SoCs as both shed great amount of performance after only a few minutes. I’ve addressed this issue and [made a great rant about it in our review of the Kirin 970](https://www.anandtech.com/show/12195/hisilicon-kirin-970-power-performance-overview/4). For this reason going forward AnandTech is going to distinguish between Peak and Sustained scores across all 3D benchmarks. This however needs to be tested on commercial devices as the QRD platform isn’t a thermally representative phone for the SoC, so until that happens, we’ll have to just estimate based on power consumption where the Snapdragon 845 ends up.

![3DMark Sling Shot 3.1 Extreme Unlimited - Physics - Peak](https://images.anandtech.com/graphs/graph12420/95166.png)

The physics score is a CPU-bound test and less limited by the GPU. Here the Snapdragon 845 provides a good improvement over the Snapdragon 835 however to a meagre 14% increase which incidentally matches the clock frequency increase between the 845 and 835’s performance CPUs.

![3DMark Sling Shot 3.1 Extreme Unlimited - Overall - Peak](https://images.anandtech.com/graphs/graph12420/95165.png)

Overall the QRD845 platform leads the Sling Shot Extreme rankings by a comfortable margin.

Moving on to GFXBench I decided to focus on T-Rex and Manhattan 3.1 as both tests stress different aspects of the GPU, fill-rate and texturing bound workloads versus more arithmetic bound workloads.

![GFXBench T-Rex 2.7 Off-screen - Peak](https://images.anandtech.com/graphs/graph12420/95168.png)

In T-Rex the Snapdragon 845 again shows an impressive 31% increase over the Snapdragon 835. This time around it’s not enough to quite match the Apple A11 but I expect that situation to quickly reverse as the latter becomes thermally constrained.

![GFXBench Manhattan 3.1 Off-screen - Peak](https://images.anandtech.com/graphs/graph12420/95167.png)

Manhattan 3.1 is more shader and compute heavy and thus puts more stress on the ALU pipelines of the GPU. Here the Adreno 630 outpaces the Adreno 540 by an ever impressive 48%. Again the A11 matches the performance here but with a device becoming very hot quite fast while the QRD845 was merely luke-warm in our preview benchmarking session.

![GFXBench Synthetic Tests - Offscreen](https://images.anandtech.com/graphs/graph12420/95157.png)

GFXBench’s synthetic micro-tests should shed more light on the architectural improvements of the Adreno 640. Indeed looking at the results we see that the Snapdragon 845 is able to achieve an over 50% increase in the texturing test to an unmatched 15400MTexels/s. Qualcomm’s claims of 2.5x faster display throughput more than likely involves also vastly increased pixel fillrate capabilities on the side of the GPU so the architecture must have increased the number of ROPs and texturing units to get to such scores.

The ALU2 test shows a 30% increase in performance over the Snapdragon 845, however the fact that Manhattan 3.1’s score increased by up to 48% means that we’re likely seeing a more fundamental change in the ALU pipelines that lead to better utilisation ratio.

The tessellation results point out that the geometry pipelines haven’t received any large improvements. One fact-check that we unfortunately weren’t able to verify is the clock frequency of the Adreno 640. The fact that the tessellation test ends up in spitting distance of the Adreno 630 means that we’re very likely looking at clocks very similar to the Adreno 630 – in the 670 to 710MHz range.

Finally the driver overhead score shows both the increased raw CPU performance of the Snapdragon 845 as well as maybe an improvement in Qualcomm’s drivers.

As beforementioned, going forward we’re going to have a more heavy focus on GPU sustained performance as well as power. During the benchmarking session we were able to probe the QRD845 for power as measured by the fuel gauge by the PMIC. We must however note that these platforms aren’t usually power optimised and have early silicon bins – Qualcomm themselves don’t advise them for power measurements. Nevertheless curiosity got the best of us and the following estimated figures should be seen as worst-case scenarios for the Snapdragon 845.

| GFXBench Manhattan 3.1 Offscreen Power Efficiency (System Active Power) |              |           |                |                   |
| ------------------------------------------------------------ | ------------ | --------- | -------------- | ----------------- |
|                                                              | Mfc. Process | FPS       | Avg. Power (W) | Perf/W Efficiency |
| Qualcomm QRD (Snapdragon 845)                                | **10LPP**    | **60.90** | **~4.38**      | **13.90 fps/W**   |
| Galaxy S8 (Snapdragon 835)                                   | 10LPE        | 38.90     | 3.79           | 10.26 fps/W       |
| LeEco Le Pro3 (Snapdragon 821)                               | 14LPP        | 33.04     | 4.18           | 7.90 fps/W        |
| Galaxy S7 (Snapdragon 820)                                   | 14LPP        | 30.98     | 3.98           | 7.78 fps/W        |
| Huawei Mate 10 (Kirin 970)                                   | 10FF         | 37.66     | 6.33           | 5.94 fps/W        |
| Galaxy S8 (Exynos 8895)                                      | 10LPE        | 42.49     | 7.35           | 5.78 fps/W        |
| Galaxy S7 (Exynos 8890)                                      | 14LPP        | 29.41     | 5.95           | 4.94 fps/W        |
| Meizu PRO 5 (Exynos 7420)                                    | 14LPE        | 14.45     | 3.47           | 4.16 fps/W        |
| Nexus 6P (Snapdragon 810 v2.1)                               | 20Soc        | 21.94     | 5.44           | 4.03 fps/W        |
| Huawei Mate 8 (Kirin 950)                                    | 16FF+        | 10.37     | 2.75           | 3.77 fps/W        |
| Huawei Mate 9 (Kirin 960)                                    | 16FFC        | 32.49     | 8.63           | 3.77 fps/W        |
| Huawei P9 (Kirin 955)                                        | 16FF+        | 10.59     | 2.98           | 3.55 fps/W        |

For Manhattan 3.1 the Snapdragon 845 had an active system power figure (Idle power subtracted from total platform power) of 4.38W. The excellent performance figure of the Adreno 630 alongside the reasonable power consumption puts the Snapdragon 845 well ahead at the top of our efficiency table, improving by up to 35% compared to the S835 Galaxy S8, with three generations of Adreno based SoC outmatching the latest ARM solutions. We’re aware of the demand for power figures on Apple’s latest SoCs but sadly we can’t tear down our review devices for battery power measurements and working on a solution. Given the A11’s thermal characteristics I’m expecting power usages more in line with the Exynos 8895 and Kirin 970 than the Snapdragon SoCs.

| GFXBench T-Rex Offscreen Power Efficiency (System Active Power) |              |            |                |                   |
| ------------------------------------------------------------ | ------------ | ---------- | -------------- | ----------------- |
|                                                              | Mfc. Process | FPS        | Avg. Power (W) | Perf/W Efficiency |
| Qualcomm QRD (Snapdragon 845)                                | **10LPP**    | **150.80** | **~4.02**      | **37.51 fps/W**   |
| Galaxy S8 (Snapdragon 835)                                   | 10LPE        | 108.20     | 3.45           | 31.31 fps/W       |
| LeEco Le Pro3 (Snapdragon 821)                               | 14LPP        | 94.97      | 3.91           | 24.26 fps/W       |
| Galaxy S7 (Snapdragon 820)                                   | 14LPP        | 90.59      | 4.18           | 21.67 fps/W       |
| Galaxy S8 (Exynos 8895)                                      | 10LPE        | 121.00     | 5.86           | 20.65 fps/W       |
| Galaxy S7 (Exynos 8890)                                      | 14LPP        | 87.00      | 4.70           | 18.51 fps/W       |
| Huawei Mate 10 (Kirin 970)                                   | 10FF         | 127.25     | 7.93           | 16.04 fps/W       |
| Meizu PRO 5 (Exynos 7420)                                    | 14LPE        | 55.67      | 3.83           | 14.54 fps/W       |
| Nexus 6P (Snapdragon 810 v2.1)                               | 20Soc        | 58.97      | 4.70           | 12.54 fps/W       |
| Huawei Mate 8 (Kirin 950)                                    | 16FF+        | 41.69      | 3.58           | 11.64 fps/W       |
| Huawei P9 (Kirin 955)                                        | 16FF+        | 40.42      | 3.68           | 10.98 fps/W       |
| Huawei Mate 9 (Kirin 960)                                    | 16FFC        | 99.16      | 9.51           | 10.42 fps/W       |

T-Rex stresses the GPU differently and we see slightly lower power consumption compared to Manhattan 3.1 ending up at 4W and showcasing an efficiency increase of 20% over the Snapdragon 835, again pointing towards more tangible changes in the ALU pipelines of the new architecture.

Overall the Adreno 630 more than delivers as it’s able to double-down on the Adreno 540’s efficiency advantage. Qualcomm current generations of SoCs are simply unmatched and the gap is so wide that I do not expect upcoming rival solutions to be able to catch up this year.



## irst Thoughts

Coming into 2018, Qualcomm is facing what we expect to be a busy and certainly competitive year for the company in the smartphone platform space. Iterating on the well-received Snapdragon 835 – and without the benefit of a new manufacturing node – is no easy task. All the while Apple has once again thrown down the gauntlet with their A11 SoC if one wants to argue about top tech, and even in the Android space Qualcomm isn’t the only high-end SoC vendor, as we await to see what Samsung’s [Exynos 9810](https://www.anandtech.com/show/12212/samsung-announces-new-exynos-9810-soc) and its new [Exynos M3](https://www.anandtech.com/show/12361/samsung-exynos-m3-architecture) CPU cores can achieve.

Still, it’s a challenge that Qualcomm should be prepared for, if not a bit unevenly. With a focus on architecture the company has been hard at work for the Snapdragon 845, and as a result while it’s very much a Qualcomm SoC, it’s also not just a rehash of Snapdragon 835. Both the CPU and GPU are seeing substantial overhauls, not to mention smaller upgrades across the board for everything from the modem to the audio codec. And while Qualcomm rightfully argues that there’s more to a platform than just raw compute performance – that all of these pieces contribute to the overall user experience – they remain vital to device performance and battery life. Which is to say that Qualcomm is innovating where they need to in order to continue improving the heart of many flagship 2018 Android smartphones.

[![img](https://images.anandtech.com/doci/12420/845-1_575px.jpg)](https://images.anandtech.com/doci/12420/845-1.jpg)

Overall the Snapdragon 845’s system performance is a mixed bag. We had higher expectations from the new CPU changes, but it seems we’ve only gotten incremental improvements. Web workloads seem to be the Snapdragon 845’s forte as that’s where we see the largest improvements. ARM is working on a long awaited overhaul as the Austin team is busy with a brand new microarchitecture which should bring larger generational improvements, but alas only with the next generation of SoCs in 2019.  For many flagship Android phones, 2018 should remain another conservative year and we should not have too high expectations.

But with that said, whatever Qualcomm doesn’t quite bring to the table with their CPU, they more than make up on the GPU side of matters. Qualcomm’s new Adreno 630 GPU easily impresses and widens the gap to the nearest competition. Compared to the Exynos 8895 and Kirin 970 I expect the Snapdragon 845 to have a 3.5-5x PPA advantage when it comes to the GPU. The competition should be worried as it’s no longer feasible to compensate the power efficiency disadvantage with larger GPU configurations and there is need for more radical change to keep up with Qualcomm.

[![img](https://images.anandtech.com/doci/12420/qrd2_575px.jpg)](https://images.anandtech.com/doci/12420/qrd2.jpg)

And while we weren’t able to test for system power efficiency improvements for this preview, we weren’t left empty-handed and were able to quickly do a CPU power virus on the QRD845. The results there have turned out promising, with 1W per-core and slightly under 4W for four-core power usage, which are very much in line with the Snapdragon 835. The new system cache and GPU improvements should also noticeably improve SoC – and in turn device – efficiency, so I’m expecting that 2018’s Snapdragon 845 powered devices to showcase excellent battery life.

What remains to be seen then is how this translates into shipping products. Previous Qualcomm device previews have turned out to be rather accurate, but handset manufacturers have countless ways to customize their phones, both for good and for bad. What we can say for now is that it looks like Qualcomm has once again delivered its handset partners a solid SoC from which to build their flagship phones. So we’re eager to see what retail phones can deliver, and ultimately how the Snapdragon 845 fits into the overall market for 2018 Android flagship smartphones.
