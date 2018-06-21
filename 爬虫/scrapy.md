# 网址
- [Docs » Scrapy Tutorial](https://docs.scrapy.org/en/latest/intro/tutorial.html)英文版的文档
- [Docs » Scrapy入门教程](http://scrapy-chs.readthedocs.io/zh_CN/0.24/intro/tutorial.html)中文版的文档
- [QuotesBot](https://github.com/scrapy/quotesbot)案例，在GitHub上
- [小白进阶之Scrapy第一篇](https://cuiqingcai.com/3472.html)可以看到scrapy的架构图
# 概念、名词
- Scrapy项目
- Item
- spider
- Pipeline
# 创建Scrapy项目
命令：
```
scrapy startproject 项目名
```
项目目录
```
项目名/
    scrapy.cfg
    项目名/
        __init__.py
        items.py
        pipelines.py
        settings.py
        spiders/
            __init__.py
            ...
```
# Item
- Item 是保存爬取到的数据的**容器**<br/>
- items.py 是文件。创建项目后首先需要在这里定义item，用来临时存储需要保存的数据。方便以后保存数据到其他地方，比如数据库或者本地文本。下面定义的就是一个item（DmozItem）。
```
import scrapy

class DmozItem(scrapy.Item):
    title = scrapy.Field()
    link = scrapy.Field()
    desc = scrapy.Field()
```
# Spider

在 项目名/spiders 目录下编写你自己的spider类。该类有几点需注意
- 必须继承 scrapy.Spider 类
- name属性唯一
- start_urls
- parse(self, response)方法

其它
- start_urls
- allowed_domains不是必须的
- 
