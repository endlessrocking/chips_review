Hot Chips 2018: Arm's Machine Learning Core Live Blog



![img](https://images.anandtech.com/doci/13253/Logo%20ARM%20ML_678x452.jpg)





[04:57PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821165715) - Arm officially announced Project Trillium earlier this year, as a way to bring machine learning to the Arm ecosystem. As part of the trade show today, we have a presentation where Arm is going to talk about its first machine learning core. The talk is set to start at 2pm PT / 9pm UTC.

[![img](https://images.anandtech.com/doci/13253/15348852382731610879263_575px.jpg)](https://images.anandtech.com/doci/13253/15348852382731610879263.jpg)

[05:01PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170146) - Combined effort of large team

[05:01PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170154) - 150+ people

[05:02PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170236) - Arm works with partners across many segments. Without fail, all those markets want machine learning acceleration

[05:02PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170251) - Need to come up with a fundamental tech that can be used for many different segments

[05:03PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170311) - ML processor focused for Neural Networks

[![img](https://images.anandtech.com/doci/13253/15348852536851125230468_575px.jpg)](https://images.anandtech.com/doci/13253/15348852536851125230468.jpg)

[05:03PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170336) - Optimized ground up architecture

[05:03PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170347) - open source stack for easy deployment

[05:03PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170359) - First design targets mobile with derivatives for additional segments

[![img](https://images.anandtech.com/doci/13253/15348854878391154418878_575px.jpg)](https://images.anandtech.com/doci/13253/15348854878391154418878.jpg)

[05:05PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170515) - Main component is the Machine Learning Processor. Biggest block is SRAM

[05:05PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170529) - 16 compute engines per ML Proc

[05:05PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170539) - 4 TOP/s of convolution at 1 GHz

[05:05PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170550) - Targeting 3 TOP/W in 7nm and 2.5mm2

[05:06PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170600) - INT8 support, support for NNAPI

[05:06PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170609) - Optimized for CNN/RNN

[05:06PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170626) - Support 16-bit, in case pixels are coming

[05:06PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170636) - 8-bit is 4x perf over 16-bit

[05:07PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170724) - Need to get four things right

[![img](https://images.anandtech.com/doci/13253/1534885498602217152631_575px.jpg)](https://images.anandtech.com/doci/13253/1534885498602217152631.jpg)

[05:08PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170814) - Static Scheduling, Efficient Convolutions

[05:08PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170838) - CNNs are static analyzable. So you can optimize for deterministic data with stuff laid out in memory ahead of time

[05:08PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170858) - Creates command stream for different parts in the processor

[05:09PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170929) - Control Unit takes command stream

[![img](https://images.anandtech.com/doci/13253/15348856791921725132017_575px.jpg)](https://images.anandtech.com/doci/13253/15348856791921725132017.jpg)

[05:09PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821170954) - No caches, simplified flow control. Simplified hardware (co-design with compiler). Predictable performance

[05:10PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171039) - Compiler needs to know the details of the core, e.g. SRAM size

[05:11PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171132) - Underlying requirement of high-throughput dot products are worth optimizing for

[05:12PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171202) - Output feature maps are interleaved across compute engines

[![img](https://images.anandtech.com/doci/13253/1534885809594844161274_575px.jpg)](https://images.anandtech.com/doci/13253/1534885809594844161274.jpg)

[05:12PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171215) - So 16 engines = 16 output feature maps

[05:12PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171242) - MAC Engine: 8 x 16-bit wide dot products per cycle

[05:13PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171305) - Each engine is 2*8*16 = 256 ops/cycle

[![img](https://images.anandtech.com/doci/13253/15348859004632055788028_575px.jpg)](https://images.anandtech.com/doci/13253/15348859004632055788028.jpg)

[05:13PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171315) - 32b accumulators, 4.1 TOPs @ 1 GHz

[05:13PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171335) - Gate for zeros to save power - 50% power reductions

[05:13PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171357) - Keep inputs to datapaths stable to save energy

[![img](https://images.anandtech.com/doci/13253/1534885945576335970328_575px.jpg)](https://images.anandtech.com/doci/13253/1534885945576335970328.jpg)

[05:14PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171420) - Also have broadcast network

[![img](https://images.anandtech.com/doci/13253/1534886043918214836618_575px.jpg)](https://images.anandtech.com/doci/13253/1534886043918214836618.jpg)

[05:14PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171447) - Creates tensor block of activations that is broadcast to all the MAC engines

[05:15PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171529) - when final result the 32b values are scaled back to 8b and sent to the programmable layer engine

[![img](https://images.anandtech.com/doci/13253/1534886066701393536391_575px.jpg)](https://images.anandtech.com/doci/13253/1534886066701393536391.jpg)

[![img](https://images.anandtech.com/doci/13253/1534886103930319461103_575px.jpg)](https://images.anandtech.com/doci/13253/1534886103930319461103.jpg)

[05:15PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171546) - POP IP for Mac Engine for 16nm and 7nm

[05:16PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171607) - Custom physical design with 40% area reduction and 10-20% power improvements

[![img](https://images.anandtech.com/doci/13253/15348861362701645291173_575px.jpg)](https://images.anandtech.com/doci/13253/15348861362701645291173.jpg)

[05:16PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171634) - DRAM power can be up to 50% without bandwidth saving

[05:16PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171652) - use weight compression, activation compression, and tiling, to save DRAM power

[05:17PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171709) - Spend dedicated silicon on compression is essential

[05:18PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171819) - Histogram of 8x8 blocks in Inception V3 shows key ML matrixes

[05:18PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171840) - Develop lossless compression for the popular 8x8 blocks

[![img](https://images.anandtech.com/doci/13253/1534886179041572347428_575px.jpg)](https://images.anandtech.com/doci/13253/1534886179041572347428.jpg)

[05:19PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171905) - 3.3x compression over standard implementation

[05:19PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171937) - When training, many training weights taper down to zero

[05:19PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821171959) - Can force the weights to zero with no change in accuracy but offers better compression

[05:20PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172021) - This allows for weight compression and 'pruning'

[05:20PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172036) - Support a compression format to get the zeroes out

[![img](https://images.anandtech.com/doci/13253/15348862663691455037306_575px.jpg)](https://images.anandtech.com/doci/13253/15348862663691455037306.jpg)

[05:20PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172046) - Take the remaining non-zero can be clamped / normalized

[05:20PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172050) - All happens in hardware

[05:21PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172109) - Weights stay compressed until read from internal SRAM

[05:21PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172136) - Very model dependent 

[05:21PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172142) - Tiling

[![img](https://images.anandtech.com/doci/13253/15348863521781215566868_575px.jpg)](https://images.anandtech.com/doci/13253/15348863521781215566868.jpg)

[05:22PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172203) - Tricks that the compiler can use to reduce bandwidth by using the SRAM

[05:22PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172241) - Possible due to static scheduling

[![img](https://images.anandtech.com/doci/13253/1534886509580794786755_575px.jpg)](https://images.anandtech.com/doci/13253/1534886509580794786755.jpg)

[05:23PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172307) - State of the art in tiling is still evolving

[![img](https://images.anandtech.com/doci/13253/1534886572843584668155_575px.jpg)](https://images.anandtech.com/doci/13253/1534886572843584668155.jpg)

[05:23PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172327) - Programmable Layer Engine helps with future-proofing

[![img](https://images.anandtech.com/doci/13253/1534886594928450446973_575px.jpg)](https://images.anandtech.com/doci/13253/1534886594928450446973.jpg)

[05:24PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172404) - Use Arm M-class CPU and extended it with vector extensions for neural networks

[![img](https://images.anandtech.com/doci/13253/15348866236991473145085_575px.jpg)](https://images.anandtech.com/doci/13253/15348866236991473145085.jpg)

[05:24PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172445) - Engine can manipulate SRAM data

[05:25PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172519) - Designed to scale in engines 

[05:25PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172530) - Designed to scale with MAC engine throughput

[![img](https://images.anandtech.com/doci/13253/15348866529211708926372_575px.jpg)](https://images.anandtech.com/doci/13253/15348866529211708926372.jpg)

[05:25PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172543) - Designed to scale with Machine Learning Processors for multiple workloads

[05:26PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172614) - Q&A time

[05:27PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172748) - Q: If there's one M-series core in the engine, is there 16 per MLP? A: Yes

[05:28PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172834) - Q: What about lower than 8-bit? A: Industry momentum is around 8-bit. We're looking into lower bit levels, but that could be in the future

[05:28PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172850) - Q: When will it be available for licencing ? A: Later this year

[05:29PM EDT](http://www.anandtech.com/show/13253/hot-chips-2018-arm-machine-learning-core-live-blog#post0821172920) - That's a wrap. Come back at 3pm for a talk on Tachyum