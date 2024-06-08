## Can Large Language Models Faithfully Express Their Intrinsic Uncertainty in Words
### 关键词： 模型内部的对齐程度，uncertainty
目的：研究大模型能否对于不确定的问题，用较为模糊的预期来表达（如not sure，possibly）
指标选择：重采样20次，对比外部的表达确定模型回答单个问题的confidence或者说准确率；引入Gemini作为judge，适当prompting用来对于前面那些模型回答中的肯定程度打分。（跟我们大创的形式好像）
前后两者之间的差值越低，说明对齐程度越高--例如模型对答案不确定，在表述中表达出来了，和在答案中犯错时吻合的。
结论： 即使模型不确定答案，回答时也倾向于给出确定的答案；并且没有找到能够有效鼓励模型表达自己的不确定度的方案。
