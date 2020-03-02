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
    * 最简单的爬虫，以及解析数据，存储成json  [00_Getting_Started](/notebooks/crawler_from_scratch/nbs/00_Getting_Started.ipynb)
    * 加cookie和headers，如何获取 [01_Advanced_Request](/notebooks/crawler_from_scratch/nbs/01_Advanced_Request.ipynb)
    * 批量爬页面
* 中级-大量数据
    * 代理
    * 数据库
    * 数据分析 numpy matplot
    * 探索式爬取
    * 断点续爬
* 高级-海量数据
    * 分布式存储？
    * seleium模拟登陆，获取cookie
    * 海量数据分析 vaex 一个开源的 DataFrame 库
    * 服务器部署



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
!pip install nbdev -U
```

    Collecting nbdev
      Using cached https://files.pythonhosted.org/packages/c4/7a/a3a3ec1018cf8d054e92c0856c2aea4232bcc5147172b88170b2467d6f33/nbdev-0.2.12-py3-none-any.whl
    Collecting nbconvert>=5.6.1 (from nbdev)
    [?25l  Downloading https://files.pythonhosted.org/packages/79/6c/05a569e9f703d18aacb89b7ad6075b404e8a4afde2c26b73ca77bb644b14/nbconvert-5.6.1-py2.py3-none-any.whl (455kB)
    [K     |████████████████████████████████| 460kB 16kB/s eta 0:00:016
    [?25hRequirement already satisfied, skipping upgrade: nbformat>=4.4.0 in /opt/anaconda3/lib/python3.7/site-packages (from nbdev) (4.4.0)
    Requirement already satisfied, skipping upgrade: pyyaml in /opt/anaconda3/lib/python3.7/site-packages (from nbdev) (5.1.2)
    Requirement already satisfied, skipping upgrade: fastscript in /opt/anaconda3/lib/python3.7/site-packages (from nbdev) (0.1.4)
    Requirement already satisfied, skipping upgrade: packaging in /opt/anaconda3/lib/python3.7/site-packages (from nbdev) (19.2)
    Requirement already satisfied, skipping upgrade: traitlets>=4.2 in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (4.3.3)
    Requirement already satisfied, skipping upgrade: defusedxml in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (0.6.0)
    Requirement already satisfied, skipping upgrade: bleach in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (3.1.0)
    Requirement already satisfied, skipping upgrade: testpath in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (0.4.2)
    Requirement already satisfied, skipping upgrade: pygments in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (2.4.2)
    Requirement already satisfied, skipping upgrade: jinja2>=2.4 in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (2.10.3)
    Requirement already satisfied, skipping upgrade: entrypoints>=0.2.2 in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (0.3)
    Requirement already satisfied, skipping upgrade: pandocfilters>=1.4.1 in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (1.4.2)
    Requirement already satisfied, skipping upgrade: jupyter-core in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (4.5.0)
    Requirement already satisfied, skipping upgrade: mistune<2,>=0.8.1 in /opt/anaconda3/lib/python3.7/site-packages (from nbconvert>=5.6.1->nbdev) (0.8.4)
    Requirement already satisfied, skipping upgrade: jsonschema!=2.5.0,>=2.4 in /opt/anaconda3/lib/python3.7/site-packages (from nbformat>=4.4.0->nbdev) (3.0.2)
    Requirement already satisfied, skipping upgrade: ipython-genutils in /opt/anaconda3/lib/python3.7/site-packages (from nbformat>=4.4.0->nbdev) (0.2.0)
    Requirement already satisfied, skipping upgrade: six in /opt/anaconda3/lib/python3.7/site-packages (from packaging->nbdev) (1.12.0)
    Requirement already satisfied, skipping upgrade: pyparsing>=2.0.2 in /opt/anaconda3/lib/python3.7/site-packages (from packaging->nbdev) (2.4.2)
    Requirement already satisfied, skipping upgrade: decorator in /opt/anaconda3/lib/python3.7/site-packages (from traitlets>=4.2->nbconvert>=5.6.1->nbdev) (4.4.0)
    Requirement already satisfied, skipping upgrade: webencodings in /opt/anaconda3/lib/python3.7/site-packages (from bleach->nbconvert>=5.6.1->nbdev) (0.5.1)
    Requirement already satisfied, skipping upgrade: MarkupSafe>=0.23 in /opt/anaconda3/lib/python3.7/site-packages (from jinja2>=2.4->nbconvert>=5.6.1->nbdev) (1.1.1)
    Requirement already satisfied, skipping upgrade: pyrsistent>=0.14.0 in /opt/anaconda3/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat>=4.4.0->nbdev) (0.15.4)
    Requirement already satisfied, skipping upgrade: setuptools in /opt/anaconda3/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat>=4.4.0->nbdev) (41.4.0)
    Requirement already satisfied, skipping upgrade: attrs>=17.4.0 in /opt/anaconda3/lib/python3.7/site-packages (from jsonschema!=2.5.0,>=2.4->nbformat>=4.4.0->nbdev) (19.2.0)
    [31mERROR: spyder 3.3.6 requires pyqt5<5.13; python_version >= "3", which is not installed.[0m
    [31mERROR: spyder 3.3.6 requires pyqtwebengine<5.13; python_version >= "3", which is not installed.[0m
    Installing collected packages: nbconvert, nbdev
      Found existing installation: nbconvert 5.6.0
        Uninstalling nbconvert-5.6.0:
          Successfully uninstalled nbconvert-5.6.0
      Found existing installation: nbdev 0.2.9
        Uninstalling nbdev-0.2.9:
          Successfully uninstalled nbdev-0.2.9
    Successfully installed nbconvert-5.6.1 nbdev-0.2.12


```python
!nbdev_build_lib
# !nbdev_build_docs
```

    Traceback (most recent call last):
      File "/opt/anaconda3/bin/nbdev_build_lib", line 10, in <module>
        sys.exit(nbdev_build_lib())
      File "/opt/anaconda3/lib/python3.7/site-packages/fastscript/core.py", line 73, in _f
        func(**args.__dict__)
      File "/opt/anaconda3/lib/python3.7/site-packages/nbdev/cli.py", line 20, in nbdev_build_lib
        write_tmpls()
      File "/opt/anaconda3/lib/python3.7/site-packages/nbdev/export2html.py", line 357, in write_tmpls
        write_tmpl(config_tmpl, 'user lib_name title copyright description', cfg, cfg.doc_path/'_config.yml')
      File "/opt/anaconda3/lib/python3.7/site-packages/nbdev/export2html.py", line 351, in write_tmpl
        dest.write_text(outp)
      File "/opt/anaconda3/lib/python3.7/pathlib.py", line 1225, in write_text
        with self.open(mode='w', encoding=encoding, errors=errors) as f:
      File "/opt/anaconda3/lib/python3.7/pathlib.py", line 1193, in open
        opener=self._opener)
      File "/opt/anaconda3/lib/python3.7/pathlib.py", line 1046, in _opener
        return self._accessor.open(self, flags, mode)
    FileNotFoundError: [Errno 2] No such file or directory: '/Users/Neo/crawler_from_scratch/docs/_config.yml'


```python
!git status
```

    On branch master
    Your branch and 'origin/master' have diverged,
    and have 1 and 1 different commits each, respectively.
      (use "git pull" to merge the remote branch into yours)
    
    All conflicts fixed but you are still merging.
      (use "git commit" to conclude merge)
    
    Changes to be committed:
    
    	[32mnew file:   ../_config.yml[m
    
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    
    	[31m../data/[m
    	[31m../docs/Getting_Started.html[m
    	[31m../docs/index.html[m
    	[31m./[m
    


```python
# add和commit合成一条
!git commit -a -m "Upadate 3: advanced request"
```

    [master 3ac2e98] Upadate 3: advanced request


```python
# 第一次push需要用户名密码，可能需要在terminal输入
# 因为国内push总超时，这是用shadowsocks代理的方法
!git config --global http.https://github.com.proxy socks5://127.0.0.1:1086
!git config --global https.https://github.com.proxy socks5://127.0.0.1:1086
!git push
```

    Enumerating objects: 12, done.
    Counting objects: 100% (10/10), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (6/6), done.
    Writing objects: 100% (6/6), 573 bytes | 573.00 KiB/s, done.
    Total 6 (delta 3), reused 0 (delta 0)
    remote: Resolving deltas: 100% (3/3), completed with 2 local objects.[K
    remote: 
    remote: GitHub found 1 vulnerability on neo4dev/crawler_from_scratch's default branch (1 moderate). To find out more, visit:[K
    remote:      https://github.com/neo4dev/crawler_from_scratch/network/alerts[K
    remote: 
    To https://github.com/neo4dev/crawler_from_scratch.git
       67a8969..3ac2e98  master -> master


```python
!git pull
```

    remote: Enumerating objects: 10, done.[K
    remote: Counting objects: 100% (10/10), done.[K
    remote: Compressing objects: 100% (6/6), done.[K
    remote: Total 7 (delta 4), reused 0 (delta 0), pack-reused 0[K
    Unpacking objects: 100% (7/7), done.
    From https://github.com/neo4dev/crawler_from_scratch
       1e2fc73..67a8969  master     -> origin/master
     * [new branch]      dependabot/bundler/docs/nokogiri-1.10.8 -> origin/dependabot/bundler/docs/nokogiri-1.10.8
    hint: Waiting for your editor to close the file... 7[?47h[?1h=[?2004h[1;24r[?12h[?12l[22;2t[22;1t[29m[m[H[2J[?25l[24;1H"~/crawler_from_scratch/.git/MERGE_MSG" 7L, 300C[2;1H▽[6n[2;1H  [1;1H[>c]10;?]11;?[1;1HMerge branch 'master' of https://github.com/neo4dev/crawler_from_scratch
    
    # Please enter a commit message to explain why this merge is necessary,
    # especially if it merges an updated upstream into a topic branch.
    #
    # Lines starting with '#' will be ignored, and an empty message aborts
    # the commit.
    [1m[34m~                                                                               [9;1H~                                                                               [10;1H~                                                                               [11;1H~                                                                               [12;1H~                                                                               [13;1H~                                                                               [14;1H~                                                                               [15;1H~                                                                               [16;1H~                                                                               [17;1H~                                                                               [18;1H~                                                                               [19;1H~                                                                               [20;1H~                                                                               [21;1H~                                                                               [22;1H~                                                                               [23;1H~                                                                               [1;1H[?25h[?25l[m[24;1HType  :qa  and press <Enter> to exit Vim[24;41H[K[1;1H[?25h
