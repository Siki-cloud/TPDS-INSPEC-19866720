# TPDS-INSPEC-19866720
This code accompanies the paper  "Cost-Effective App Data Distribution in Edge Computing,"[1]  by X. Xia,etc.,INSPEC number is 19866720. This code writed by qiusiki@foxmail.com make for  Advanced Computer Technology course.
In this repository, the features below are implemented:
- reproduct EDDIP、EDDA alogrithms proposed by the paper.
- reproduct referenced constrastive algrithms Random,Greedy, MMR[2]  
- train for EUA dataset[2]https://github.com/swinedge/eua-dataset

## Usage
for implement this code,you should install at first:
<code>
- python >=3.7
- python library networkx、 matplotlib、 queue
</code>

I test the reproduction code in pycharm2020.
for single example experiment, you should fir generate a GP model graph by python NetworkX.

#### 高亮 Html 代码
```html
run GreatGrapgGM.py  ,input your number of vertex and edges in graph ,then the result will be restored in randomNetwork01.txt.
or 
run GreatGrapgGP.py  ,input your number of vertex and densitity in graph ,then the result will be restored in randomNetwork02.txt.

then calculate the cost and  time for EDDIP\EDDA\Random\Greedy\MMR
run main.py.
if your want to adjust some parameter of the problems, you can amend this command：

```

```python
g=createGM(yg=20,dlimit=2,rnump=1,readfile='randomNetwork02.txt')
```
#### Result of a example 

>i run GreateGraphGP.py

>i input : 10,1.2
>i output:

>s <b>randomNetwork02.txt<br></b>
>s 0 1 1 1 0 0 0 1 1 1 
>s 1 0 1 1 0 0 0 0 0 0 
>s 1 1 0 1 0 0 0 0 0 0 
>s 1 1 1 0 1 0 0 0 0 0 
>s 0 0 0 1 0 0 0 0 0 0 
>s 0 0 0 0 0 0 0 0 0 0 
>s 0 0 0 0 0 0 0 0 0 0 
>s 1 0 0 0 0 0 0 0 0 0 
>s 1 0 0 0 0 0 0 0 0 0 
>s 1 0 0 0 0 0 0 0 0 0 
>s 2 1 4 8 3 9 5 10 

![text](D:\SikiUser\code\一些github开发\2.png)

>i run main.py

>g=createGM(yg=20,dlimit=2,rnump=1,readfile='randomNetwork02.txt')

>i output:
> 物种算法得到的cost 和 计算时间分别为：
> Greedy: cost = 46 time = 0.0
> Random: cost = 225 time = 0.0
> EDDA: cost = 46 time = 0.0019714832305908203
> EDDIP: cost = 46 time = 0.010987043380737305
> MMR: cost = 46 time = 0.005053520202636719

>  red represences the specified edge server -> r node.
>  green represences the common edge server -> common node.
>  the graph visualization like the below image shows:
> ![text](D:\SikiUser\code\一些github开发\23.png)

## dataset

https://github.com/swinedge/eua-dataset

## Reference
[1]X. Xia, F. Chen, Q. He, J. C. Grundy, M. Abdelrazek and H. Jin, "Cost-Effective App Data Distribution in Edge Computing," in IEEE Transactions on Parallel and Distributed Systems, vol. 32, no. 1, pp. 31-44, 1 Jan. 2021, doi: 10.1109/TPDS.2020.3010521.
[2] G. Xue, “Minimum-cost QoS multicast and unicast routing in communication networks,” IEEE Trans. Commun., vol. 51, no. 5, pp. 817–824, May 2003.
