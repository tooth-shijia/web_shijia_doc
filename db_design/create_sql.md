##### **【产品展示】**
```
CREATE TABLE `product_show` (
`id` int(10) NOT NULL AUTO_INCREMENT COMMENT 'id 主键',
`product_name` varchar(100) NOT NULL DEFAULT '' COMMENT '产品名称',
`product_id` varchar(100) NOT NULL DEFAULT '' COMMENT '产品编号',
`product_classify` int(10) DEFAULT NULL COMMENT '产品大分类(预留)',
`product_type` int(10) DEFAULT NULL COMMENT '产品类型，见表product_type',
`comefrom` varchar(50) DEFAULT NULL COMMENT '来源',
`author` varchar(50) DEFAULT NULL COMMENT '作者',
`content` longtext DEFAULT NULL COMMENT '产品介绍内容',
`show_count` int(5) DEFAULT NULL COMMENT '点击次数',
`createtime` datetime DEFAULT NULL COMMENT '创建时间',
`lastmodifytime` datetime DEFAULT NULL COMMENT '最后修改时间',
`is_delete` tinyint(1) NOT NULL DEFAULT '0' COMMENT '是否删除',
`_timestamp` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT '需要增加的列，用于DMO抽取数据',
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8 COMMENT='product_show 产品展示表';
```

#####**【产品类型表】**
```
CREATE TABLE `product_type`(
    `id` int(10) NOT NULL AUTO_INCREMENT COMMENT 'id 主键',
    `type_name` varchar(50) NOT NULL DEFAULT '' COMMENT '类型名',
    `createtime` datetime DEFAULT NULL COMMENT '添加时间',
    `lastmodifytime` datetime DEFAULT NULL COMMENT '最后修改时间',
    `lastmodifypeople` varchar(50) NOT NULL DEFAULT '' COMMENT '最后修改人',
    `_timestamp` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT '需要增加的列，用于DMO抽取数据',
    PRIMARY KEY (`id`)
)ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8 COMMENT='产品类型表'
```

#####**【新闻类表】**
```
CREATE TABLE `news_show` (
`id` int(10) NOT NULL AUTO_INCREMENT COMMENT 'id 主键',
`news_name` varchar(100) NOT NULL DEFAULT '' COMMENT '新闻名称',
`news_type` int(3) NOT NULL DEFAULT '' COMMENT '新闻类型，1：公司新闻；2，行业新闻；3，口腔百科',
`comefrom` varchar(50) DEFAULT NULL COMMENT '来源',
`author` varchar(50) DEFAULT NULL COMMENT '作者',
`content` longtext DEFAULT NULL COMMENT '新闻内容',
`show_count` int(5) DEFAULT NULL COMMENT '点击次数',
`createtime` datetime DEFAULT NULL COMMENT '创建时间',
`lastmodifytime` datetime DEFAULT NULL COMMENT '最后修改时间',
`is_delete` tinyint(1) NOT NULL DEFAULT '0' COMMENT '是否删除',
`_timestamp` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT '需要增加的列，用于DMO抽取数据',
PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8 COMMENT='新闻表';
```