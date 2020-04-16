# awesome-tools


## JVM
* 按线程状态统计线程数

``` shell
jstack $pid | grep java.lang.Thread.State:|sort|uniq -c | awk '{sum+=$1; split($0,a,":");gsub(/^[ \t]+|[ \t]+$/, "", a[2]);printf "%s: %s\n", a[2], $1}; END {printf "TOTAL: %s",sum}';
```


## network
* 查看系统当前网络连接数
``` shell
netstat -n | awk '/^tcp/ {++S[$NF]} END {for(a in S) print a, S[a]}'
```




## 摘录
https://mp.weixin.qq.com/s/mzJLGBJR3Bcmx-jKCLbuHA
