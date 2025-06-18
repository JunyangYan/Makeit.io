1. I have resume in front of me. Just give me a brief overview about your self
2. Follow up question, you said you want to explore how your skills will be applied to finance world, why finance? Why not other area which is science-based or tech-based?
3. What does it look like in your postdoc daily research? Do you deal with large data sets with HPC a lot? (基于简历上的HPC，high performance computing，估计还是想问有没有large data处理经验）
4. Why this position why do you choose us and this role,
5.  tell me about your current job.
6.  what's most chanlenging part of your job?
7.   what would you do if there are conflicts in your team?
8.   what do you think would be the biggest challenge you will face after you get into the industry
9. Do you have other company's offer? Is there any ongoing interview? 
10. Tell me about a time you received critisim from others and how you resolved it？ 讲了下自己teamwork的经历，如何接受反馈提高自己的 communication skills
11. 一次收到负面回馈的经历。tell me an experience when you received negative feedback 
12. When collaborating with others, did you come across a situation where the whole team have different ideas of how to get started of the project, and you were able to convince everyone to start on your path?
13. Tell me about someone you look up to and why? 但我就直接回答的我很崇拜我的妈妈，她有哪些优秀的qualities然后如何constantly inspire me to be a better version of myself.
14. Before HR sharing info about virtu, how much do you know about Virtu?
15. A good thing you did recently
16. Something you didn't mention on resume
17. Follow-up (上个问题问答中提到了Virtu的first-year training program). I’m very curious, do you know somebody that went through the company’s training or how do you hear about our training program?
18. Tell me a project you are most proud of，此外基于这个project问了很多细节，比如怎么解决问题的之类
19. 讨论两个你最喜欢的编程语言的优缺点和存储方式的不同
20. 讲述自己如何小组协作的
21. teamwork中遇到的challenge
22. Introduce Virtu: started in 2018, as market makers, also conduct HFT, Three major sides of our business in Virtu: we are a proprietary market maker, this is where we conduct our track trading; we are a customer market maker, where we work with broker and institutional investors, VCMM (Virtu customer market making), which we will put you under; and last is executional services, we do two things: 1. Conduct agency trading (agency execution) ; 2. Have developers to build tools for customer to purchase from us (algo execution).  Headquarter in NY, second headquarter in TX.
23. Next step:
if passed, next is a tech round. First part is live coding for 1hr. Second part dive into your research experience, the tools you pick up along your academic career, will have brain teaser, probability/statistic/geometry/algebra/algorithmic problem-solving question; and at last, is about “culture, purpose, perspective” to make sure you fit the company.
If tech round passed, next is onsite/super day: talk to 5/6 members in quant team, each conversation will be about research, tech skills, brainteaser. Will lean more on probability and statistical intuition. Will expect a data analysis approach test. In addition, will have a 35 min logic and reasoning test with 63 questions.
24. Tell me about your project, give me some highlight of your research
25. Any question remaining?
Me: Can you tell me more about difference our role or work portion on agency execution and algo execution?
For start quant, they can do both, depends on which specific strategy they are working on. It can either be facing client or doing algorithm training. For me as a signal quant, there is not a such distinguish between these two kinds of execution.
26. 这里竞争很激烈，你怎么样能够让自己stand out？你想好了在金融公司长时间做下去了吗，这里竞争很激烈。
27. Tell me your dissertation
28. Who came up with the research ideas?
29. Do you usually work alone or collaboratively?
30. How much do you know about Virtu? (Used as a segue for her to introduce virtu.)
31. What is the most challenging part in this work experience?
32. Tell me about a time you received negative feedback
33. How do you find this opportunity?
34. what is your greatest accomplishment
35. tell me situation when a disagreement happens in a group project.
36. What's the most challenging thing that you think to transfer from academy to industry?
37. 对下一份职位看重哪些方便
38. what is your most successful project
39. share your biggest accomplishment
40. the biggest challenge you faced
41. 最近你做了什么好事 act of comfort


Why Finance

finance is a fast-pace area. I see finance impact on a daily basis, while science and tech usually take more time to see effects. This fast-pace environment motivates me to learn new skills and techniques and see the feedback/impact in a faster time frame.



Reference: https://www.1point3acres.com/bbs/thread-1122925-1-1.html

Tech round 1.1: live coding
Interviewer self-intro: I work with VCMM team as a signal quant. My daily job is to build models to predict price movement of US equities based on different market data. We also have strategy quant, spending more time to a specific trading strategy, trying to optimize predicting models for trading strategies, closer to the actual production. My role as signal quant is more research focused. The whole quant team (not including traders) is round 40 people. 

2. Looking at your resume, I’m curious about your project on optimization of wavefunction overlap calculations, what is the complexity before your work?
Originally, the problem is No^5Nv^2, where No is the number of electrons/2 and Nv is total number of orbitals - No. 
Previous method used in software package is mainly No^2Nv^2, using svd to find most similar orbitals to the previous nuclear geometry, such that the overlap matrix is mainly diagonal. 
Current method decomposes the expression into two cheaper factorized summations, with time complexity to be No^2*Nv+No*Nv^2, around N^3, compared to previous N^4


. So this improvement is not a numerical advance, it’s actually finding out analytical solution. What about your recent work, as postdoc? Now I guess the problem is different, since you have O(N^4) here? (基于聊的上一个课题的复杂度是O(1). 实际上, 上个课题的复杂度也是O(N^4)，是我没写清楚)
This time complexity comes from calculating two electron integrals. This is the most time consuming part when developing self-consistent field algorithm in electronic structure. To arrive self consistency, we must update integrals in every cycle. However, my work separates this two sub cycles, where in microcycle, only two indices gets updated (O(N^2)), and in macrocycle, we update full integrals (O(N^4)). By doing so, we reduced the number of big cycles that update O(N^4) integrals.
