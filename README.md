# 从零学习爬虫 Crawler from scratch
> 运用Jupyter Notebook 演示爬虫是如何运作的


## 学习准备

1. 具备1年代码经验，熟悉python
* 了解HTML，以及网络传输的基础知识
* 以一个全新的心态面对这个学习过程
    * 一定能学会，因为我自己也只是个PM
    * jupyter notebook 特有的交互式展示方式，很好的还原了爬虫运行的每个环节，一看就懂


## 学习大纲：

1. 初级-入门
    * 最简单的爬虫，以及解析数据，存储成json  [00_Getting_Started](/notebooks/crawler_from_scratch/index.ipynb)
    * 加cookie和headers，如何获取
    * 批量爬页面
* 中级-大量数据
    * 代理
    * 数据库
    * 数据分析 numpy matplot
* 高级-海量数据
    * 分布式


## 学习资料：

1. [nbdev](https://github.com/fastai/nbdev):fastai开源的探索式编程IDE
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



## 发布
> 将文件打包，上传到github

```python
!nbdev_build_lib
!nbdev_build_docs
```

    Converted 00_Getting_Started.ipynb.
    Converted index.ipynb.


```python
!git status
# add和commit合成一条
!git commit -a -m "Upadate 1: write the summary of this project"
```

```python
# 第一次push需要用户名密码，可能需要在terminal输入
# 因为国内push总超时，这是用shadowsocks代理的方法
!git config --global http.https://github.com.proxy socks5://127.0.0.1:1086
!git config --global https.https://github.com.proxy socks5://127.0.0.1:1086
!git push
```
