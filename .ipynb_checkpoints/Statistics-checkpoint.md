

造一个例子 两个random variable dependent but not correlated

请举出一个栗子，X,Y不独立

相关系数为0，X和Y不一定独立，这我知道，但是怎么举例子呢（还要满足 X ,Y 是服从正态分布的随机变量

X+Y 和 X-Y

补充内容 (2019-7-11 05:11):
不对 这俩是独立的

补充内容 (2019-7-11 05:25):
https://en.m.wikipedia.org/wiki/Misconceptions_about_the_normal_distribution


X ~ N(0,1), Y = UX where U follows Rademacher 



给你一个function f(x), x 属于[0, 1]之间，已知f(x)有唯一最小值，但是f(x)不可导，没有f(x)的表达式，当做黑盒，问你有没有算法把函数的最小值点估计出来，满足一定精确度即可。解法：把x的domain分成相等的三份，比较两个等分点a，b的相对大小，如果f(a) > f(b)，那么解就在[a, 1]之间，<在[0, b]之间，相等则在[a, b]之间。重复此步骤即可。难度不大，四十分钟在和对方qr的讨论下轻松过。


Conditions to diagonalize a matrix （我答的是full rank，他不太满意说最方便是check if symmetric，我觉得不对但没当场反驳）
你第一题回答的是错的。 full rank只能保证存在对应的Jordan 标准型， 但这个标准型不一定是对角矩阵。最简单的例子是A = [1, 1;0,1] full rank但是不可以对角化。
一般矩阵对角化的充要条件是sum of dims of eigenspaces  = dim of the matrix.
具体到C^{n*n}的矩阵，充分条件是 Hermitian的。只考虑实矩阵，那就是symmetric
对，对C/R矩阵Hermitian/symmetric是比可对角化要强的条件，我的思维定势是找出不可对角化的矩阵，那symmetric就不是个有效的条件


AB testing how to decide sample size, how to verify whether the result is statistically significant?

开放式问题讨论就是trader 手里有两个策略A，和B，理论上每天return 的mean 和 std 都不一样，现在trader 在跑一个策略，但他也不知道自己跑的是哪个，并且你换了后就不能再换回来。基于这个问题的各种讨论。他家面试感觉都是面试的人随意出，没啥规律。我还碰到一轮问 estimation 的题，要求给出所有假设和逻辑。

How to estimate the coefficient (beta) of linear regression is different from 0.  (这里应该是个假设检验的问题)

Explain the Chi-square distribution?

Non-parametric regression methods. Boosting Tree.

How to solve overfitting in linear regression. How to estimate lambda in LASSO and Ridge.

Min-stack application and implementation.

Final的体验可以用直线下滑来形容：
第一轮问背景，聊research，给对方聊懂了，然后问我几个数学题，如何用[0, 1]的均匀分布来模拟二维的均匀分布，如果二维的形状是任意的（三角形或者方形），但是是凸型，在这个任意形状内想要得到均匀分布的点，如何用[0, 1]的一维均匀分布模拟。问题不难，map二维正方形区域[0, 1] x [0, 1]的端点到这个任意形状，内部的点直接weight average即可。
第二轮依旧问背景，很奇怪，问题和第一个人一模一样，我又疯狂地讲了一遍我的research，对方好像对我的领域也不是很熟悉，也不感兴趣。然后问数学问题，如果一开始A=1, B=1，第一轮随机选A或者B加1，选择的概率是proportional to A或者B的占比，比如 A/(A+B)。 问你后续会发生什么。解法：其实就是列一下前三次采样的情况，发现A+B总和一定的情况下，A,B各种分布结果的概率都是一样的。

本来以为前两轮都答上来了，也问题不大，然后！！本来约好的半小时后的第三轮神奇地取消了，说skill set不符合，我懵了，不知道我哪里做的不好，整个流程下来其实lz已经做的比较流畅了，可能的原因就是他们已经招满了QR(他们自己叫quant strategist)。或者干脆面完两轮看我不顺眼，对我的科研不对胃口，好吧，哎感觉有点rude，不说了，权且给地里做些贡献吧。


上来先是问一 爱根外流 的问题。然后问我 positive semi definite 条件（感觉就是rephrase前面的问题）。 之后问我PSD在optimization里面有什么好处啊。后来他看到我用了TSNE的方法，然后就开始问这个了。先让我解释了TSNE，然后问我我是怎么决定这个算法里面的hyper parameter的，我只回答了perplexity，hyper-parameter， learning rate还有iteration的选择。 然后突然问我你的t的自由度是怎么选的。。。我当时就闷逼了，因为我不记得我用的包里面有这个选项啊。。。于是我老老实实的坦白我用的包里面没见过定义自由度的attribute。。。然后大哥问我你自己会怎么想定义呢。我把我以前看过的一片论文上的三个方法说了一下，他来了一句fine。。。 感觉很不妙。。。还有些记不太清楚了。。。

请问idenpotent matrix 的rank和trace是多少

soln: 就是sum of eigenvalues, 因为 idempotent matrix 的eigenvalues 只可能是1 或者0. 所以它的trace 和rank的值相等。


你我比赛抛硬币。我赌hth 先出，你赌hhh 先出。请问我赢的概率有多大，请问期望抛多少次才会分出胜负。


soln: 这个写一个markove chain transition matrix 就可以了。


1. Say you a have a list of float number with length N, each number is IID between 0 and parameter a. Give me an unbiased estimate of the parameter a. 
我自己说了两种办法，一个是sample mean，一个是linear regression，但好像都不是满意的答案。我后来查了一下，sample mean是unbiased，linear regression不是unbiased（linear regression的方法是可以无偏估计1/a）。后来搜了一下，恍然大悟，原来可以直接用max来估计，然后考虑max的期望是N/N+1 * a，所以parameter a的无偏估计就是N+1/N * max，可惜了！




3. Tell me about your project, give me some highlight of your research


4. Does it get the same accuracy as mean-field method?


5. Would you miss some phenomenon based on this mean-field theory?


6. Tell me some software development research experience on your resume


7. Tell me a little bit about your chemistry context of your research? What do you try to simulate?


8. These simulations seem standard. There must some packages already existing doing the similar job, why do you develop it from the beginning?


9. How accurate is your result? Since your metal system doesn’t have band gap, will it behave the same as the actual metal?


10. What are the remaining steps to achieve your final goal?


11. If the result is not accurate enough, what adjustment will you do to make it more accurate?



Reference: https://www.1point3acres.com/bbs/thread-1122925-1-1.html
