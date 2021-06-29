0000 此节为介绍node-template代码

0020 项目分为三个大部分node,pallet,runtime。用它可以构建一个最小化的区块链系统。

0055 node部分介绍，大多数不是在链上的底层操作。如网络，共识，transaction pool都是放到node里。  
0140 command.rs  
0233 service.rs node中最重要的部分代码。用来一步一步创建整个节点的所有组件。

0822 runtime介绍，构建链上的部分。链上逻辑会分为很多pallet，runtime的作用就是把这些pallet组合在一起，编译成一个wasm文件，作为链上运行的逻辑定义。  
1019 最底层的pallet frame_system  
1121 最重要的宏construct_runtime!  
1331 runtime_apis 通过调用某个pallet的某个方法来实现某个api。

1343 pallet介绍  
1355 3.0介绍，之前过程宏，现在属性宏。最大区别在于属性宏更接近于原生语法也更容易理解。这节课主要讲3.0，但会稍微介绍2.0  
1518 2.0介绍  
1730 3.0写法介绍  
2250 mock.rs介绍，写了pallet后做测试。  
2537 test.rs介绍

