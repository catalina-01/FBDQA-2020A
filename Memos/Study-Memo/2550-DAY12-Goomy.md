量化策略的深入诊断

必有的量化步骤
ETF期权是欧式期权
==背对策略==
解决回测虚高收益的问题
交易逻辑中是否存在隐蔽问题
量化策略的基本流程

流程细则与技术方案选择 自动化操作：数据、统计分析、调试修正
数据处理：数据对齐、管理配置、数据收集、数据校验、数据比对、数据清洗
统计分析：鲁棒性分析、基础模型、统计检验、数据样本检验、协整分析、样本内外测试、过拟合检验
调试修正：回测平台选择与特性；计算层面维度选择：TICK/MIN；策略层面基本逻辑；系统层面操作系统选择；编程语言层面；样本内外测试；再次进行鲁棒性检验
解决问题：回测收益率高，实盘性能差距大；交易逻辑中是否存在隐蔽的问题，导致实盘中无法交易出来回测的结果
鉴别回测中的虚高收益是运气还是实力

回测是否具有统计意义
回测阶段不足200次交易不可行
==经验值最低也要70次交易==
策略逻辑的问题：未来函数
量化策略诊断checklist

蒙特卡洛模拟

期权估值

欧式期权：看涨期权、看跌期权
期权的风险中立预期定价 $C_0=e^{-rT}E(h(S_T))$ $h(S_T)=max(S_T-K,0)$ $h(S_T)=max(K-S_T,0)$
使用蒙特卡洛模拟来近似该期望 $\widetilde C_0=e^{-rT}\frac{1}{I}\sum\limits_{i=1}^{I}h(\widetilde{S}^j_T)$
