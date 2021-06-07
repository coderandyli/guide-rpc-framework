[toc]
# 项目骨架
## simple
```
.
├── config                                                                                    -- 编码规范检测(git commit前进行检测)
├── docs                                                                                      -- 文档 
├── example-client                                                                            -- 示例-客户端
├── example-server                                                                             -- 示例-服务端
├── hello-service-api                                                                         -- 存放服务接口
│   ├── pom.xml
│   └── src.main.java.github.javaguide
│                       ├── Hello.java
│                       └── HelloService.java
├── images
├── rpc-framework-common                                                                     -- 存放实体类及工具类 
│   └── src.main.java.github.javaguide
│                       ├── enums
│                       ├── exception
│                       ├── extension
│                       ├── factory
│                       └── utils
└── rpc-framework-simple                                                                     -- RPC的核心实现 
    └── src.main.java.github.javaguide
        │   │           ├── annotation 
        │   │           │   ├── RpcReference.java
        │   │           │   ├── RpcScan.java
        │   │           │   └── RpcService.java
        │   │           ├── compress
        │   │           │   ├── Compress.java
        │   │           │   └── gzip
        │   │           │       └── GzipCompress.java
        │   │           ├── config
        │   │           │   ├── CustomShutdownHook.java
        │   │           │   └── RpcServiceConfig.java
        │   │           ├── loadbalance                                         -- 服务发现负载均衡
        │   │           │   ├── AbstractLoadBalance.java
        │   │           │   ├── LoadBalance.java
        │   │           │   └── loadbalancer    
        │   │           │       ├── ConsistentHashLoadBalance.java
        │   │           │       └── RandomLoadBalance.java
        │   │           ├── provider                                            -- 服务提供者(内部调用ServiceRegistry)
        │   │           │   ├── ServiceProvider.java
        │   │           │   └── impl
        │   │           │       └── ZkServiceProviderImpl.java
        │   │           ├── proxy                                               -- rpc client 代理（基于动态代理实现） 
        │   │           │   └── RpcClientProxy.java
        │   │           ├── registry                                            -- 服务注册与发现
        │   │           │   ├── ServiceDiscovery.java
        │   │           │   ├── ServiceRegistry.java
        │   │           │   └── zk
        │   │           │       ├── ZkServiceDiscoveryImpl.java
        │   │           │       ├── ZkServiceRegistryImpl.java
        │   │           │       └── util
        │   │           │           └── CuratorUtils.java
        │   │           ├── remoting                                            
        │   │           │   ├── constants
        │   │           │   │   └── RpcConstants.java
        │   │           │   ├── dto
        │   │           │   │   ├── RpcMessage.java
        │   │           │   │   ├── RpcRequest.java
        │   │           │   │   └── RpcResponse.java
        │   │           │   ├── handler
        │   │           │   │   └── RpcRequestHandler.java
        │   │           │   └── transport
        │   │           │       ├── RpcRequestTransport.java
        │   │           │       ├── netty
        │   │           │       │   ├── client
        │   │           │       │   │   ├── ChannelProvider.class
        │   │           │       │   │   ├── NettyRpcClient$1.class
        │   │           │       │   │   ├── NettyRpcClient.class
        │   │           │       │   │   ├── NettyRpcClientHandler.class
        │   │           │       │   │   └── UnprocessedRequests.class
        │   │           │       │   ├── codec
        │   │           │       │   │   ├── RpcMessageDecoder.class
        │   │           │       │   │   └── RpcMessageEncoder.class
        │   │           │       │   └── server
        │   │           │       │       ├── NettyRpcServer$1.class
        │   │           │       │       ├── NettyRpcServer.class
        │   │           │       │       └── NettyRpcServerHandler.class    
        │   │           │       └── socket
        │   │           │           ├── SocketRpcClient.java
        │   │           │           ├── SocketRpcRequestHandlerRunnable.java
        │   │           │           └── SocketRpcServer.java
        │   │           ├── serialize                                              -- 序列化
        │   │           │   ├── Serializer.java
        │   │           │   ├── kyro
        │   │           │   │   └── KryoSerializer.java
        │   │           │   └── protostuff
        │   │           │       └── ProtostuffSerializer.java
        │   │           └── spring                                                 -- 
        │   │               ├── CustomScanner.java
        │   │               ├── CustomScannerRegistrar.java
        │   │               └── SpringBeanPostProcessor.java
```