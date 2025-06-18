

扔硬币最多可以扔一百次。我说H-T期望不论选怎样策略都是0，他说如果我扔H-T>0就停下来那么期望就大于0。给他从概率空间，martingale，OST，各种角度解释，他就是不停重复你是错的。

这个和绿皮书上 all girl world 那题是等价的。 但是我觉得楼主要是面试的时候就给出这个简单的实验来反驳面试官，那肯定比来一堆martingale ost 要有效。
1. fair coin, expected number of flips until n heads
2. 一道概率题，第一天下雨概率 x% （我不记得x是多少了），第二天是 y% （不记得+1），问两天中至少有一天下雨概率的上下限。 - 印象中绿皮书有类似题，叫 joint default 什么的。绿皮书里这题的回答分为两部分，第一部分就是问概率的上下限，第二部分问corr还是cov的上下限。我是完全不记得这题了，一上来我就写了概率和corr的关系，面试的老哥也没啥互动，最后啥也没算出来。老哥不耐烦的就结束了面试。面完之后翻绿皮书才发现原来是个小学暑假作业水平的脑筋急转弯，绿皮书还专门提了一句 千万不要从corr出发否则算不出来 - 周六50%概率下雨，周日80%下雨，问周末下雨的概率。当时在地里看到 觉得太简单就跳过了，结果让我说correlation范围的时候被问住了，卡了一会儿才算出来，感觉没表现好。
3. 面的题目地里有，但我当时没见过，就是圆圈上随机20个点选4个点连线，求两条线交叉的概率。这题一定要用permutation，其实概率也能做 写一个sum答案也一样，但是容易出错。总体面得不错 - 圆上先随便确定四个点，拉弦相交的概率都是1/3. 和从20个，200个点中取四个，均匀取四个，甚至不均匀任意分布取四个点都没关系。相交概率一直都是1/3
4. 一个是抛硬币有T个tail就要T+1 consecutive head的  - Flip a coin. If you have flipped T tails, you need to flip T+1 consecutive heads to win the game. What is the probability to win the game? - ，问赢的概率。列出式子后大致估计一下赢的概率是否<1， 回答是，因为那个连乘会收敛到某个大于0的数，然后他就结束了问题 - 条件概率。

P(永不停下) = P(在扔出2个连续H之前又扔出一个T | 已扔出一个T)*P(在扔出3个连续H之前又扔出1个T | 已扔出2个T) * ... * P(在扔出n+1个连续H之前又扔出一个T | 已扔出n个T)* ...

所以是(1-1/2)*(1-1/4)*(1-1/8)* ...
这个连乘你可以取log然后放缩一下，是大于0的 - 差不多。就是算永远停不下来的概率是多少，应该是(1-1/2)*(1-1/4)*(1-1/8)*...,然后估计一下这个连乘是不是收敛到0  

5. N is a positive number. I randomly pick a number, K, from [0, N-1]. If K == 0, the process ends, otherwise we keep picking a number from [0, K-1] until we pick 0. What is the expected number of picks to end the game? - 递推一下f(n) 是harmonic series. - 1 - Product[1-1/2^k, {k, 1, Infinity}]，可以证明这个无穷乘积是收敛的，最后数值上是0.711212
我是用马尔科夫链做的 1-10，10个数，不放回地抽两个数的乘积的期望与放回地抽两个数的乘积的期望，哪个大？要求intuitive地心算回答并解释为什么。
6. How to estimate the coefficient (beta) of linear regression is different from 0.  (这里应该是个假设检验的问题)
7. 第一题：扔硬币100次，问得到大于等于60H的概率是多少，用CLT
8. 关于随机游走里面的反射原理
9. 有两个棍子A,B不同长度。你有把尺子，每次度量会有一个N(0,sigma)的误差。给出一个测量A,B的方案使得误差的方差最小。 测量A+B跟A-B
10. 甲抛硬币，规则是，每当出现了k个T，甲需连续抛出k+1个H游戏才能结束。问游戏有限次结束的概率。
11. 甲抛硬币，赌博游戏，起始有一刀，抛出H资产翻倍，抛出T归零。问期望收益。（细节忘了，大概是这种题目）。
12. 青蛙在0点往正方向跳，每次跳的长度是Uniform(0,1). 问它第一次跳出1需要的期望步数（我给了个简单解法，答案是e步）。followup：第一次跳出k需要的期望步数。 感觉像是Petersburg paradox？lz简单解法大概是用m（x）=m'(x)代入boundary condition解，一般的可以求出分布然后暴力算。 https://artofproblemsolving.com/community/c7h20848
13. 甲抛硬币，与乙比赛。如果H的个数比T多k个则甲胜，如果T比H多k个则乙胜。问：游戏在100次抛硬币后还没结束的概率。（没有显式解，要给出计算思路）问题的反面等价于一个随机游走n步之内达到k or -k的概率，写递推式P(n,k)=P(n-1,k) + (1-P(n-1,k))*0.5*P(n-1,k-1)，?
14. expected value of roll 3 times of dice
15. 一是电话号码的个数，不考虑区号，7位电话号码，第一位不能是0或1，7位中不能出现连续的911，问一共有多少种可能的组合，反正就容斥原理一下，最后的答案是7958028，我很好奇有没有更简单的做法
16. 


