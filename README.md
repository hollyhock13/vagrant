# vagrant

Vagrant的主要概念
Provider
Provider指的是为Vagrant提供虚拟化支持的具体软件，比如vmware或virtual box。
Box
Box代表虚拟机镜像。Vagrant根据Porvider的不同提供了很多的基础镜像（通过url从s3上获取），用户可以根据自己的需求使用vagrant package制作属于自己的box。
Project
一个目录和目录中的Vagrantfile就组成了vagrant的一个项目，项目下可以有子项目，子项目中的Vagrantfile配置将继承和重写父项目的配置。项目的虚拟机实例并不会存储在这个目录（存储在~/.vagrant.d/box下），所以可以通过git等版本管理工具来管理项目。
Vagrantfile
Vagrant的配置文件，使用Ruby的语法描述。里面定义了项目所使用的box，网络，共享目录，provision脚本等。当vagrant up命令运行时，将读取当前目录的Vagrantfile。
Provisioning
Provisioning指的是虚拟机实例启动后，所需要完成的基础配置工作，比如说安装LAMP服务等。Vagrant支持使用shell，puppet，chef来完成provisioning工作。
Plugin
Vagrant提供了插件机制，可以很好的扩展对宿主机OS, GuestOS，Provider，Provisioner的支持，比如vagrant的aws和openstack支持都是通过plugin来实现的。



G:\work\vagrant>vagrant init bento/ubuntu-16.04 --box-version 201906.18.0
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.


vagrant up 
