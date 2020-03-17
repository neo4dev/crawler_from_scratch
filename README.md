# 从零学习爬虫 Crawler from scratch
> 运用Jupyter Notebook 演示爬虫是如何运作的


## 如何使用
1. 下载本教程 `git clone https://github.com/neo4dev/crawler_from_scratch.git`
* [下载并安装Anaconda](https://www.anaconda.com/distribution/#download-section) （包含了Jupyter Notebook以及运行代码所需要的常用库）
* 命令行中启动 Jupyter Notebook `jupyter notebook`

## 学习准备

1. 具备1年代码经验，熟悉python
* 了解HTML，以及网络传输的基础知识
* 以一个全新的心态面对这个学习过程
    * 一定能学会，因为我自己也只是个PM
    * jupyter notebook 特有的交互式展示方式，很好的还原了爬虫运行的每个环节，一看就懂


## 学习大纲：

1. 初级-入门（Requests + BeautifulSoup）
    * [00_Getting_Started](./00_Getting_Started.ipynb)：最简单的爬虫，以及解析数据，存储成json  
    * [01_Advanced_Request](./01_Advanced_Request.ipynb)：访问被拒？加cookie和headers，以及如何自动识别要爬取的内容 
    * [02_Crawler_Sample](./02_Crawler_Sample.ipynb)：批量爬页面，完整实现bilibili搜索结果的爬取
* 中级-大量数据（Proxy + Redis + Pandas）
    * [11_Proxy_Request](./11_Proxy_Request.ipynb)：批量爬取免费代理，自动切换健康的代理
    * [12_Database](./12_Database.ipynb)：数据库 Redis，支持高性能数据读写 
    * [13_Data_Analysis](./13_Data_Analysis.ipynb)数据分析 pandas
* 高级-海量数据
    * Scrapy:探索式爬取,断点续爬
    * MongoDB:分布式存储
    * Vaex:海量数据分析(一个开源的 DataFrame 库)
    * 云端爬虫：服务器部署
    * APP爬虫：seleium模拟登陆，获取cookie


## 学习资料：

1. [nbdev](https://github.com/fastai/nbdev):fastai开源的探索式编程IDE
    * [官方完整的一步一步教程](http://nbdev.fast.ai/tutorial/#Set-up-Repo)
    * [用模板创建](https://github.com/fastai/nbdev_template/generate)一个github项目 
    * 修改setting.ini 所有配置都在这里
    * nbdev_build_lib 生成.py的文件 [其他命令](http://nbdev.fast.ai/cli/)
    * nbdev_build_docs 生成文档所需文件
* [Anaconda](https://www.anaconda.com/distribution/) 打包了用Python进行数据分析需要的一切环境
* [Jupyter](https://jupyter.org/) Notebook 基于Web的交互式计算环境
    * Enter/双击: 进入编辑模式
    * Esc: 退出编辑模式
    * 命令行/非编辑模式
        * D,D: 删除选中单元格
        * A/B: 上方/下方插入新代码块
        * H: 显示快捷键
        * O: 选择单元格的输出
    * 编辑模式
        * ⇧↩: 运行代码块, 并选择下面的代码块
        * ⇧M: 合并选中单元格
* [markdown](https://www.runoob.com/markdown/md-tutorial.html)一种轻量级标记语言，可以便捷的为这里的文字添加样式



## 其他教程
* https://github.com/wistbean/learn_python3_spider
* https://github.com/Kr1s77/Python-crawler-tutorial-starts-from-zero

