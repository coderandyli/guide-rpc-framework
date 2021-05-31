# 项目骨架
```
.
├── config                                                                          -- 编码规范检测
│   ├── checkstyle.xml
│   └── git-hooks                                                               -- git钩子
│       └── pre-commit
├── docs                                                                            -- 文档 
├── example-client                                                                  -- 示例-客户端
│   ├── pom.xml
│   └── src
│       └── main
│           ├── java
│           │   └── github
│           │       └── javaguide
│           │           ├── HelloController.java
│           │           ├── NettyClientMain.java
│           │           └── SocketClientMain.java
│           └── resources
│               └── rpc.properties
├── example-server                                                                  -- 示例-服务端
│   ├── pom.xml
│   └── src
│       └── main
│           ├── java
│           │   ├── NettyServerMain.java
│           │   ├── SocketServerMain.java
│           │   └── github
│           │       └── javaguide
│           │           └── serviceimpl
│           │               ├── HelloServiceImpl.java
│           │               └── HelloServiceImpl2.java
│           └── resources
│               └── rpc.properties
├── hello-service-api                                                              -- 存放服务接口
│   ├── pom.xml
│   └── src
│       └── main
│           └── java
│               └── github
│                   └── javaguide
│                       ├── Hello.java
│                       └── HelloService.java
├── images
├── init.sh
├── pom.xml
├── rpc-framework-common                                                          -- 存放实体类及工具类 
│   ├── pom.xml
│   └── src
│       └── main
│           └── java
│               └── github
│                   └── javaguide
│                       ├── enums
│                       │   ├── CompressTypeEnum.java
│                       │   ├── RpcConfigEnum.java
│                       │   ├── RpcErrorMessageEnum.java
│                       │   ├── RpcResponseCodeEnum.java
│                       │   └── SerializationTypeEnum.java
│                       ├── exception
│                       │   ├── RpcException.java
│                       │   └── SerializeException.java
│                       ├── extension
│                       │   ├── ExtensionLoader.java
│                       │   ├── Holder.java
│                       │   └── SPI.java
│                       ├── factory
│                       │   └── SingletonFactory.java
│                       └── utils
│                           ├── PropertiesFileUtil.java
│                           ├── RuntimeUtil.java
│                           └── concurrent
│                               └── threadpool
│                                   ├── CustomThreadPoolConfig.java
│                                   └── ThreadPoolFactoryUtils.java
└── rpc-framework-simple                                                        -- RPC的核心实现 
    ├── README.md
    ├── pom.xml
    └── src
        ├── main
        │   ├── java
        │   │   └── github
        │   │       └── javaguide
        │   │           ├── annotation-- 
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
        │   │           ├── provider                                           -- 服务提供
        │   │           │   ├── ServiceProvider.java
        │   │           │   └── impl
        │   │           │       └── ZkServiceProviderImpl.java
        │   │           ├── proxy
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
        │   │           │       │   ├── codec
        │   │           │       │   └── server
        │   │           │       └── socket
        │   │           │           ├── SocketRpcClient.java
        │   │           │           ├── SocketRpcRequestHandlerRunnable.java
        │   │           │           └── SocketRpcServer.java
        │   │           ├── serialize
        │   │           │   ├── Serializer.java
        │   │           │   ├── kyro
        │   │           │   │   └── KryoSerializer.java
        │   │           │   └── protostuff
        │   │           │       └── ProtostuffSerializer.java
        │   │           └── spring
        │   │               ├── CustomScanner.java
        │   │               ├── CustomScannerRegistrar.java
        │   │               └── SpringBeanPostProcessor.java
        │   └── resources
        │       └── META-INF
        │           └── extensions
        │               ├── github.javaguide.compress.compress
        │               ├── github.javaguide.loadbalance.LoadBalance
        │               ├── github.javaguide.registry.ServiceDiscovery
        │               ├── github.javaguide.registry.ServiceRegistry
        │               ├── github.javaguide.remoting.transport.RpcRequestTransport
        │               └── github.javaguide.serialize.Serializer
```