[06:56PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821185615) - Xilinx has several talks this year at Hot Chips, and aside from the ACAP earlier in the day, the talk about their Deep Neural Network processor also looks interesting. The talk is set to start at 4pm PT / 11pm UTC.

[![img](https://images.anandtech.com/doci/13256/15348922324551811486208_575px.jpg)](https://images.anandtech.com/doci/13256/15348922324551811486208.jpg)

[07:01PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190123) - Xilinx Inference Engine - DNN Processor for Xilinx FPGA and software tools

[07:02PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190212) - No FPGA expertise required

[07:02PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190220) - Low latency, high throughput

[07:02PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190248) - All work shown was performed on Ultrascale+ VU9P

[![img](https://images.anandtech.com/doci/13256/1534892587038977485752_575px.jpg)](https://images.anandtech.com/doci/13256/1534892587038977485752.jpg)

[07:03PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190349) - FPGA maps well to Deep Learning

[07:04PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190402) - Flexible on-chip memory, high bandwidth, multiple acess ports

[07:04PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190411) - Near memory compute, for power 

[![img](https://images.anandtech.com/doci/13256/15348925965541163574717_575px.jpg)](https://images.anandtech.com/doci/13256/15348925965541163574717.jpg)

[07:04PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190452) - Can do variable data types

[07:05PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190500) - INT2 to FP32 and beyond

[07:05PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190509) - Binary / Ternary

[07:05PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190518) - Sparse friendly compute

[07:05PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190545) - Uses a full scale or memory

[![img](https://images.anandtech.com/doci/13256/1534892683417664981217_575px.jpg)](https://images.anandtech.com/doci/13256/1534892683417664981217.jpg)

[07:07PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190750) - Configurable overlay processor

[![img](https://images.anandtech.com/doci/13256/1534892829488563332217_575px.jpg)](https://images.anandtech.com/doci/13256/1534892829488563332217.jpg)

[07:08PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190820) - DNN specific instruction set

[07:08PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190825) - Any network, any image size

[07:08PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190832) - high frequency and high compute

[07:08PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190847) - Compile and run new networks

[07:09PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190917) - Systolic array is a 2D channel parallel datapath and distributed weight buffers

[![img](https://images.anandtech.com/doci/13256/1534892877896493956763_575px.jpg)](https://images.anandtech.com/doci/13256/1534892877896493956763.jpg)

[07:09PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190944) - All the processing elements are mapped on the DSP blocks with weight buffers

[07:09PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190954) - The distributed RAMs are close to the weight blocks as a cache

[07:09PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821190958) - feed it to the DSP block

[07:10PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191003) - Ping pong architecture

[07:10PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191014) - Get the weights from DDR in ping and use on pong

[07:10PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191025) - DSP block has been optimized for INT16 and INT8

[07:10PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191036) - INT8 maps as 2 Multiply-Add on each block

[07:10PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191052) - Fun Multiply Accumualte at 2x clock, memory access at clock speed

[07:11PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191100) - Cascaded along the columns

[07:11PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191114) - Columns mapped to output maps

[07:11PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191139) - Microarchitecture optimized for underlying Ultrascale+ FPGA Fabric

[07:11PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191151) - Tensor memory next to systolic array

[07:12PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191204) - Channel parallel concurrent access

[07:12PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191216) - Mapped to UltraRAMs

[07:14PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191432) - Memory utilization is optimized as well

[07:15PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191504) - compiler schedules data reuse 

[![img](https://images.anandtech.com/doci/13256/15348929710581907502318_575px.jpg)](https://images.anandtech.com/doci/13256/15348929710581907502318.jpg)

[![img](https://images.anandtech.com/doci/13256/1534893293776921454792_575px.jpg)](https://images.anandtech.com/doci/13256/1534893293776921454792.jpg)

[07:15PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191540) - Output through memory addresses get concatinated for input to next layer 

[![img](https://images.anandtech.com/doci/13256/15348933182291945104640_575px.jpg)](https://images.anandtech.com/doci/13256/15348933182291945104640.jpg)

[07:15PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191555) - Full middleware tools and API

[07:16PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191603) - Caffe, Tensorflow and mxnet

[07:16PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191632) - Give the trained model and the weights, convert into Xilinx Graph, does few optimizations, then goes to the compiler to run the network on the DNN on the FPGA

[07:16PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191649) - Also have a quantizer, done offline

[07:17PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191704) - Runtime manages all the communication between CPU and FPGA

[![img](https://images.anandtech.com/doci/13256/1534893346797384182193_575px.jpg)](https://images.anandtech.com/doci/13256/1534893346797384182193.jpg)

[07:17PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191725) - Compiler does graph partitioning and optimizing

[07:17PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191731) - one-time loading of sub-graph instructions

[07:17PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191750) - Splits up data depending on chips available

[07:18PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191813) - Fusing of operations into pipeline stages

[![img](https://images.anandtech.com/doci/13256/1534893471501217670486_575px.jpg)](https://images.anandtech.com/doci/13256/1534893471501217670486.jpg)

[07:18PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191827) - access activations only once, into pipelined operators with no RAM access

[![img](https://images.anandtech.com/doci/13256/1534893509899189346605_575px.jpg)](https://images.anandtech.com/doci/13256/1534893509899189346605.jpg)

[07:18PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191853) - Has an amount of Instruction Level Parallelism where possible

[07:19PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191900) - Can schedule parallel instructions

[07:19PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191939) - Automatic Intra-Layer Tiling when map size exceeds on chip memory

[07:19PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821191944) - any feature map size

[![img](https://images.anandtech.com/doci/13256/15348935224911195656436_575px.jpg)](https://images.anandtech.com/doci/13256/15348935224911195656436.jpg)

[07:20PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192014) - Hardware does the tiling automatically

[![img](https://images.anandtech.com/doci/13256/153489360602580684205_575px.jpg)](https://images.anandtech.com/doci/13256/153489360602580684205.jpg)

[07:20PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192055) - Key functions: INT8 and INT16

[07:21PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192103) - Supports square and rectangular sizes

[07:21PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192110) - Various networks

[![img](https://images.anandtech.com/doci/13256/15348936433241189656548_575px.jpg)](https://images.anandtech.com/doci/13256/15348936433241189656548.jpg)

[07:22PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192206) - 96x16 PEs, 1 in each SLR

[07:22PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192223) - 90% of the maximum device frequency

[![img](https://images.anandtech.com/doci/13256/153489369342897868976_575px.jpg)](https://images.anandtech.com/doci/13256/153489369342897868976.jpg)

[07:23PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192300) - Launching the IP as a product at the Xilinx Developer Forum, Oct 1st

[07:23PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192306) - Also custom DL pipelining

[07:23PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192332) - All Pipelines can be running the same networks or different networks

[07:23PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192344) - Or leading data from one to another

[![img](https://images.anandtech.com/doci/13256/15348937601831432319034_575px.jpg)](https://images.anandtech.com/doci/13256/15348937601831432319034.jpg)

[07:24PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192439) - Deploy in cloud or on PCIe cards

[![img](https://images.anandtech.com/doci/13256/1534893851358808949849_575px.jpg)](https://images.anandtech.com/doci/13256/1534893851358808949849.jpg)

[07:24PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192447) - No FPGA experience needed

[07:25PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192523) - Xilinx Dev Forum - Silicon Valley, Beijing, Frankfurt

[07:25PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192528) - Q&A Time

[07:26PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192651) - Q: You showed 90% of Fmax with 50% of LUTs. Can you add another application in the spare area? A: Yes.But you are using 92% of the UltraRAMs, so it will have to avoid those. Might want to only map one or two engines, not all three

[07:29PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821192932) - Q: A lot of research in new topologies. How do you support these new features? A: If you have new features that don't map, you can map into the FPGA. Or run on CPU.

[07:30PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821193029) - Q: Today Xilinx announced ACAP. What is perforamnce? A: This xDNN is about 16nm. We will make it mapped on the ACAP as well in time. Performance will increase.

[07:30PM EDT](http://www.anandtech.com/show/13256/hot-chips-2018-xilinx-dnn-processors-live-blog#post0821193046) - That's a wrap. 30 minute break, and then the server talks.