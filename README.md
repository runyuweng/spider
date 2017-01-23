# spider
node.js & spider  
知乎小爬虫
## 思路：
- 选择一位用户的个人主页作为起点；
- 爬取此用户的个人信息；
- 将所有关注他的人的个人主页`url`push进urlList数组；
- 直到所有关注他的人的`url`都被push入urlList数组；
- 从urlList中shift出一个url重复以上操作

## 过程：
### index1.js
第一次写爬虫，直接爬取页面，发现爬到的东西不是我所想要的dom树。  
页面有一部分是用js渲染出来的，  
导致爬取过程中信息不全并且爬了一会就会自己停下。
### index2.js
使用phantom，爬取完整的到完整的渲染完成的页面，  
但是使用Promise，运行报错爬取失败。
### index3.js
使用phantom，并且使用async function，  
终于爬取成功，  
虽然有很多小问题但在主要目的基本实现，  
若要运行 请在t中输入:
```
node --harmony-async-await index.js   //  index1.js和index2.js只需用node命令即可运行
```

----- 持续完善中 -----
