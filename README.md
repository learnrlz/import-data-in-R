# import-data-in-R
自己收藏经常用到的一些r导入数据的程序
用 openxlsx 包来实现，之前又用过另外一个包，但是需要加载好几个包，
速度一般，导入一个3万条左右的数据花来估计又10分钟使用体验不大好。
明天去验证一下用这个包导入3万条数据大概花多长时间

install.packages("openxlsx")
library(openxlsx)

#测试是否可用
ta <- read.xlsx("/Users/soft/RDATA/test.xlsx")
＃result
> data
  this    is test
1    1    fe   fs
2   23 retwt   12
#result str()
> str(data)
'data.frame':	2 obs. of  3 variables:
 $ this: num  1 23
 $ is  : chr  "fe" "retwt"
 $ test: chr  "fs" "12"
 
＃完美搞定还有就是常用的导入sas 数据集来
