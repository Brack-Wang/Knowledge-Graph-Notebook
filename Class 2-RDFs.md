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


# RDFs形式语义
