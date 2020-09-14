# RDFs
## RDF/RDFs/OWL的区别
RDF（s）是指schema,模式,对RDF的一个抽象和归类。对个体的抽象形成的概念。

RDF表述的是资源，是实体。

OWL基于RDFs添加了语法，描述关系

RDFs与OWL都是本体语言

## 动机
RDF 描述的是事实/资源/实体 ->

模式（schema）知识，术语知识(terminological knowledge)用一般化的知识，对于实例的抽象，不特指特定的实例 ->

RDFs进行模式建模，OWL有更好的表示能力

## RDFs概述
兼容RDF

每个RDFs文档都是RDF文档

命名空间：定义一个标签，为一个特定的URI,在里面定义各种不同的词汇。

RDF命名空间的词汇是通用的


## RDFs类和层次结构
rdf:type 表示一个类的实例

类之间可以按层次结构进行组织

rdfs:Class ：所有的类都是这个的一个实例，rdfs:Class的所有类的类

rdfs:Resource 

rdf:Property

rdf:XMLLiteralRDF唯一的预定义类型 

rdfs:Literal 所有字面体的类

rdf:Bag rdf:Alt rdf:Seq rdf:s:Container rdf:List rdf:nil 列表类 

rdf:ContainerMembershipProperty 容器属性类

（各种列表容器的属性类内部元素之间的关系）

rdfs:member 所有集合之间的包含关系的超类

（a rdf:ContainerMembershipProperty b --> a rdfs:member b）

rdfs:Datatype 数据类型类

rdf:Statement 物化三元组类

## 隐式知识
通过推理演绎得到的知识

rdfs:subClassOf 是传递的（transitive）

Ontology(RDF/OWL)-> Reasoner(produce implicit knowledge)->Completed knowledge base <->Application

通过显示知识推出逻辑结论。不需要进行显示地声明。

什么样的是逻辑结论？根据三元组的形式语义

## 类的等价
两个类互为子类， subclassof

每个类为自己的子类

## 属性层次结构
通过子属性可以退出属性的语义

## 属性约束
值域的限制

### 缺陷一
定义域和值域之间组成了类和属性之间的语义链接，因为它提供了术语化的相互依赖关系的唯一方式

有潜在问题：导致一个实体同时是两个取值范围的，但是有语义冲突

### 缺陷二


**每个被声明的属性限制会全局地影响此属性所有的出现情况，在使用属性限制时要非常小心，尽量使用足够一般的类**

## 物化三元组 Reification
辅助接点 

利用空白节点代替一整句话，说明这个空白节点的诸位并，同时将空白节点声明为statements的一个实例

## 补充信息
rdfs:label URI命名

rdfs:comment 为资源指定注解

rdfs:seeAlso 链接：用于连接到提供关于主语资源更多信息或定义URIs

rdfs:definedBy 由什么来定义




# RDFs形式语义
## 为什么定义语义
这里讨论的语义是逻辑纬度的语义，形式语义（formal semantics）

引入RDF(S)的作用： 给定的说明中得到的结论的解释不足够充分

通过样例解决问题并不能在其他的推理中达到共识

给定一个逻辑，用P表示命题的全集

用一个符号|=表示推论关系，比如{p1,p2}|={p3,p4}

推论关系把命题的集合与命题的集合关联起来

一个逻辑L是由一个命题集合一个推论关系共同组成的，子啊抽象的层次上可以描述为L=（P，|=）

## 语法/语义
Syntax:语法是没有意义的字符串

Semantics:语义是有意义的字符串

## 逻辑语义
### 模型论/证明论
模型论：给出程序的模型，说明性的第给出程序的意义
证明论：给出一个证明过程，得到程序所能推导出的逻辑结论

模型论语义的研究是从逻辑基础出发，定义程序的模型，并使其接近直观模型，就是建模呀

证明论：基于模型论，使其更加合理。论证呀

## 什么样的语义是好的
语义网的语义是通过逻辑结论形式进行表示

定义语义，不是通过直接指定其意思，而是通过该概念和其他概念之间的关系定义其语义

### interpretation
潜在的“现实”和”世界” 它不用遵循常识。

在形式逻辑中，根据逻辑选择合适的数学结构

I是p的模型，记作I |= p，与推论关系使用相同的符号

解释是一种数学结构（模型）

## RDFS解释器分三层
imple intepreter -> RDF ->RDFS



