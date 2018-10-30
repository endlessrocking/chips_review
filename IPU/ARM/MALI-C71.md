![img](https://images.anandtech.com/doci/11293/bdgrm_678x452.png)





ARM’s success in the CPU IP field has and remains the cornerstone of the company, but it has not been a company that sits idle. Over the years – and especially in the smartphone boom of the last decade – ARM has been investing their profits into expanding their business into other fields, both software and hardware. Now this morning the company is making their big move in the [Image Signal Processing](http://www.anandtech.com/show/6777/understanding-camera-optics-smartphone-camera-trends/4) (ISP) market, taking the wraps off of their first in-house ISP design: the Mali-C71.

ARM’s foray into the ISP market has been in the works for a bit now, and comes as a product of one of their 2016 acquisitions: imaging technology developer Apical. Picked up by ARM just under a year ago, Apical specialized in ISPs and computer vision technology, two growing markets for processor IP and two areas that meshed well with ARM’s own product plans, especially in the case of computer vision. With ARM further investing in their new imaging division to make Apical’s previous roadmap a reality, today the company is announcing the first imaging product developed and released as part of ARM.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-03b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-03b.png)



While there are a significant number of ISPs in the market – it is a growing field, but a highly competitive one – what makes the Mali-C71 particularly notable is how aggressively ARM is going after the high-end of the market. Immediately swinging for the fences, ARM’s first in-house ISP is designed specifically for Advanced Driver Assistance Systems (ADAS) market. ADAS a lucrative market that the company is expecting to grow quickly, but also one with extensive reliability and safety requirements.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-05b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-05b.png)

ARM expectation – and indeed much of the industry’s – is that cars are going to continue to have larger and larger numbers of processors and other electronics integrated into them. And while self-driving cars are obviously the end goal of this process, consumer products are still many years off. So ARM’s more immediate focus is on processor designs that would improve Level 1 and Level 2 driver assistance features, which brings us back to ADAS. The company is expecting the number of cameras in a given car to double (or more), and they want to be the vendor developing the processor IP that consumes all of that camera information.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-10b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-10b.png)

The Mali-C71 then is the first of the company’s Mali-C series of ISPs, designed specifically for this task. From a feature standpoint it’s a high-end ISP, supporting 4 real-time (streaming) camera inputs and another 16 non-streaming inputs. Altogether the ISP can stream/process 1.2GPixels/second, about twice as many inputs and twice as much data as predecessor Apcial’s contemporary smartphone ISPs. And if that’s not enough, then multiple ISPs can be setup to work in tandem to handle more camera inputs and more overall pixels. The ultimate goal of the Mali-C71 being to efficiently and most appropriately processing imaging data so that it can be passed on to the driver and to other processors for true computer vision processing.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-09b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-09b.png)

Raw specifications aside, however, a bigger part of ARM’s pitch to SoC developers and automakers is Mali-C71’s feature set, and this is where Mali-C71 is distinctly an ADAS-focused ISP. ARM is heavily focusing on both dynamic range and reliability features. The former being extremely useful to ADAS applications, and the latter being critical to getting anything on the road.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-11b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-11b.png)

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-12b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-12b.png)

In the case of dynamic range, the Mali-C71 can handle a rather massive 24 stops of camera range via multiple exposures. Which from a more practical perspective means that it can process 16.8 million (2^24) light intensity levels. This is over twice as many stops as most smartphone ISPs and is even better than DSLRs, but more importantly it’s critical to ARM’s ADAS goals. Because cars need to see exceptionally well in the dark as well as in the light – and because the ultimate goal for many in the industry is to do all-visual (no LIDAR/RADAR) self-driving – C71 needs to support enough stops to capture and map a very large dynamic range.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-13b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-13b.png)

The goal, in some ways, is to exceed human vision. Humans can see a rather wide range of intensities, but as anyone who’s driven at night can attest, we can’t see bright and dark at the same time. Supporting a large number of stops means that not only can ADAS systems see dark and light details at the same time – allowing computer vision processes to better understand what they’re seeing – but it can also quickly be tone mapped to something that can be displayed on a non-HDR (or at least not quite as HDR) automotive display for the drive.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-14b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-14b.png)

The back-half of the feature set for the Mali-C71 then is focused on the reliability side of the equation, so that CV systems and ultimately automakers can trust what the C71 is reporting. A big part of this is ASIL D compliance, which is the most risk-averse level under the ASIL scheme. This means that as a processor the Mali-C71 needs numerous safeguards such as self-testing and numerous fault-detection circuits, but it also needs safeguards in place with respect to imaging. The latter comes in the form of an additional data layer the ISP provides, the consistency plane. A form of sorts of image metadata, the consistency plane is responsible for several tasks, including informing consuming processors about motion and whether any unusual data (e.g. a bright pixel) is accurate or if it’s an erroneous hot pixel. In the case of hot pixels it’s important to detect them and pass that information on to computer vision systems so that they can determine if they need to act on the bright pixel they’re seeing or if it’s something that can be ignored.

Moving on, while the focus of ARM’s announcement is on the ISP IP itself, the company is offering more than just hardware. Mali-C71 is intended to be a combined hardware + software product, with ARM also including a full reference software suite to go with the ISP. Customers will still want to tune the system to their specific needs – and ARM provides those tools as well – but it means that customers can hit the ground running with ASIL-compliant software as well.

[![img](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-15b_575px.png)](https://images.anandtech.com/doci/11293/mali-c71-launch-deck_final-deck-%281%29-15b.png)

Finally, although ARM isn’t naming specific partners, they have stated that the lead partner for Mali-C71 already has working sample silicon. Other partners are farther back at the design or licensing stage. Automotive electronics have a significant lag period in development – the hardware needs to be certified, and then it needs to continue to ship for a number of years – so unlike consumer gear, Mali-C71 is a long-term product for ARM’s chip partners and the eventual automaker customers. Even after chip designers adopt it and get it into shipping chips, it will likely be years until it finally shows up in retail cars, which highlights just how long of a game ARM is playing here by getting into ISPs for ADAS.