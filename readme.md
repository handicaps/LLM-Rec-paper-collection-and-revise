
##24年5月阅读

### RecSys-Assistant-Human- A Human-Centered Recommendation Framework with LLM Agents
推荐系统完成随机筛选若干不同分类商品-助手开始工作，根据用户feedback学习用户特征-从初始商品中挑出部分符合的-返回给推荐系统
让agent专注于用户，而不是推荐系统。最大化初始互动的利用率，减少选择性偏差（由于学习时选择的样本分布不均匀导致的？）
如果出现conflict，那么就解构冲突特征来最小化冲突，并且等待后续的用户feedback信息来确认。
因为使用了LLM，所以可以用较少的action完成personality的学习，减小用户负担；因为LLM可以更广泛地理解，不会单纯向训练数据中出现的like或者dislike的物品去拟合，所以减小了bias；可以本地使用，加强了user control。
可控的结果，assistant分享给推荐系统的信息有限，保护用户隐私。
采用GPT-4-0613完成实验。测试部分，1000个用户每个对应一个assistant。  一个消融实验，验证Learn Agent的作用
对比没有使用assistant的情况，使用assistant的在多种方法的召回率都更高。
