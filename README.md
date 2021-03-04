# 4. 机型适配

<b>* 标准流程</b>

下载完代码以后, 在开源项目根目录, 执行以下命令初始化开发环境: 

    $ source build/envsetup.sh

创建一个新的机型工程的目录(以demo为例), 后续的移植都在机型目录完成。

    $ mkdir -p devices/demo
    $ cd devices/demo

按照如下步骤，完成一个新机型的适配：

    $ makeconfig      # 生成机型配置文件Makefile
    $ make newproject  # 生成新机型目录
    $ make patchall    # 自动插桩
    $ make fullota     # 生成适配完成的ROM包


<b>* 冲突处理</b>

自动插桩可能会造成代码合并冲突。冲突会以下面的形式标注出来, 开发者需要在厂商的文件中手工解决这些冲突。

    <<<<<<< VENDOR
      原厂的代码块
    =======
       exTHmUI的代码块
    >>>>>>> BOSP


# 5. 贡献代码

我们鼓励开发者为开源社区作出贡献。利用Github的Pull-Request机制，便可将内容变更发送给' exTHmUI-patchrom '审阅。

![image](github-pull-request.png)

- 首先，在github页面上，点击“Fork”，将'exTHmUI-patchrom'的git库拷贝到自己账户
- 然后，对拷贝的git库进行修改，将内容变更提交到自己的账户
- 最后，在github页面上，点击"New pull request"，向' exTHmUI-patchrom '发起代码审阅



