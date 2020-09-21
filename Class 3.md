语义互联网并不是独立的另一个web,而是web的另一个延申。信息被赋予明确而完整的信息

web of data 3.0时代

对问题领域进行分析，去欸的那个语义互联网能够解决的问题

选择或创建Ontology，如果问题领域已经有了领域的标准化ontolology

定义ontology的classes，对领域知识的抽象描述

使用子类-父类（subclass-superclass）继承关系组织这些关系

为class定义属性（slots）并描述属性的约束（数值的类型，取值范围，可出现次数）


依据选择建立的ontology，创建对象实例

依据需求应用程序和服务

## RDFS
RDFS是给RDF提供语义，添加语义的方式主要通过词汇，RDFS主要内容是词汇表

<rdf:list> <rdf:first> <rdf:second> <rdf:nil>

##OWL
`web ontology language OWL`

源自DAML+OIL，是作为RDF（Resource Description Framework）的扩展词典进行开发



xml,xmls满足拥有一直定义的词典进行数据交换

RDF/RDFS提供了概念/属性/子属性/。但是还不够强大，缺少cardinality, disjiont


OWL FULL(OWL DL(OWL LITE))

FULL版本取决于用户在多大程度上需要RDF，可能不可预测

OWL成为WEB语言是因为URL提供了唯一标识

RDFS的扩展和有效推理的需求相冲突？定义是灵活的，但是推理是不可判定的

OWL 和OWL LITE没有完全的继承RDFS。而是采用经i的那的逻辑解释。要求个体、类、特性是不相交的集合

所有的个体都是资源，类是资源的集合

OWL FULL完全兼容RDFS 也包含了OWL DL的内容，也是其推理不可判定的原因


# 命名空间
向下兼容，利用实体来简略URI

在文档类型声明中提供的一些实体定义常常是很有用的。

# OWL
owl:thing 指代的是全集

owl:nothing指代的是空集

基本元素：唯一值，表示只有唯一一个

inverof 表示两个属性互为逆

allvaluesfrom:属性所有的值域必须是B，相当于对其做出限定，全都是B

somevaluesfrom：至少一个实例的属性值满足B。至少有一个是B

hasvalue:表示它的值可能有很多个，只要有一个包含就是

same as: 做个体间的映射

alldifferent: 集合当中的元素互不相同

distinctmemebers用于承接上面那个说明集合中的各个元素各不相同

通过匿名类构造复合类

