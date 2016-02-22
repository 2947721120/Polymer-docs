###CN
##相关资料
相关视频一[https://www.youtube.com/watch?v=YBNBr9ECXLo]
视频二[https://www.youtube.com/watch?v=g7f1Az5fxgU]
视频三[https://www.youtube.com/watch?v=CdV0VGYhKXk]
如果不懂英语,视频点击设置---显示字幕---字幕语言选择自动翻译
聚合物说明文档[https://elements.polymer-project.org/]

聚合物文档大多在降价与一些HTML。 [化身] [化身]使用
生成站点的静态HTML。输出被产生成
文件夹，名为'_site`和谷歌App Engine的服务。

我们使用杰基尔2.4和[咕噜] [咕噜]生成的文档，并指南针编译SASS为CSS。

##官网下载文件
官网下载的文件大多是无打开方式的单纯文件名,可以在文件名后加后缀.zip后即可打开


＃＃ 建立

在本节中，您将学习如何：

1.安装所有建立的网站所需要的工具
2.建立网站
3.在本地预览网站

这些安装说明进行了验证针对Mac OS X的10.10.3。

我们提供了对每个工具如何在构建使用简要说明
处理。构建过程是自动的，所以你并不真正需要
要知道这东西，但它会知道什么时候是非常有用
不如意的事情。

安装NPM：

    http://nodejs.org/download

故宫是一个JavaScript依赖管理。它是捆绑在一起的Node.js
默认。

安装捆扎机：

    创业板安装打捆--user安装

打捆是一个Ruby的依赖经理。我们用它来管理
杰基尔（我们用它来生成降价静态HTML工具），以及
它的依赖。

在命令中的`--user-install`标志上方安装宝石到您家
目录（通常`〜/ .gem /红宝石/ 1.9.1`）。默认行为是
安装到全系统的Ruby目录
（通常是`在/ var / lib中/宝石/ 1.9.1`），它可以创建各种
问题的路线。

如果红宝石警告您，用户安装目录是不是你
路径，加入以下到你的`.bashrc`文件现在添加
（或者您的开发环境是合适的）：

    PATH =“$ PATH：$（红宝石-rubygems -e'把Gem.user_dir'）/ BIN”

接下来，安装咕噜，硫化和鲍尔：

    NPM安装-g咕噜-CLI vulcanize@0.7凉亭

咕噜自动重复任务，如缩小文​​件
JavaScript中，SASS编译和部署的网站。
硫化（由高分子建队）减少HTML文件及其
依赖进口的HTML到一个文件中。鲍尔是另一种工具
管理JavaScript的依赖关系。

`硫化@ 0.7`指示NPM来istall版本0.7。如果省略此，
它会安装最新版本，它不发挥很好
我们构建的工具链。

该`-g`标志全球安装这些命令行工具，从而使
你可以在任何目录中使用它们。一些构建脚本的期望
这些工具是全局访问。

下载并安装谷歌应用程序引擎的Python SDK：

    https://cloud.google.com/appengine/downloads#Google_App_Engine_SDK_for_Python

我们将使用App Engine在本地预览和部署的网站。

克隆该存储库。例如起见，我们假设您克隆
它`〜/聚合物/ docs`。

    混帐克隆https://github.com/Polymer/docs.git

更改目录到该存储库。

    CD〜/聚合物/文档

安装杰基尔及其依赖：

    捆绑安装--path〜/ .gem

这将安装所有的宝石相同的位置，捆扎机，而
比全系统的Ruby目录。

安装步兵和其他各种工具构建/部署的网站：

    NPM安装

`npm`读取`package.json`并安装所有的依赖关系
它发现到`node_modules`。

目录更改为0.5文件目录：

    CD 0.5

安装了一堆的依赖关系：

    亭子安装

当凉亭指示您选择一个聚合物的版本，选择`0.5`。

目录更改为聚合物1.0版文件的目录：

    CD ../1.0

安装更多的依赖关系：

    亭子安装

当它会提示您指定要使用的高分子版本选择
`0.5`一次。

更改目录到`samples`目录：

    CD采样/

安装依赖：

    亭子安装

不同的是网站的其他部分，样品都建有高分子
版本1.0。

更改目录到仓库的根目录：

    CD ../ ..

建立的网站：

    咕噜文档

当咕噜运行`doc_merge：0_5`和`doc_merge：1_0`任务，你会看到
沿着无法的`行错误的列表，以找到@extends输入
核心input`或'无法找到@mixins从核心tooltip` CoreFocusable。您
可以放心地忽略这些错误。

本地部署的网站：

    咕噜

打开网页浏览器，并查看在以下位置的网站：

    HTTP：//本地主机：3000

你完成了。唷！

##进行编辑和预览变化

该回购（`聚合物/ docs`）是文档的源文件住的地方。做出改变：

1.一定要在你的文档目录下运行`NPM install`如果它是一个新的结帐。
2.火了`grunt`任务。该任务运行多个进程：一个本地应用程序引擎服务器，杰基尔，指南针，和硫化。该化身，指南针，和硫化任务都将监视文件修改和更新网站，如果你所做的任何修改。
**注：**化身生成静态网站一个名为`_site`文件夹中。它可能需要一些时间的文档完全再生和复制到输出文件夹......不断刷新！
3.编辑。

一旦更改好看，'混帐commit`他们和推动。

##发布：推文档

**注意**：只有项目拥有者可以发布的文档。

###本地预览

这是一个好主意，推文档之前运行'grunt`，因为它运行一些咕噜任务。验证事情进展得很顺利，并在本地使用开发服务器预览更改。

###更新应用程序

当更新聚合物网站使用的版本，请确保在下面的应用程序也更新：

- [教程]（https://github.com/Polymer/polymer-tutorial）
- [托皮卡（https://github.com/Polymer/topeka）
- [设计]（https://github.com/Polymer/designer）

解压候选发布到每个应用程序的`bower_components`目录，验证，然后运行该应用程序的`deploy.sh`脚本。在本教程的情况下，你需要按照在回购自己的部署指令。

＃＃＃ 发布

运行`凉亭update`，以确保您有最新的组件依赖性。

一旦这些更新，您需要更新一些版本的文档：

- 增量`app.yaml`的版本;
- 更新中`_config.yml`高分子发行版本。
- 添加在`changelog.md`一个链接点链接的发行说明。

构建文档：

    咕噜文档
    
在这一点上，与`grunt`运行开发服务器，并在本地预览的事情，以确保没有什么是可怕的
聚合物后打破，内容已经更新。

接下来，运行在`聚合物/ docs`目录的根目录的部署脚本：

    ./scripts/deploy_site.sh
    
这个脚本构建网站，API文档，运行硫化超过进口，并部署到App Engine。

最后一件事就是在App Engine管理控制台切换应用程序的版本。为了使文档活，撞了上去https://appengine.google.com/deployment?&app_id=s~polymer-project并选择您刚刚部署的版本。

[化身]：http://jekyllrb.com/
[咕噜咕噜]：http://gruntjs.com/

###EN
Polymer docs are mostly in Markdown with some HTML. [Jekyll][jekyll] is used 
to generate the static HTML for the site. The output is generated into a 
folder called `_site` and served from Google App Engine.

We use Jekyll 2.4 and [Grunt][grunt] to generate the documentation, and compass to compile SASS to CSS.



## Setup

In this section you learn how to:

1. install all of the tools needed to build the site
2. build the site
3. locally preview the site

These setup instructions were validated against Mac OS X 10.10.3.

We've included brief descriptions on how each tool is used in the build
process. The build process is automated, so you don't really need 
to know this stuff, but it will be very useful to know when
things go wrong.

Install npm:

    http://nodejs.org/download

npm is a JavaScript dependency manager. It is bundled with Node.js 
by default.

Install Bundler:

    gem install bundler --user-install 

Bundler is a Ruby dependency manager. We use it to manage 
Jekyll (the tool we use to generate static HTML from markdown), and 
its dependencies. 

The `--user-install` flag in the command above installs the gem to your home
directory (usually `~/.gem/ruby/1.9.1`). The default behavior is to
install to the system-wide Ruby directory
(usually `/var/lib/gems/1.9.1`) which can create all kinds of
problems down the line. 

If Ruby warns you that the user install directory is not on your
path, add it now by adding the following to your `.bashrc` file
(or whatever is appropriate for your development environment):

    PATH="$PATH:$(ruby -rubygems -e 'puts Gem.user_dir')/bin"

Next, install Grunt, Vulcanize, and Bower:

    npm install -g grunt-cli vulcanize@0.7 bower

Grunt automates repetitive tasks, like minifying 
JavaScript, compiling SASS, and deploying the website.
Vulcanize (built by the Polymer team) reduces HTML files and their 
dependent HTML imports into one file. Bower is another tool for
managing JavaScript dependencies.

`vulcanize@0.7` instructs npm to istall version 0.7. If you omitted this,
it would install the latest release, which does not play nicely
with our build toolchain.

The `-g` flag installs these command-line tools globally, so that 
you can use them in any directory. Some of the build scripts expect
the tools to be globally accessible.

Download and install the Google App Engine Python SDK:

    https://cloud.google.com/appengine/downloads#Google_App_Engine_SDK_for_Python

We'll use the App Engine to locally preview and deploy the website.

Clone this repository. For sake of example, we'll assume you clone 
it to `~/Polymer/docs`.

    git clone https://github.com/Polymer/docs.git

Change directories to this repository.

    cd ~/Polymer/docs

Install Jekyll and its dependencies:

    bundle install --path ~/.gem

This installs all gems to the same location as Bundler, rather 
than the system-wide Ruby directory.

Install Grunt and various other tools for building / deploying the site: 

    npm install

`npm` reads `package.json` and installs all of the dependencies
it finds into `node_modules`.

Change directories to the directory for 0.5 documents:

    cd 0.5

Install a bunch of dependencies:

    bower install

When bower instructs you to select a Polymer version, select `0.5`.

Change directories to the directory for Polymer version 1.0 documents:

    cd ../1.0

Install more dependencies: 

    bower install

When it prompts you to specify which version of Polymer to use, select
`0.5` again.

Change directories to the `samples` directory:

    cd samples/

Install dependencies:

    bower install

Unlike the rest of the website, the samples are built with Polymer
version 1.0.

Change directories to the root of the repository:

    cd ../..

Build the website:

    grunt docs

When grunt runs the `doc_merge:0_5` and `doc_merge:1_0` tasks, you will see 
a list of errors along the lines of `Unable to find @extends input from
core-input` or `Unable to find @mixins CoreFocusable from core-tooltip`. You
can safely ignore these errors.

Deploy the site locally:

    grunt

Open a web browser and view the website at the following location:

    http://localhost:3000

You're done. Phew!

## Making edits and previewing changes

This repo (`Polymer/docs`) is where the documentation source files live. To make a change:

1. Be sure to run `npm install` in your docs directory if it's a new checkout.
2. Fire up the `grunt` task. This task runs a number of processes: a local app engine server, jekyll, compass, and vulcanize. The jekyll, compass, and vulcanize tasks will all watch for file changes and update the site if you make any edits.
**Note:** Jekyll generates the static site in a folder named `_site`. It can take some time for the docs to fully regenerate and be copied to the output folder...keep refreshing!
3. Make your edits.

Once your changes look good, `git commit` them and push.

## Releases: pushing the docs

**Note**: only project owners can publish the documentation.

### Preview locally

It's a good idea to run `grunt` before pushing the docs, as it runs a number of grunt tasks. Verify things went well and preview your changes locally using the dev server.

### Update apps

When updating the version of Polymer that the site uses, make sure to also update it in the following apps:

- [Tutorial](https://github.com/Polymer/polymer-tutorial)
- [Topeka](https://github.com/Polymer/topeka)
- [Designer](https://github.com/Polymer/designer)

Unzip the release candidate into the `bower_components` directory of each app, verify, then run the app's `deploy.sh` script. In the case of the Tutorial, you'll need to follow the deploy instructions on the repo itself.

### Release

Run `bower update` to make sure you have the latest component dependencies.

Once these are updated, you need to update some versions for the docs:

- Increment the version in `app.yaml`;
- Update the Polymer release version in `_config.yml`.
- Add a link point link to the release notes in `changelog.md`.

Build the docs:

    grunt docs
    
At this point, run the dev server with `grunt`, and preview things locally to make sure nothing is terribly
broken after Polymer and the elements have been updated. 

Next, run the deploy script in the root of the `Polymer/docs` directory:

    ./scripts/deploy_site.sh
    
This script builds the site, api docs, runs Vulcanizer over the imports, and deploys to App Engine.    

Last thing is to switch the app version in the App Engine admin console. To make the docs live, hit up https://appengine.google.com/deployment?&app_id=s~polymer-project and select the version you just deployed.

[jekyll]: http://jekyllrb.com/
[grunt]: http://gruntjs.com/
