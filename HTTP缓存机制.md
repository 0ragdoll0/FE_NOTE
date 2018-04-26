# cache相关头部信息
![](https://github.com/0ragdoll0/FE_NOTE/blob/master/pics/cacheheader.png)

# 缓存过程
![](https://github.com/0ragdoll0/FE_NOTE/blob/master/pics/cache.PNG)

# 缓存过程详情

## 强缓存
> 1.浏览器在请求某一资源时，会先获取该资源缓存的header信息，判断是否命中强缓存（cache-control和expires信息），判断依据：Pragma > Cache-Control > Expires           
> 2.若命中直接从缓存中获取资源信息，包括缓存header信息。     
> 3.返回200（from cache），不会与服务器进行通信        

## 协商缓存
> 1.强缓存未命中，向服务器发请求，让服务器根据请求的头信息来决定返回内容          
> 2.Last-Modified/If-Modified-Since,Etag/If-None-Match是成对存在的，前者是第一次请求的响应头返回的，后者是后续协商缓存时请求头中的。     
> 3.上缓存过程中Etag?和Last-Modified?的意思是是否存在，不是判断是否不同。        
> 4.为什么出现Etag:Last-Modified只精确到秒级/周期性更新值会改变，其实内容未改变。        
> 5.根据If-Modified-Since，If-None-Match的值判断返回304/200      
> 6.返回304即使用本地缓存，返回200及资源

## 状态码
![](https://github.com/0ragdoll0/FE_NOTE/blob/master/pics/state.PNG)
