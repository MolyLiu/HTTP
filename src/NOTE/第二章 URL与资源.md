#第二章 URL与资源
URL就是因特网资源的标准化名称。

URL指向一条电子信息片段，告诉你它们位于何处，以及如何与之进行交互。
##2.1 浏览因特网资源
URL是浏览器寻找信息时所需的资源**位置**。

URL分为以下三部分：

1. URL的第一部分被称为方案。说明了访问资源所使用的协议类型，告知客户端**怎么样**访问资源。
2. 第二部分指的是服务器的位置。这部分告知客户端资源位于**何处**
3. 第三部分是资源路径，路径说明了，请求的是服务器上**哪个**特定的本地资源
##2.2 URL语法
大部分URL都是遵循通用的URL语法的，大多数URL方案的URL语言都是简历在由这9部分构成的通用格式上。

    <scheme>://<user>:<password>@<host>:<post>/<path>;<params>?<query>#<frag>
几乎没有哪个URL包含了所有这些组件。URL**最重要**的部分是：方案，主机，路径。  
###2.2.1 方案——使用什么协议
方案实际上是规定如何访问资源的主要标识符，会负责告诉解析URL的应用程序使用的是何种**协议**。

方案名与大小写无关。
###2.2.2 主机和端口
主机组件标识了因特网上能够访问资源的宿主机器。

端口组件标识了服务器正在的网络端口。
###2.2.3 用户名和密码
很多服务器都要求输入用户名和密码才会允许用户访问数据。FTP服务器就是这样一个常见的实例。
###2.2.4 路径
URL路径组件说明了资源位于服务器的什么地方。
###2.2.5 参数
除了以上介绍的部分，很多协议还需要更多的信息才能进行工作。

（太常见了）
###2.2.6 查询字符串
很多资源，比如数据库服务，都是可以通过提问题或进行查询来缩小所请求资源类型范围的。
###2.2.7 片段
为了引用部分资源，或者资源的一个片段，URL支持只适用片段来表示一个资源内部的片段。

HTTP服务器通常处理整个对象。浏览器从服务器获得了**整个**资源后，会根据片段来显示你感兴趣的那部分资源。
##2.3URL快捷方式
Web客户端可以理解并使用几种URL快捷方式。
###2.3.1 相对URL
URL有两种方式：绝对的和相对的。

绝对URL：URL中包含访问资源所需要的全部信息。

相对URL：URL是不完整的。要从相对URL中获取访问资源所需的全部信息，就必须相对于另一个被称之为基础的URL进行解析。
###2.3.2自动扩展URL
用户不需要输入完整的URL，浏览器就会自动扩展。

“自动扩展”特性有以下两种方式：

1. 主机名扩展：在主机名扩展中，浏览器通常可以在没有帮助的情况下，将你输入的主机名自动扩展为完整的主机名。（比如，在地址栏中输入baidu）
2. 历史扩展：浏览器用来节省用户输入URL时间的另一种技巧是，将以前用户访问的URL历史存储起来。

##2.4 各种更令人头疼的字符
URL是可移植的。

因为URL是统一地命名因特网上的所有资源，这些资源会通过不同协议进行传输，而不同协议之间也会使用不同的机制。所以设计URL，要使其能够通过任意因特网协议并且**安全传输**。

为了安全传输，URL只能使用一些相对较小的，通用的安全字母表中的字符，除此之外，URL是希望可以供人类阅读的。最重要的是URL必须是完整的，因此就会有一种转义机制，能够将不安全的字符编码为安全字符，在进行传输。
###2.4.1 URL字符
转义序列集成US-ASCII字符集，通过转义序列，就可以用US-ASCII字符集的有限子集对任意字符值或数据进行编码了，这样就实现了可移植性和完整性。
###2.4.2 编码机制
为了避免安全字符集带来的限制，人们设计了一种编码机制，用来在URL中表示各种不安全的字符。
###2.4.3 字符限制
在URL中，有几个字符被保留起来，有着特殊的含义。 不做详解。
##2.5方案的世界
常见的几种方案：http，https,mailto,ftp,rtsp,rtspu,file,news,telnet.不做详解。
