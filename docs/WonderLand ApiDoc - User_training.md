﻿# WonderLand ApiDoc - User_training

标签（空格分隔）： WonderLand

---

[TOC]

---

## **属性**

- **`【user_training 表】`**

| 属性名          | 中文   | 最小长度 | 最大长度 | 类型      | 特殊要求
| --------------- | ------ | -------- | -------- | --------- | --------
| **UTid**        | 记录id | -        | -        | int       | - 
| **Uusername**   | 拥有者 | -        | -        | char(20)  | -                       
| **UTtitle**     | 标题   | 1        | 50       | char(50)  | - 
| **UTdate**      | 日期   | -        | -        | TIMESTAMP | -          
| **UTplace**     | 排名   | -        | -        | int       | -           


- **`【user_training_contest 表】`**

| 属性名          | 中文   | 最小长度 | 最大长度 | 类型      | 特殊要求
| --------------- | ------ | -------- | -------- | --------- | --------
| **UTid**        | 记录id | -        | -        | int       | -
| **UTaddress**   | 地址   | 1        | 150      | char(150) | -
| **UTproblemset**| 题集   | 1        | -        | char(50)  | -


- **`【user_training_article】`**

| 属性名          | 中文   | 最小长度 | 最大长度 | 类型      | 特殊要求
| --------------- | ------ | -------- | -------- | --------- | --------
| **UTid**        | 记录id | -        | -        | int       | -
| **UTarticle**   | 文章   | -        | -        | char(200) | -


---

## **接口 · 增加记录**

- **接口网址：http://icpc-system.and-who.cn/User_training/post**

- **表单要求**

| 属性名          | 必要性 | 最小长度 | 最大长度 | 特殊要求
| --------------- | ------ | -------- | -------- | --------
| **Utoken**      | O      | -        | -        | **持有token的用户即作为成员1**
| **UTtitle**     | O      | 1        | 50       | -    
| **UTplace**     | O      | -        | -        | -    
| **UTaddress**   | O      | 1        | 150      | -
| **UTproblemset**| O      | -        | -        | **用#分隔的字符数组，如O#O#.#O#.**