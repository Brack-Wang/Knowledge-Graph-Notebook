# 语义网概述
## 教学目标
```
了解知识表示、语义网的基本概念
掌握RDF,RDFs，OWL,Rules等语义知识表示语言，熟练掌握描述逻辑的语法和予以，掌握本体概念和本体建模方法
了解知识图谱基本概念，理解知识图谱的技术内涵和外延
掌握知识图谱的表示和关联建模、存储和关联查询，知识图谱的获取和语义关系抽取技术，知识图谱的简单推理等
掌握领域本体和知识图谱构建技术，并开展简单的应用
```
## 课程资源
[http://www.openkg.cn/](http://www.openkg.cn/)

NLP词库：HOWNET/WORDNET

在线词库

### 知识图谱网络
GOOGLE: Freebase

沃森：YaGo

Tim Berles-Lee: Linked Open Data

交大： zhishi.me

[## 课程安排](https://github.com/Brack-Wang/Knowledge-Graph-Notebook/blob/master/images/KG%E8%AF%BE%E8%A1%A8.jpg)
[## 课程实验](https://github.com/Brack-Wang/Knowledge-Graph-Notebook/blob/master/images/KG%E5%AE%9E%E9%AA%8C.jpg)

---
# 总结：
什么是语义网，从WEB到语义网

什么是本体，本体的作用

资源描述框架RDF，TURTLE语法与XML-based语法

---
# 发展历程
## www
web1.0->web of docunments

web2.0->web of persons

web3.0->web of data

## 发展历史
1998年 Tim Berners-Lee提出（89年提出WWW）

W3C metadata activity（提出RDFs）

## 存在问题
本体库构造代价太高

语义网太丰富，目前的推理算法不能识别（可判定性低）

# 概念
## 当前WEB存在的问题
但是当前的web中知识不能被机器所理解，大量的知识不能被人挖掘。信息很多但是结构化的信息太少，如果机器可以自动的进行知识提取，将大幅度的提高web上知识的利用率。

信息多为满足人类消费使用->搜索的方式非常的简单（通过关键词搜索）

WEB内容多为异构的（内容异构/结构异构/编码方式异构）

## 语义WEB的基本组成
描述WEB信息

主要方法：逻辑演绎（自动推理）/归纳

---
# 本体
## 对于本体的理解（存在与本质）
>ontology就是本体，也就是一个抽象的概念，这个抽象的概念在现实生活中进行映射。就是柏拉图所说的本质与存在之间的关系。因而人与人之间可以进行沟通交流。因此如果想要让机器完成这样的任务，我们让机器对一个概念有共同的理解，那么当机器进行交流中就不存在语义偏差。理解是在个体与个体之间建立起来的？

>知识图谱是基于存在论衍生的计算机模型。

>刘炜：认为每个人大脑中，有一个结构相同，内容近似，涵盖丰富，查询和推理功能强大并能方便提升的知识库系统。对机器而言，也是同样的，机器之间进行相互理解和沟通，也需要这样的知识库，我们称之为**本体**，即**术语库**

本体：以概念为核心，描述的内容更加丰富。利用OWL语言进行。<-->知识图谱：描述的是大量的实例。利用RDF。

本体是指一种”形式化的，对于共享概念体系的明确而又详细的说明”。

本体提供的是一种**共享词表**，特定领域之间村啊在着的对象类型和概念机器属性和相互关系 formal representation。

## 本体语言
有合适的知识

含义通过推理和逻辑算法

可伸缩性具有挑战

Expressivity<-->scalability表示能力与可扩展性拮抗

本体的核心是分类体系（Taxonomy）分层体系/（partonomy）整体-部分体系 的层次结构

---
# RDF
## 知识图谱层次结构
```
Unicode:编码

URI：全球资源标识。每一个实体对应的标识

XML：非常重要

本体层->

RDF：描述的是实体。资源描述框架，做数据交换

RDF-s：描述的是概念。

Rules:RIF: 规则描述语言

Query:SPAROL

ontology:OWL
```

## 为什么使用RDF

一开始是用XML传输信息。但是XML将信息描述成树形结构。当信息很多的时候，需要同时描述，需要对树形结构进行合并。数据将变得臃肿且不易理解

通过三元组的方式，很自然的将实体变成了节点与线的形式，形成图的形式。信息通常被分散存储和管理，合并不同来源的RDF数据变得更加容易。使得扩展更加便利。

## 什么是RDF
RDF(Resourse Description Framework)

标准规范： http://www.w3.org/RDF/

Metadata：描述数据的数据

用于描绘web pages的metadata结构化的信息/通用的机器可读的信息/基本的语法是遵循XML规范的

### RDF的结构
URIs： 表示的是一个个的数据和实体。避免歧义，在全球范围内可以查询。-for referencing resources

Literals文字：没有打上双引号的字符串-data values

Empty nodes空节点:没有命名的节点-允许节点内容为空
```
Lieral:
表示数据的值
采用字符串进行编码
值通过数据类型进行解释
没有数据类型的字面体当作字符串进行处理
```
### 规则
主语： URIs/空节点
谓语： URIs（属性properties）
宾语： URIs/空节点/文字（Literal）

### Turtle语法【不被W3C支持】
```
-URIs放在<>中
-文字用双引号""
-三元组用英文句号结束
-忽略空格
```
#### 前缀缩写
@prefix xxx:

#### 相同主语进行合并
主语合并，两句之间用；分开

谓语合并，两句之间用,分开

### RDF的XML-based写法
名字空间用来对标签进行消歧

三元组嵌套

无类型的

DTD 利用！ENTITY 做字符串替代。由于有时候在UUI中的“”不能写：，只能通过该方式进行引用使用方式为 &book;

基础命名空间(base namespace) 相当于设置默认的URI，直接写URI相当于指代开头指定的值

#### 数据类型
相当于强制类型转换

`rdf:XMLLiteral`是RDF唯一内嵌的

### 语言表述结构
考虑到结构性，便于查询，准确表述

利用三元组表示
```
IMPORTANT:
`rdf:parseType="Resourse"`表示自动创建一个空节点

*_:id 空节点有一个下划线代替命名空间前缀
```
### Open Lists <-> Closed Lists
open可以添加节点，closed不可以添加
```
open 可添加新元素
rdf:Seq 有序
rdf:Bag 无序
rdf:Alt 可替代的
```
* RDF是链表

* nil表示结尾
