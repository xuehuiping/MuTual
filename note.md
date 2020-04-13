2020-04-13 15:06:22 

多轮对话推理的数据集


ACL2020的论文，微软亚洲研究院、西湖大学、浙江大学发布

主要任务：听一段对话，从4个选项中，选择正确答案。

基于检索的多轮对话推理

数据来源：高中英语听力理解



数据举例：

```json
{
    "answers": "C",
    "options": [
        "m : when we finish making the birthday cake , we can start preparing for the birthday party .",
        "m : oh , i forget it , cooking a huge dinner is not easy .",
        "m : okay , i 'll put candles on it right away . i think i will be a little tired after all this preparation for this birthday party .",
        "m : the party is almost ready , but the food is not enough . let 's prepare some more ."
    ],
    "article": "m : is everything ready for billy 's birthday party ? f : yes . i finished making the birthday cake and i put everything on the table . did you find the party hats ? m : yes , i did . i put one for each child on the table . i put up the big `` happy birthday '' sign , too . f : thanks , honey . do you think we have enough for the kids to eat and drink ? m : i 'm sure we do . here 's enough food to feed an army . f : that birthday cake looks beautiful , but you have n't put any candles on it yet .",
    "id": "train_10"
}
```

正确答案是C，也就是options的第三个。

article是两个人之间的一段对话，m代表man，f代表female。



将问答方式换为选择式。

<img src="./readme/construct.png" width="1000" >


所有的选项都与上下文有关，但其中只有一个是逻辑正确的。

在极端情况下，一些错误的选项可能是合理的，但正确的选项是最合适的。

紫色下划线是线索词。

<img src="./readme/example.png" width="1000" >


```
训练集：7089
验证集：886
测试集：886
```


测试集没有正确答案。


We will start MuTual challenge soon.

比赛即将开始

