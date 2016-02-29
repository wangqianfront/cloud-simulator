# cloud-simulator


云计算日益热门，借此实验一些关键性技术。记录一些实验过程与心得。

1.背景

1.1 硬件
◾二个linode vps
◾一个阿里云标准C套餐
◾两台公司淘汰下来的2U服务器，一台1U服务器
◾联通光纤+独立ip

1.2 目的
◾实现完全自动化地部署
◾R Hadoop 大数据计算实验，跑Map reduce任务
◾任意开服

1.3 测试数据
◾微博2012年23G测试数据
◾大脑结构数据

2. vagrant与veewee

2.1 vagrant基础
◾Vagrant Documentation
◾［教學]使用Vagrant練習環境佈署 - 好麻煩部落格](http://gogojimmy.net/2013/05/26/vagrant-tutorial/)

vagrant box 列表：
◾A list of base boxes for Vagrant - Vagrantbox.es

国内访问速度不行，我提供的dropbox镜像：
◾https://www.dropbox.com/s/jgpdtomcgpshd4s/precise-server-cloudimg-amd64-vagrant-disk1.box
◾https://www.dropbox.com/s/7h5ynztb4hektut/quantal64-vanilla.box
◾https://www.dropbox.com/s/yovpjswe00cdlox/opscode_ubuntu-12.04-i386_chef-11.4.4.box

2.2 vagrant、lindoe vps与kvm等

vagrant加载linode vps镜像
◾Copying a Disk Image Over SSH – Linode Library

vagrant与Cloud Foundry

Installing Cloud Foundry on Vagrant | Cloud Foundry Blog

2.3 制作包：veewee
◾jedi4ever/veewee

3. 配置管理：chef

3.1 chef基础
◾Getting Started with Chef

3.2 chef的三种配置方式
◾chef-solo
◾chef-server
◾hosted chef

第一种方式的教程：
◾［Rails佈署實戰教學]使用Chef-Solo一鍵安裝機器 - 好麻煩部落格](http://gogojimmy.net/2013/06/01/Chef-Solo-Basic-with-Vagrant/)

第三种方式的教程：
◾ Converge the node - QuickStart Guide | Opscode Learn Chef 

3.3 最常用的方式：chef-solo

3.4 最佳实践：knife solo+berkshelf+railsbox

最佳流程：
◾第一步：knife solo 

knife-solo
◾第二步：berksfile文件

Berkshelf
◾第三步：整合Vagrantfile文件

名词解释：
◾RUNIT - UNIX初始化
◾Berkshelf

链接
◾#339 Chef Solo Basics (pro) - RailsCasts
◾How to include the Windows Cookbook Helper methods in your Chef recipe - Automate All the Things!

常见错误

4. 撰写box：Railsbox实例

4.1 基础box：appbox

4.2 撰写与定制个人的box

我写的部署box项目：
◾ouyangzhiping/railsbox
◾ouyangzhiping/railsbox-example

一键部署：基础server安装+postgresql+rbenv+rails+nginx+unicorn

5. 使用railsbox部署阿里云、linode vps与openstack

5.1 部署rails app

5.2 部署R app

6. openstack部署

6.1 一键部署

chef社区提供的：

Search Results for openstack - Opscode Community

常用的一键部署项目：
◾DevStack - Deploying OpenStack for Developers
◾StackGeek - Installing OpenStack on Ubuntu 12.04 LTS in 10 Minutes

国人写的：
◾onestack - A tool to deploy complete and real OpenStack cloud computing service.（一键部署OpenStack） - Google Project Hosting

6.2 openstack架构与基础
◾Introducing the OpenStack Operations Guide » The OpenStack Blog

Open Cloud

6.3 vagrant与openstack

6.4 openstack配套项目解析

图书：
◾开源云OpenStack技术指南 (豆瓣)

7. hadoop

7.1 hadoop部署

chef社区提供的部署项目
◾Search Results for hadoop - Opscode Community

7.2 hadoop与Python、R

python与hadoop
◾Writing An Hadoop MapReduce Program In Python - Michael G. Noll

7.3 hadoop实例

8 R in Cloud

8.1 Revolution R
◾Real-time Big Data Analytics: From Deployment to Production

8.2 高性能R项目

概述：
◾CRAN Task View: High-Performance and Parallel Computing with R

图书：
◾Parallel R

snow、multicore
◾CRAN - Package snow
◾CRAN - Package multicore

RHIPE
◾RHIPE
◾R and Hadoop: Step-by-step tutorials

PHDR
◾pbd: programming with big data in R

9 其它
