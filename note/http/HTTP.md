# HTTP

### GET和POST的区别

##### 浏览器的GET和POST

-  一般会**泛泛的说**“GET请求没有body，只有url，请求数据放在url的querystring中；POST请求的数据在body中“。但这种情况**仅限于浏览器发请求的场景**。

##### 接口中的GET和POST

- 从协议本身看，并没有什么限制说GET一定不能没有body，POST就一定不能把参放到URL的querystring上。因此其实可以更加自由的去利用格式。

- REST 对API的规定
  - REST中GET和POST不是随便用的。在REST中, 【GET】 + 【资源定位符】被专用于获取资源或者资源列表，与浏览器的场景类似，REST GET也不应该有副作用，于是可以被反复无脑调用。
  - REST 【POST】+ 【资源定位符】则用于“创建一个资源”

#### GET请求一次，POST请求两次

- POST第一次请求先给请求头，然后请求通过之后进行第二次请求，发送请求体

- 举个实际的例子，比如写一个上传文件的服务，请求url中包含了文件名称，请求体中是个尺寸为几百兆的压缩二进制流。服务器端接收到请求后，就可以先拿到请求头部，查看用户是不是有权限上传，文件名是不是符合规范等。如果不符合，就不再处理请求体的数据了，直接丢弃。而不用等到整个请求都处理完了再拒绝。